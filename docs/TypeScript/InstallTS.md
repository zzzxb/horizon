# Install TS

[TS - OS](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)

## [<-back](README.md)

## MacOS

* 下载 NodeJS

[Node JS - OS](https://nodejs.org/zh-cn/)

推荐选了 LTS 版本， 下载到 node-vxx.xx.x.pkg 文件后打开安装就行了

`node -v` 查看 node 版本, node 用来解释运行代码的

`npm -v` 查看 npm 版本, npm 用来下载远程仓库中发布的各种工具包

> 因为国外镜像仓库下载东西比较慢，下边是改为淘宝公开的仓库

`npm config set registry https://registry.npm.taobao.org`

或者

```bash
> npm config edit
> registry=https://registry.npm.taobao.org/
```

* 通过 npm 安装 TS

```bash
npm install -g typescript
```

`tsc -v` 查看版本

`tsc -h` 查看操作指令

`tsc fileName.ts` 解释 ts 文件

## Hello World

```typescript
let msg = "Welcome to TS!"

function welcome(name : string) {
    return "Hello " + name + ", " + msg;
}

console.info(welcome("Zzzxb"));
// document.body.textContent = welcome("Zzzxb");
```

通过 `tsc fileName.ts` 翻译后会生成一个 *fileName.js* 的文件,如下:

```javascript
var msg = "Welcome to TS!";
function welcome(name) {
    return "Hello " + name + ", " + msg;
}
console.info(welcome("Zzzxb"));
// document.body.textContent = welcome("Zzzxb");
```

可以看出 ts 中指定的强类型，到 js 中变成了弱类型

执行 `node FileName.js`, 进行解释js代码

> 输出: Hello Zzzxb, Welcome to TS!

* 在 HTML 页面上输出

* 打开上边代码中的注释, 并创建下边 html 文件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script src="hello-world.js"></script>
</body>
</html
```

打开html文件后页面也会出现同样的信息