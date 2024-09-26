# pyTencentTranslator

## 介绍

这个翻译API使用的是腾讯云的翻译服务, 每月它有五百万字符的免费使用量，针对个人项目，一般够用了。
你可以在这里免费申请 [腾讯云翻译](https://curl.qcloud.com/4iLMkfzX)  
然后你会得到一个 secret id and secret key, 在下面的使用中会用到  

如果你需要云服务器，这里有一款很高性价比的，高性能的腾讯云服务器，当前优惠价 79元一年，不保证一直有效。 链接地址： [腾讯特惠云服务器](https://curl.qcloud.com/xQJBnWxe)


## 安装依赖库
安装 腾讯云 sdk
```
pip install tencentcloud-sdk-python

```
## 使用

```
import tencentCloudTranslator as tcTranslator
```
定义 你的 secret id 和 secret key
```
(secretId,secretKey)=(your_secrect_id,your_secret_key)
```
使用 secret id and secret key 获取 translator 实例
```
tc_translator = tcTranslator.TencentCloudTranslator(secretId,secretKey)
```
使用 方法 cloud_translate(original_text,original_lang,target_lang)  来进行翻译
- 参数 original_text：待翻译的文本
- 参数 original_lang: 待翻译文本的语言的代码，
- 参数 target_lang: 目标翻译文本的语言代码
```
en_text = tc_translator.cloud_translate("你好世界","zh","en")
zh_tw_text = tc_translator.cloud_translate("你好世界","zh","zh-TW")
ja_text = tc_translator.cloud_translate("你好世界","zh","ja")
ko_text = tc_translator.cloud_translate("你好世界","zh","ko")
```
