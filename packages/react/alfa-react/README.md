# Alfa (React Version)

标准微前端 API 的 React 版本，面向最终用户。

# Usage

创建 Alfa 微应用

```javascript
import { createAlfaWidget, createAlfaApp } from '@alicloud/alfa-react';

const AlfaMicroApp = createAlfaWidget({
  name: '@ali/example',
  version: '1.0'
});


const App = () => {
  return <AlfaMicroApp />
}
```

创建历史 Widget

```javascript
import { createAlfaWidget } from '@alicloud/alfa-react';

const AlfaWidget = createAlfaWidget({
  name: '@ali/example',
  version: '1.x'
});


const App = () => {
  return <AlfaWidget />
}
```

```javascript
import { createAlfaWidget } from '@alicloud/alfa-react';

const AlfaWidget = createAlfaWidget({
  name: '@ali/example',
  url: 'https://some-url/index.js'
});


const App = () => {
  return <AlfaWidget />
}
```

# API

```createAlfaWidget(AlfaFactoryOption)``` or ```createAlfaApp(AlfaFactoryOption)```

## AlfaFactoryOption

| 属性名         | 类型                                       | 说明                    | 默认值    |
| ------------- | ------------------------------------------ | ---------------------- | --------- |
| name            | `id: string;`                              | widget or alfa app ID  | -  |
| version       | `version?: string;`                         | 微应用版本               | -  |
| env           | `env?: 'prod' | 'local' | 'pre' | 'daily'` | 当前环境                 | -  |
| loading       | `loading?: boolean | React.ReactChild;`    | 微应用加载的 loading 展示 | -  |
| manifest           | ```manifest?: string;```                        | manifest URL         | - |