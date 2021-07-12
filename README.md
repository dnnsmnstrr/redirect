# redirect

A proxy for my [redirect-api](https://github.com/dnnsmnstrr/api/blob/master/pages/api/redirect/redirects.js), so it can be accessed via https on a simple url, namely [muensterer.link](https://muensterer.link)

When called with an [available route](https://dnnsmnstrr.vercel.app/api/redirect/redirects), for example https://muensterer.link/gh will return my github profile. Some redirects can even be extended with paths or parameters, so http://muensterer.link/gh/api will expand to https://github.com/dnnsmnstrr/api or http://muensterer.link/zk/helloworld will become https://dnnsmnstrr.github.io/zettelkasten/helloworld

How it works is that the [index.html](./index.html), which is served via Pages, uses a meta tag to refresh the page after changing the window location and adding a `noReturn`-parameter, to avoid redirect-loops.
