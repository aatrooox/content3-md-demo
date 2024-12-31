---
title: issue3
date: 2024-11-08
lastmod: 2024-11-08
tags: [Nitro, issue]
versions: ["@nuxt/content@2.13.4"]
---

使用`nuxt/content` 时，抛出警告:

@nuxt/content warn：

```bash
[@nuxt/content 09:52:13] Using <NuxtLayout> inside app.vue will cause unwanted layout shifting in your application.
```

在nuxt.config.ts中配置解决：

The layout warning is resolved by the following nuxt config: 

```bash
content: {
        documentDriven: {
            injectPage: false // turn off injectPage because we are using our own [...slug].vue
        },
        ...
}
```

Github issues :

[NuxtLayout warn vs documentation #15240](https://github.com/nuxt/nuxt/issues/15240)  find the comment by `zzdaddy`

[nuxt-blog-starter](https://github.com/dan-bowen/nuxt-blog-starter/pull/9) closed

