# 可插件化的组件库

目前程序实现了基础功能，但只是基础，有能满足需求但是做的不够好的地方，可能有人希望接上更好的内容，所以单独把这部分抽象出来做成插件。

目前插件逻辑主要有几部分，image_operations里的图像操作逻辑，OCR里的OCR逻辑，tts里的tts逻辑，translators里的翻译逻辑。简单来说个人感想的话，我目前是对OCR效果十分满意，其他三个有待提高。

基本每个类里都实现了一个基类并定义了接口，新插件按照接口把自己具体的逻辑接一下，然后在全局状态管理那里注册就可以用了。