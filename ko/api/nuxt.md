---
title: "API: Nuxt(options)"
description: nuxt.js 의 programmatically 을 사용하면, 렌더링 시 원하는 방식으로 서버를 구성할 수 있는 미들웨어로 사용할 수 있습니다.
---

# Nuxt.js Programmatically 사용

미들웨어와 API 만을 사용하여 서버를 구성해야 할 수도 있기에, Nuxt.js programmatically을 사용해야합니다.
Nuxt.js 는 코드가 좀 더 재미있고, 깔끔하게 읽을 수 있게 만들어주는 ES2015 를 기반으로 구현되었습니다. 코드는 별다른 트랜스파일러를 사용하지 않으며, 코어 V8 엔진에만 의존합니다. 때문에 Nuxt.js 는 Node.js `4.0` 또는 `그 이상의 버전` 을 대상으로 합니다.

require를 통해 Nuxt.js를 사용할 수 있습니다.
```js
const Nuxt = require('nuxt')
```

## Nuxt(options)

Nuxt.js의 옵션을 보려면, configuration section 을 확인해보세요.

```js
const options = {}

const nuxt = new Nuxt(options)
nuxt.build()
.then(() => {
  // nuxt.render(req, res) 또는 nuxt.renderRoute(route, context) 를 사용할 수 있습니다.
})
```
[nuxt-express](https://github.com/nuxt/express), [adonuxt](https://github.com/nuxt/adonuxt)를 사용하면 빠르게 시작할 수 있습니다.

### 디버그 로그

nuxt.js 로그가 화면에 표시되는 것을 원한다면, 파일의 최상단에 아래와 같은 코드를 추가하시면 됩니다.

```js
process.env.DEBUG = 'nuxt:*'
```
