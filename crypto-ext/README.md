## crypto-ext
`crypto-ext`, 一个使用在 [electron](https://www.electronjs.org/) 上, 基于 `crypto` 包的扩展, 简化了官方繁琐的调用方法

#### 版本选择
找到适合对应 `electron` 的版本, 目前只支持 `electron 17.x` 以上的版本, 每个版本只选最高版号

#### 引用须知
调用该文件需要引入包 `bytenode`

#### 方法介绍
`function setKEY()` 设置密钥, 密钥必须为`32`位字符串  
`function setIV()` 设置向量, 向量必须为`32`位字符串  
`function encrypt()` 加密字符串  
`function dencrypt()` 解密字符串

#### 使用方法
先引入包 `bytenode`, 再引用 `crypto-ext` 的文件, 最后三个步骤：`设置密钥`, `设置向量`, `加密或解密`, 即可
```
require('bytenode')
const crypto = require('crypto.jsc')
crypto.setKEY('00000000000000000000000000000000')
crypto.setIV('00000000000000000000000000000000')
const ciphertext = crypto.encrypt('abc')
console.log(ciphertext)
```

