# pyTencentTranslator
### [中文文档请看这里](README_ZH.md)
## introduction

This cloud translator use tencent cloud translation service,which is free in limit 5million characters allowance each month.
But, don't worry, it's enough for personal project.
you can sign up a free account at [Tencent Cloud Translation](https://curl.qcloud.com/4iLMkfzX)  
then you can get the secret id and secret key, which you need to use in the following API

if you need an affordable price vps, you can get a tencent cloud premium vps for 79 yuan for one year at [premium tencent cloud vps](https://curl.qcloud.com/xQJBnWxe)


## requirement
install tencent cloud sdk
```
pip install tencentcloud-sdk-python

```
## usage

```
import tencentCloudTranslator as tcTranslator
```
define your secret id and secret key
```
(secretId,secretKey)=(your_secrect_id,your_secret_key)
```
use secret id and secret key to get the translator instance
```
tc_translator = tcTranslator.TencentCloudTranslator(secretId,secretKey)
```
use function cloud_translate(original_text,original_lang,target_lang)  to translate
- original_text: the text need to be translated
- original_lang: the lang code of the original text
- target_lang: the lang code of the text which will be translated to
```
zh_text = tc_translator.cloud_translate("hello world","en","zh")
zh_tw_text = tc_translator.cloud_translate("hello world","en","zh-TW")
ja_text = tc_translator.cloud_translate("hello world","en","ja")
ko_text = tc_translator.cloud_translate("hello world","en","ko")
```
