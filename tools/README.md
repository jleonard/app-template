# Tools #
The tools provided are a combination of [phantomjs](http://phantomjs.org/) and [casperJS](http://casperjs.org/) scripts.

### Installation ###
* Download & install [phantomjs](http://phantomjs.org/download.html)
* Download & install [casperJS](http://casperjs.org/installation.html)

## YSlow (for PhantomJS) ##
http://yslow.org/phantomjs/

Usage: phantomjs [phantomjs options] yslow.js [yslow options] [url ...]

  PhantomJS Options:

    http://y.ahoo.it/phantomjs/options

  YSlow Options:

    -h, --help               output usage information
    -V, --version            output the version number
    -i, --info <info>        specify the information to display/log (basic|grade|stats|comps|all) [all]
    -f, --format <format>    specify the output results format (json|xml|plain|tap|junit) [json]
    -r, --ruleset <ruleset>  specify the YSlow performance ruleset to be used (ydefault|yslow1|yblog) [ydefault]
    -b, --beacon <url>       specify an URL to log the results
    -d, --dict               include dictionary of results fields
    -v, --verbose            output beacon response information
    -t, --threshold <score>  for test formats, the threshold to test scores ([0-100]|[A-F]|{JSON}) [80]
                             e.g.: -t B or -t 75 or -t '{"overall": "B", "ycdn": "F", "yexpires": 85}'
    -u, --ua "<user agent>"  specify the user agent string sent to server when the page requests resources
    -vp, --viewport <WxH>    specify page viewport size WxY, where W = width and H = height [400x300]
    -ch, --headers <JSON>    specify custom request headers, e.g.: -ch '{"Cookie": "foo=bar"}'
    -c, --console <level>    output page console messages (0: none, 1: message, 2: message + line + source) [0]

  Examples:

    phantomjs yslow.js http://yslow.org
    phantomjs yslow.js -i grade -f xml www.yahoo.com www.cnn.com www.nytimes.com
    phantomjs yslow.js -info all --format plain --ua "MSIE 9.0" http://yslow.org
    phantomjs yslow.js -i basic --rulseset yslow1 -d http://yslow.org
    phantomjs yslow.js -i grade -b http://www.showslow.com/beacon/yslow/ -v yslow.org
    phantomjs --load-plugins=yes yslow.js -vp 800x600 http://www.yahoo.com
    phantomjs yslow.js -i grade -f tap -t 85 http://yslow.org


## Crawl (for CasperJS) ##
