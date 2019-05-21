# PinYinImeDicBuilder
谷歌拼音输入法词库生成工具
**修复生成词库不可用bug**
原版输入法dictlist.cpp->save_list中使用sizeof（size_t），在 DictList::load_list时使用的是uint32，在32位机器上应该是没问题，
在64位机器上所占字节数量不同就会导致生成的词库格式不对，所以代码中已经修改为uint32。
需要的小伙伴可以自己在优化下代码。
