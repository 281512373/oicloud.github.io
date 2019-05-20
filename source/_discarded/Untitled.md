title: Untitled
author: John Doe
date: 2019-05-19 21:19:53
tags:
---
---
title: 更新内容
tags: 更新说明,小书匠
grammar_mindmap: true
renderNumberedHeading: true
grammar_code: true
grammar_mathjax: true
---


[toc!?direction=lr]

# 小书匠收费

## 收费与不收费的区别

### 收费

#### 收费项目
1. pdf 定制化导出(pdf封面，水印，加密等)
2. 支持在线更新，优先使用新功能
3. 配置数据同步
4. 自定义数据中心

#### 收费价格

1. 一年 20￥, 两年 40￥。 目前只支持两年，如果付费超过 40￥,只能算做两年的套餐。
 
### 不收费

1. 免费又实用的功能太多了，不知道重点写什么好，自己到 http://soft.xiaoshujiang.com/feature.html 这里看吧.....

## 其他

http://soft.xiaoshujiang.com/price.html

___

# 升级日志

## 注

如果您从较老版本的小书匠升级，内置数据库会有不兼容问题，建议在升级前进行数据导出备份，或者数据库文件备份，防止升级失败。

数据库文件路径

```
Windows: %LOCALAPPDATA%/storywriter/
Mac: ~/Library/Application Support/storywriter/
Linux: ~/.config/storywriter
```

## 7.3.0

开放小书匠官网( http://soft.xiaoshujiang.com )静态博客生成源码 ( https://github.com/suziwen/roadbike )

### 7.3.0 新功能

1. 添加全局资源中心,方便不同文章共用相同的资源。(比如文章部份内容的复制，自动将该部份内的图片资源也复制到对应的新文章上) #1076
2. 添加腾讯云图床 v5 版本
3. 图床图片自动在小书匠内置数据库保存一份，防止图床失效 #1075
4. 导出时，添加`导出全局设置`， 提供导出时样式主题的单独设置功能 #1083


### 7.3.0 修改

1. 升级 pouchdb 到 7.0.0 版本
2. 重构底层资源读取策略，改进文章切换速度，特别是有大量图片资源的文章
3. 修复表格组件图片重复上传问题
4. 绘图组件在打印成 pdf 时，如果空间允许，系统自动适当放大绘图显示效果
5. 导出 docx 时， svg 图片无法正常显示的问题
6. 调整附件语法显示的附件大小格式
7. 限制用户上传的图片，附件大小，最大不能超过 30M
8. 修复客户端重启失败问题
9. 导出 docx 时，标签之间自动添加逗号

## 7.2.2 

### 7.2.2 新功能

1. 添加代码块高亮语言别名 `设置>预览>代码块语言别名`


### 7.2.2 修改

1. 关闭微博图床，标明腾讯图床支持的版本
2. 修复 codechunk 语法不能正确高亮代码块的问题
3. 修复表格行列信息在打印，导出 pdf 时会被显示的问题 #1081

## 7.2.1

### 7.2.1 新功能

1. 数学公式引入 `extpfeil` , `mhchem`, `color` 等插件

``` mathjax!
$$
\color{blue}{
\enclose{box}{
  \enclose{circle}{\bbox[5px]{x+y}} +
  \enclose{circle}{\enclose{circle}{z}} -
  \enclose{updiagonalstrike,downdiagonalstrike}{w}
}
}
$$
```


``` mathjax!
$$
\ce{CO2 + C -> 2 CO}
$$
```

``` mathjax!
$$
\xcancel{x+1}
$$
```

``` mathjax!
$$
\xtwoheadrightarrow[c]{b}
$$
```

``` mathjax!
$$
\bbox[#FD9,border:2px solid purple,10px]{
  \bbox[red]{r} +
  \bbox[green,5px]{\color{yellow}{g}} +
  \bbox[border:2px dashed blue,3px]{b}
}
$$
```

### 7.2.1 修改

1. 数学公式自动换行选项修改为打开状态

``` mathjax!
\[\vec\nabla\times\vec F
  = \left({\partial F_z\over\partial yt} - {\partial F_y\over\partial z}\right){\bf i}
  + \left({\partial F_x\over\partial z} - {\partial F_z\over\partial x}\right){\bf j}
  + \left({\partial F_y\over\partial x} - {\partial F_x\over\partial y}\right){\bf kb}
\]
```

## 7.2.0

### 7.2.0 新功能

1. 实现编辑器全局样式自定义入口
2. 鼠标经过预览区表格时列高亮

## 7.1.4

### 7.1.4 修改

1. 在预览区表格编号显示
2. 在预览区表格鼠标经过显示效果
3. 禁用所有 html 标签的 on 事件， #924

## 7.1.3

### 7.1.3 修改

1. 改进导出 docx 效果
2. 自定义图床路径时，如果有不存在的变量时，引起不能正常保存图片
3. 图床迁移时替换功能改进
4. 图片在表格内统一改为非块级图片
5. 修改导出 docx 和 doc 说明

## 7.1.2

### 7.1.2 修改

1. 图床设置添加更多基础变量 #1062

## 7.1.1

### 7.1.1 修改

1. 代码块预览功能调整
2. 修正代码块语言提示错误的问题
3. 修复 开启写作模式和全屏阅读模式按钮无效 问题 #1058
4. 修复错误的元数据格式造成文章无法保存的问题 #1059

## 7.1.0

### 7.1.0 新功能

1. 添加邀请注册优惠功能，查看[详细说明](http://soft.xiaoshujiang.com/blog/user/invitation)
2. 添加为知远程搜索功能 (会员)
3. 添加为知按标签树结构显示文件功能 (会员)
4. 添加 github 远程搜索功能 (会员)
5. 升级 semantic ui  到 2.4.2 版本
6. 升级底层 nwjs 到 0.36.2 版本


### 7.1.0 修改

1. 对为知笔记里通过 editor.md 编辑的文章图片地址做兼容适配
2. 修正为知笔记标签没有正确同步到为知服务器的 bug
3. 通过拖拽方式添加的图片，自动添加图片标题生成规则调整
4. 解决代理弹出认证窗口的问题


## 7.0.0

### 7.0.0 新功能

1. 升级底层 nwjs 到 0.36.1 版本
2. 添加印象笔记/evernote 远程搜索功能(会员)
3. 添加印象笔记/evernote 按标签树结构显示文件的功能(会员)
4. 实现快速添加 fontawesome 5 图标按钮功能
5. 升级 fontawesome 到 5.7.1 版本

### 7.0.0 修改

1. 修复 svg 格式的图片无法正常打印出 pdf 的问题
2. 代理认证失败时，自动关闭代理功能
3. 修复 fontawesome 图标导出印象笔记，或者发送邮件等情况时，图标消失问题
4. 编辑器主题样式调整
5. emoji 表情默认渲染为 svg 图标
6. 图片为 svg 格式时，保存到印象笔记/evernote 不再做附件转换
7. 修复代码块显示行号时，最后一行自动消失的 bug
