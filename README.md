McKinley Park Development Council
=====================

This is the repository for the [McKinley Park Development Council website](https://mckinleyparkdevelopmentcouncil.org/).

This version was initially forked from the Lets Encrypt website's code.

This site is built with [Hugo](https://gohugo.io/). It's entirely static, no server-side code/scripting.

To see your changes, [install
Hugo](https://gohugo.io/getting-started/installing), then run it with:

```
hugo server -F
```

And open <a href="http://localhost:1313/">http://localhost:1313/</a> in your
browser. Note that the -F flag will show items to be published in the future
(like blog posts with dates in the future).

Here is a deploy script that makes deploying a site and then updates to a site a one command operation:

```
#!/bin/sh
USER=[server user name]
HOST=[server host name]
DIR=[path to web root]   # can be be initially empty!

hugo && rsync -avz --delete public/ ${USER}@${HOST}:~/${DIR}

exit 0
```

Contributions welcome.


