# Readme for developer
I put all file into `app/` for clean structure     
(GitHub would display root folder `readme.md` higher, instead under a bunch of folder)          
我知道下面中英文混搭比较奇怪，我只是暂时没空整理，麻烦读者先忍着   

## 代码解释
`app/src/` 目录是核心代码，文件不多，解释如下：   

  * `ass.js` 处理 ass 字幕
  * `srt.js` 处理 srt 字幕
  * `config.js`  配置文件
  * `common.js`  常用函数
  * `translate_api.js` 翻译 API
  * `view.js` 页面会载入的 js，监听点击事件等

## Version
* 0.0.1 release at 2018-5-8 (for Windows and macOS)
<!-- * 0.0.2 release at 2019-2-16 -->
<!-- * 0.0.2 release at 2018-9-20 想更新支持多文件翻译，没坚持写完放弃了。没时间了。 -->

## Tech Stack
* Electron
* jQuery
* Vue

## 本地开发
```
cd app/
npm run start
```

## 打包指南 (How to compile new release)
### macOS      
```bash
  npm run dist
```
run this under macOS
output file in `dist/`        

### Windows
```bash
  electron-packager .
```
run this under Windows
because somehow `electron-builder` not working on Windows, so we use `electron-packager`

Note: in `package.json`, some config are for `electron-builder`


## 翻译服务提供商:谷歌 (Translate Service Provider: Google)
Only 3 Translate API: Google/Microsort/Yandex  

## Google doesn't have free quote:
FAQ: https://cloud.google.com/translate/faq?hl=en#pricing
> Is there any free quota?         
> No, the Google Cloud Translation API is only available as a paid service. Please see Pricing for more details.

## 试过 (Tried)
tried `google-translate-api` on Github, it's a node.js module or something, not working.      

## 第三方库 (Third Party Lib)
* eush77/ass-parser    https://github.com/eush77/ass-parser
* eush77/ass-stringify https://github.com/eush77/ass-stringify

### 测试 (Testing)
`test file/` folder have file to test.         
because trasnlation is not the same everytime, it can only test by hand         

### Changelog
0.0.2


#### TODO
1. 批量翻译
2. 编辑翻译
3. 无需翻墙
4. 可选语言转换

#### 0.0.2
* [feature] translate multiple file


