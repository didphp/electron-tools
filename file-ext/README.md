## file-ext
`file-ext`, 一个使用在 [electron](https://www.electronjs.org/) 上, 使用nodejs内置库，操作生成与转化文件的方法

#### 版本选择
找到适合对应 `electron` 的版本, 目前只支持 `electron 17.x` 以上的版本, 每个版本只选最高版号

#### 引用须知
调用该文件需要引入包 `bytenode`

#### 方法介绍
`function toJSC()` 使用 bytenode 将 js 文件转换成 jsc 文件, 成功返回文件路径
`function toJSON()` 将对象转化为json文件, 成功返回文件路径

#### 使用方法
先引入包 `bytenode`, 再引用 `file-ext` 的文件, 即可
```
require('bytenode')
const js_file = require('file.jsc')
return js_file.toJSC('./aaa.js')	//return aaa.jsc
return js_file.toJSC('./aaa.js', './abc.jsc')	//return abc.js

var a = {}
a['list'] = [] 
a['list'].push('{"id":1}')
a['list'].push('{"id":2}')
try {
  status = js_file.toJSON('./aaa.json', a)
} catch(err) {
  console.log(err)
}
```
