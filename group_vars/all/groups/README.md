# LUGs
Here is a list of LUGs (and [inactive](inactive/) LUGs) which are hosted on the
lug.org.uk servers. At the time of writing the "flags" required here are:

* `state`: (default) `active` or `inactive`
* `hosting`: the server storing the hosting values - usually either (default) 
`snm` or `web-01`
* `web`: `redirect`, `jekyll`, `dokuwiki`, `php` or (default) `static`
* `target`: used by `web: redirect` to indicate where to forward traffic to, or
by `web: jekyll` to indicate what the git source is for the jekyll site.
(default: '')
