# content-root

The root of the content hierarchy.

Although there is no single, global content hierarchy, we pretend that there is. 

No, this is more like a sample assembly where multiple individual content repositories will be assembled in a single hierarchy, by means of .externals. Whoever checks out this repo and ```ext up```s its externals will have access to the sample content hierarchy. Everybody is free to create their own collections, using .external files or other mechanisms that seem fit. It will hopefully clarify once there is a critical mass of examples. 

The content items may contain their own transpect configuration overrides. If they are part of a collection (for example, a book series), the collection’s transpect configuration should be stored below the transpect [code repo](https://github.com/consortium/BinB/tree/master/transpect/adaptions/), and the mapping between code and content repo paths should be laid out in a [configuration file](https://subversion.le-tex.de/common/pubcoach/trunk/schema/transpect-conf.rng) (see [setup manual](https://subversion.le-tex.de/common/transpect-demo/content/le-tex/setup-manual/en/out/xhtml/transpect-setup.xhtml#sec-cascade)).

It can be checked out anywhere, but if you put it next to your local copy of [transpect](https://github.com/consortium/BinB/tree/master/transpect), you will avoid some extra XML catalog configuration.

Example (cloning via ssh):

    git clone git@github.com:consortium/content-root.git content

So that it looks like that:

    $ ll
    total 6
    drwxr-xr-x+ 1 gerrit None  0 Feb 23 21:56 content/
    -rw-r--r--  1 gerrit None 23 Feb  1 10:10 README.md
    drwxr-xr-x+ 1 gerrit None  0 Feb 23 20:06 transpect/

Then

    cd content
    ext co
    
(see [the ext tutorial](http://nopugs.com/ext-tutorial)).
