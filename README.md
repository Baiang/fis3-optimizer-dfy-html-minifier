# fis3-optimizer-dfy-html-minifie

主要针对官方插件fis-optimizer-html-minifie进行修复和升级

- 修复无法压缩vue.js的简写方式
- 修复模板语法压缩失败

## 安装插件

全局安装

```bash
npm install -g fis3-optimizer-dfy-html-minifie
```

或者本地安装到项目所在目录。

```bash
npm install fis3-optimizer-dfy-html-minifie
```

## fis-conf.js文件配置

```javascript
fis..match('**.html', {
        optimizer: fis.plugin('dfy-html-minifier',{
            removeComments: true, //去掉注释
            collapseWhitespace: true,
            conservativeCollapse: true,
            minifyJS: true, //压缩html内的js代码
            minifyCSS: true
        })
    })
```
