<p align="center">
  <a href="https://docsify.js.org">
    <img alt="docsify" src="./docs/_media/icon.svg">
  </a>
</p>

<p align="center">
  A magical documentation site generator.
</p>

<p align="center">
  <a href="#backers"><img alt="Backers on Open Collective" src="https://opencollective.com/docsify/backers/badge.svg?style=flat-square"></a>
  <a href="#sponsors">
    <img alt="Sponsors on Open Collective" src="https://opencollective.com/docsify/sponsors/badge.svg?style=flat-square"></a>
  <a href="https://github.com/docsifyjs/docsify/actions/workflows/test.yml"><img src="https://github.com/docsifyjs/docsify/actions/workflows/test.yml/badge.svg" alt="Build & Test"></a>
  <a href="https://www.npmjs.com/package/docsify"><img alt="npm" src="https://img.shields.io/npm/v/docsify.svg?style=flat-square"></a>
  <a href="https://discord.gg/3NwKFyR"><img alt="Join Discord community and chat about Docsify" src="https://img.shields.io/discord/713647066802421792.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2&cacheSeconds=60"></a>
  <a href="https://gitpod.io/#https://github.com/docsifyjs/docsify"><img src="https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod" alt="Gitpod Ready-to-Code"></a>
</p>

<p align="center">Gold Sponsor via <a href="https://opencollective.com/docsify">Open Collective</a></p>

<p align="center">
  <a href="https://opencollective.com/docsify/order/3254">
    <img src="https://opencollective.com/docsify/tiers/gold-sponsor.svg?avatarHeight=48">
  </a>
</p>

Docsify turns one or more Markdown files into a Website, with no build process required.

## Features

- No statically built html files
- Simple and lightweight
- Smart full-text search plugin
- Multiple themes
- Useful plugin API
- Emoji support

## Quick Start

Get going fast by using a static web server or GitHub Pages with this ready-to-use [Docsify Template](https://github.com/docsifyjs/docsify-template), review the [quick start tutorial](https://docsify.js.org/#/quickstart) or jump right into a CodeSandbox example site with the button below.

[![Edit 307qqv236](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/307qqv236)

## Showcase

A large collection of showcase projects are included in [awesome-docsify](https://github.com/docsifyjs/awesome-docsify#showcase).

## Links

- [Documentation](https://docsify.js.org)
- [Docsify CLI (Command Line Interface)](https://github.com/docsifyjs/docsify-cli)
- CDN: [UNPKG](https://unpkg.com/docsify/) | [jsDelivr](https://cdn.jsdelivr.net/npm/docsify/) | [cdnjs](https://cdnjs.com/libraries/docsify)
- [`develop` branch preview](https://docsify-preview.vercel.app/)
- [Awesome docsify](https://github.com/docsifyjs/awesome-docsify)
- [Community chat](https://discord.gg/3NwKFyR)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Backers

Thank you to all our backers! 🙏 [[Become a backer](https://opencollective.com/docsify/contribute)]

<a href="https://opencollective.com/docsify#backers" target="_blank"><img src="https://opencollective.com/docsify/backers.svg?width=890"></a>

## Sponsors

Thank you for supporting this project! ❤️ [[Become a sponsor](https://opencollective.com/docsify/contribute)]

<img src="https://opencollective.com/docsify/sponsors.svg?width=890" />

## Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
<a href="https://github.com/docsifyjs/docsify/graphs/contributors"><img src="https://opencollective.com/docsify/contributors.svg?width=890" /></a>

## License

[MIT](LICENSE)




###解释
docsify 是一个“魔法般”的文档网站生成器，不像 GitBook 那样生成静态 HTML 文件，而是在浏览器中动态读取并渲染 Markdown 文件。要使用它，只需创建 index.html 并部署到 GitHub Pages 即可

项目功能

不生成静态 HTML 文件

简单轻量

内置智能全文搜索插件

提供多种主题

实用的插件 API

支持 Emoji

项目依赖

运行环境需要 Node.js ≥ 20.11.0

核心依赖包含：
- dexie
- medium-zoom
- opencollective-postinstall
- prismjs
- tinydate

使用方法

1. 建议全局安装 docsify-cli：

`npm i docsify-cli -g`

2. 在指定目录初始化文档：

`docsify init ./docs`

3.编辑 ./docs/README.md 等 Markdown 文件。

4.运行本地服务器并在浏览器中预览：

`docsify serve docs`
默认地址为 http://localhost:3000

以上即为该项目的简介、主要功能、依赖项及基本使用方式。

------------------

1. build/
存放各种构建脚本和工具文件：

cover.js：在封面页中替换版本号。

emoji.js：从 GitHub API 获取表情数据并生成对应 Markdown 与 JS 文件。

release.sh：发布脚本，完成版本更新、构建、生成 changelog 等操作。

util.js：提供辅助函数。

2. docs/
项目的文档源文件，包含 Markdown 文档和资源文件，最终用于生成官网或帮助文档。例如：

_navbar.md、_sidebar.md：定义导航栏和侧边栏内容。

多个 Markdown 文件（如 quickstart.md、deploy.md 等）记录使用指南。

3. src/
核心源码目录，包含 Docsify 的实现：

core/：核心逻辑，分为模块化子目录（如 router/、render/、event/ 等），负责路由、渲染、事件处理等功能。

plugins/：内置插件实现，如 search、emoji、zoom-image 等。

themes/：主题样式文件，shared/ 下包含具体的 CSS 片段。

4. test/
自动化测试相关代码：

unit/：单元测试。

integration/：集成测试。

e2e/：端到端测试，使用 Playwright 等工具。

config/：测试环境配置脚本（setup、teardown 等）。

helpers/：测试辅助函数。

5. server.js 与 server.configs.js
用于本地开发或预览文档的开发服务器配置，内部使用 BrowserSync 实现。

6. Dockerfile
定义容器化环境，便于在容器中构建和运行项目。

7. .github/
GitHub 相关设置：

issue 与 PR 模板（ISSUE_TEMPLATE/、PULL_REQUEST_TEMPLATE.md）。

workflows/：GitHub Actions 工作流，如自动测试、更新 emoji 等。

----------------------


Notes笔记

The project is a Node-based documentation generator. Core dependencies and tooling are defined in package.json and other configuration files.该项目是一个基于 Node 的文档生成器。核心依赖项和工具定义在 package.json 和其他配置文件中。

Summary概括

Dependencies依赖项
The primary runtime dependencies include Dexie (IndexedDB wrapper), medium‑zoom, PrismJS and Tinydate:主要运行时依赖项包括 Dexie（IndexedDB 包装器）、medium-zoom、PrismJS 和 Tinydate：

38    "dependencies": {
39      "dexie": "^4.0.11",
40      "medium-zoom": "^1.1.0",
41      "opencollective-postinstall": "^2.0.2",
42      "prismjs": "^1.29.0",
43      "tinydate": "^1.3.0"
44    },

Dexie is used in the search plugin (IndexedDB storage):Dexie 用于搜索插件（IndexedDB 存储）：

6  import Dexie from 'dexie';
10 const db = new Dexie('docsify');
11 db.version(1).stores({
12   search: 'slug, title, body, path, indexKey',
13   expires: 'key, value',
14 });

Medium‑zoom provides zoomable images:中等缩放提供可缩放的图像：

1 import mediumZoom from 'medium-zoom';
...
23   zoom = mediumZoom(elms, { background: 'var(--color-bg)' });

PrismJS is imported for syntax highlighting:导入 PrismJS 进行语法高亮：

import prism from 'prismjs';
Frameworks框架
Docsify can render Vue components inside markdown. The rendering logic checks Vue version and mounts components accordingly:Docsify 可以在 Markdown 中渲染 Vue 组件。渲染逻辑会检查 Vue 版本并相应地挂载组件：

56 const docsifyConfig = this.config;
57 const markdownElm = dom.find('.markdown-section');
58 const vueVersion =
59   'Vue' in window &&
60   window.Vue.version &&
61   Number(window.Vue.version.charAt(0));
...
70 if ('Vue' in window) {
71   const mountedElms = dom
72     .findAll('.markdown-section > *')
73     .filter(elm => isMountedVue(elm));
...
210 if (vueVersion === 2) {
211   vueConfig.el = undefined;
212   new window.Vue(vueConfig).$mount(mountElm);
213 } else if (vueVersion === 3) {
214   const app = window.Vue.createApp(vueConfig);
215   app.component(name, config);
216   app.mount(mountElm);
}

A dedicated guide on Vue support appears in the documentation:文档中提供了有关 Vue 支持的专门指南：

# Vue compatibility
Docsify allows [Vue.js](https://vuejs.org) content to be added directly to your markdown pages.

Build Tools构建工具
The build process uses Rollup and PostCSS. Rollup’s configuration imports several plugins:构建过程使用了 Rollup 和 PostCSS。Rollup 的配置导入了几个插件：

3 import { babel } from '@rollup/plugin-babel';
4 import commonjs from '@rollup/plugin-commonjs';
5 import css from 'rollup-plugin-import-css';
6 import replace from '@rollup/plugin-replace';
7 import resolve from '@rollup/plugin-node-resolve';
8 import terser from '@rollup/plugin-terser';

PostCSS is configured in postcss.config.cjs:PostCSS 在 postcss.config.cjs 中配置：

module.exports = ctx => ({
  map: ctx.options.map,
  plugins: {
    'postcss-import': {},
    'postcss-nesting': {
      edition: '2024-02',
    },
    cssnano: ctx.env === 'production' ? { preset: 'default' } : false,
  },
});

Babel is configured via babel.config.json:Babel 通过 babel.config.json 配置：

{
  "presets": [
    [
      "@babel/preset-env",
      {
        "targets": "defaults"
      }
    ]
  ]
}

Development & Testing Tools开发和测试工具
The development server is BrowserSync:开发服务器是 BrowserSync：

1 import { create } from 'browser-sync';
...
14 bsServer.init(config);

Testing uses Jest and Playwright, as shown in package scripts and dev dependencies:测试使用 Jest 和 Playwright，如包脚本和开发依赖项所示：

65      "eslint-plugin-playwright": "^2.1.0",
70      "jest": "^29.7.0",
71      "jest-environment-jsdom": "^29.7.0",
112      "test:e2e": "playwright test",
116      "test:jest": "cross-env NODE_OPTIONS=--experimental-vm-modules jest",
119      "test": "run-s test:jest test:e2e",

These configurations demonstrate the project’s reliance on Node.js tooling (Rollup, PostCSS, Babel), development utilities (BrowserSync, Cross‑Env, Husky), and testing frameworks (Jest, Playwright) alongside runtime dependencies like Dexie, PrismJS, and Vue integration. The repository provides a comprehensive build and test setup for generating and serving documentation.这些配置展示了该项目对 Node.js 工具（Rollup、PostCSS、Babel）、开发实用程序（BrowserSync、Cross-Env、Husky）和测试框架（Jest、Playwright）以及 Dexie、PrismJS 和 Vue 集成等运行时依赖项的依赖。该代码库提供了全面的构建和测试设置，用于生成和提供文档。
