---
title: Debugging Ray Payloads
weight: 1
---

When developing a Ray Library, you may find it necessary to debug the data being sent to the Ray app.

You may use the following third-party package to intercept and display the data being sent from your code to the Ray app:

[permafrost-dev/ray-proxy](https://github.com/permafrost-dev/ray-proxy)

## Usage

Install `ray-proxy` as you would any other npm package:

```bash
npm install ray-proxy --save-dev
```

First, set your port in the Ray app to `23516` in the preferences. Finally, run the proxy:

```bash
./node_modules/.bin/ray-proxy
```

Once you start sending ray messages, you'll see the raw payloads being sent in the proxy, along with statistics!
