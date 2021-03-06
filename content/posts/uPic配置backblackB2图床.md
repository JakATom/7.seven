---
title: "UPic配置backblackB2图床"
date: 2021-04-03T15:20:22+08:00
draft: false
---

# UPic配置backblackB2图床

## 配置项说明
- 勾选“自定义”
- 服务端URL：登录自己的backblaze账号，选择作为图床的“桶”，拷贝Endpoint的地址。
- 空间名称: 图床的“桶”的名称。
- Access Key: 密钥id。建议在App Keys下专门创建一个新的密钥，专门给uPic使用。
- Secret Key: 密钥。
- 域名: 填写图床自定义域名。
- 保存路径: 文件储存的路径（包括文件夹）。支持 {year} {month} {day} {hour} {minute} {second} {since_second} {since_millisecond} {random} {filename} {.suffix} 等变量。比如：上传的图片为 uPic.jpg，设定为 “uPic/{filename}{.suffix}”，则会保存到 “uPic/uPic.jpg”。我这里不设置文件夹。{filename}{.suffix}

⚠️注意名称中不要有特殊字符，中文字符等。生成的图床链接是经过uri base64处理的。

配置完成后点击“验证”。如果验证成功，会在B2的桶中上传一个测试图片。

![upic配置backblazeB2图床(使用amazons3接口)](https://bedimg.7seven.xyz/upic%E9%85%8D%E7%BD%AEbackblazeB2%E5%9B%BE%E5%BA%8A(%E4%BD%BF%E7%94%A8amazon+s3%E6%8E%A5%E5%8F%A3).jpg)

