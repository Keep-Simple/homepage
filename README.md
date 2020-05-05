This is just a résumé for my buddy Donald Trump <sup>🐷</sup>

## Links
[Jump to Trumps' resume](https://keep-simple.github.io/homepage/index.html)

[Dive to AWS production-bucket](http://keep-simple-homepage-production.s3-website.eu-central-1.amazonaws.com/index.html)

## Info
I Host it with [**GitHub Pages**](https://pages.github.com/), because it's so much easier, cost efficient, and saves me time on deployments. Other than that it's just good old plain HTML and CSS with a very little bit of JavaScript. `<head>` is built using excellent [**HEAD**](https://github.com/joshbuchea/HEAD) for reference, `<body>` uses some of the styles from the great [**Semantic UI**](https://github.com/Semantic-Org/Semantic-UI) framework. Website is frequently tested with [**Lighthouse**](https://developers.google.com/web/tools/lighthouse/) automated tool. Amazing [**Workbox**](https://developers.google.com/web/tools/workbox/) helps build a decent Service Worker for this website _(hence it even works offline)_, [**serve**](https://zeit.co/blog/serve-7) is used to run my website locally during development. I have [**workbox**](https://github.com/GoogleChrome/workbox) and [**serve**](https://github.com/zeit/serve) npm packages installed globally with `sudo npm install --global workbox-cli serve`, and I've also set up a pre-commit git hook which automatically runs `workbox generateSW workbox-config.js` before I commit and push my code to GitHub, so that I don't have to do it manually every time I make changes. **.git/hooks/pre-commit** looks as simple as this:

``` bash
#!/bin/sh
if workbox generateSW workbox-config.js ; then
  git add sw.js
  exit 0
else
  echo "Cannot generate sw.js"
  echo "Aborting"
fi
```

------

_“Taken from my mentor”_ <sup>🐷</sup>
