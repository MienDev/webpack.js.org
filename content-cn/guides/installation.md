---
title: 安装
sort: 1
contributors:
  - pksjce
  - Mien
---

### 先决条件

假设你已经安装了`node` 和 `npm`。
We assume you have `node` and `npm` already installed.

### 全局安装

``` bash
npm install webpack -g
```

全局安装后，`webpack` 命令全局可用。（译注：在安装时，注意权限。）

但这并不是推荐的最佳实践。 这样有可能会将`webpack`锁定在某一个版本，有可能进而导致使用不同版本的项目出错误。下面的内容会介绍如何进行本地安装。
This locks you down to a specific version of webpack and might fail in projects that use a different version. The next section tells you how to install webpack locally in a project.

### 本地安装

``` bash
npm install webpack --save-dev

npm install webpack@<version> --save-dev
```

在项目中使用`npm`脚本时，`npm`会偿试在模块内搜索本地安装可用的webpack。
If you are using npm scripts in your project, npm will try to look for webpack installation in your local modules for which this installation technique is useful.

```json
"scripts": {
	"start": "webpack --config mywebpack.config.js"
}
```

这是票标准的并且推荐的方式。
This is standard and recommended practice.

本地安装方式，也可以通过`node_modules/.bin/webpack`来直接运行
T> To run the local installation of webpack you can access its bin version as `node_modules/.bin/webpack`


### Bleeding Edge

如果你有热情使用webpack的最新功能（注意-可能会不稳定），也可以直接通过代码库来安装使用。
If you are enthusiastic about using the latest that webpack has to offer (beware - may be unstable), you can install directly from the webpack repository using

``` bash
npm install webpack/webpack#<tagname/branchname>
```
