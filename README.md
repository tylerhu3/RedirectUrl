# RedirectUrl

Stable Netlify address for TylerTube. TylerTube runs at home behind a Cloudflare quick tunnel
whose `*.trycloudflare.com` URL changes on every restart; this site 302-redirects to the current one.

`_redirects` and `index.html` are **generated** by `scripts/tunnel.mjs` in the TylerTube repo
(`npm run deploy:public`, or the `com.tylertube.tunnel` LaunchAgent) and pushed automatically.
Don't edit them by hand. The redirect is 302 on purpose: browsers cache 301s forever.
