---
layout: post
title: "Share your localhost over the internet"
date: 2022-06-22
category: misc
---

You can use Cloudflare to easily setup a secure and temporary tunnel for anyone to access your local deployment over the internet.

Imagine you just build your first [Jekyll](/misc/2022/06/11/welcome-to-jekyll.html) website and you run it localy at [http://localhost:4000](http://localhost:4000). Just install [`cloudflared`](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/tunnel-guide/#set-up-a-tunnel-locally-cli-setup) (no need to create an account and authenticate) and run:
```shell
cloudflared tunnel --url http://localhost:4000
```

The output will give you a temporary URL on which you anyone can reach your machine:
```
2022-06-22T19:27:12Z INF Requesting new quick Tunnel on trycloudflare.com...
2022-06-22T19:27:14Z INF +--------------------------------------------------------------------------------------------+
2022-06-22T19:27:14Z INF |  Your quick Tunnel has been created! Visit it at (it may take some time to be reachable):  |
2022-06-22T19:27:14Z INF |  https://assigned-peninsula-hd-macro.trycloudflare.com                                     |
2022-06-22T19:27:14Z INF +--------------------------------------------------------------------------------------------+
```
