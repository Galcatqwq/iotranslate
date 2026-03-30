<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./media/iotranslate-glow.png">
  <img alt="TETR.​IO 中文插件 Logo" src="./media/iotranslate-glow-background.png">
</picture>

# [TETR.​IO 中文插件](https://github.com/huanmieSAA/iotranslate)

> 为 [TETR.​IO](https://tetr.io/) 提供中文翻译，支持客户端和网页端使用

[![GitHub issues](https://img.shields.io/github/issues/huanmieSAA/iotranslate?style=flat-square)](https://github.com/huanmieSAA/iotranslate/issues)[![GitHub file size in bytes on a specified ref (branch/commit/tag)](https://img.shields.io/github/size/huanmieSAA/iotranslate/source.js?branch=main&label=script%20size&style=flat-square)](https://github.com/huanmieSAA/iotranslate/blob/main/source.js)[![GitHub Repo stars](https://img.shields.io/github/stars/huanmieSAA/iotranslate?style=flat-square)](https://github.com/huanmieSAA/iotranslate/stargazers)[![GitHub forks](https://img.shields.io/github/forks/huanmieSAA/iotranslate?style=flat-square)](https://github.com/huanmieSAA/iotranslate/network)[![Greasy Fork](https://img.shields.io/greasyfork/dt/466016?color=%23007EC6&label=GreasyFork&style=flat-square)](https://greasyfork.org/zh-CN/scripts/466016)

</div>

> [!NOTE]  
> 本项目已进行现代化重构，现在可以获得更好的使用体验了！
>
> 代码开发将迁移到 [tetrio-chinese](https://github.com/A-Minos/tetrio-chinese) 仓库中进行

<details>
<summary>目录</summary>

- [TETR.​IO 中文插件](#tetrio-中文插件)
  - [功能](#功能)
  - [安装](#安装)
    - [客户端](#客户端)
      - [方法一](#方法一)
      - [方法二](#方法二)
    - [浏览器](#浏览器)
      - [安装脚本管理器](#安装脚本管理器)
      - [安装脚本](#安装脚本)
  - [施工计划](#施工计划)
  - [为此项目贡献](#为此项目贡献)
  - [鸣谢](#鸣谢)
    - [主要开发团队](#主要开发团队)
    - [贡献者墙](#贡献者墙)

</details>

## 功能

- [x] 将 [TETR.​IO](https://tetr.io/) 翻译为中文
  - [x] 支持翻译游戏内画面和页面文本内容
  - [x] 支持动态生成字体文件[^1]
- [x] 支持客户端和网页端使用
- [x] 支持自动更新[^2]

[^1]: 如果是客户端则支持兼容在 TETR.​IO PLUS 中设定的自定义字体，中文文本会使用另一个固定的字体
[^2]: 使用方案为滚动更新，即跟随最新的源代码进行更新

## 安装

### 客户端

#### 方法一

访问 [Github Actions](https://github.com/A-Minos/tetrio-plus-plus/actions/workflows/build.yml) 或者 [nightly.link](https://nightly.link/A-Minos/tetrio-plus-plus/workflows/build/feat%2Fcustomize) 页面[^3]，下载最新的构建产物 `artifact.zip`，解压两次后会得到 `app.asar` 文件

按 `win`+`r` 打开运行窗口后输入下面这串代码，点确定会打开一个文件夹，粘贴替换文件夹里的 `app.asar` 文件后重启客户端，在 TETR.​IO PLUS 的设置窗口内启用翻译功能即可[^4]

```text
%USERPROFILE%/AppData/Local/Programs/tetrio-desktop/resources
```

[^3]: 二选一即可，前者是需要登录后才能下载构建产物，后者则不需要登录也能下载

#### 方法二

加入渣渣的个人 QQ 群 [831797331](https://qm.qq.com/cgi-bin/qm/qr?k=EKq625P5qpas9-m5lVFTDnyCgR1I9yPw&authKey=zqbyY33MW7xTvSEBm+fqVv7lrq3EhV7UuVPrYnQZTal9dQpkD9XM3ViHSu2QnGb3)，在群文件内下载魔改后的 TETR.​IO PLUS 压缩包，解压后会得到 `app.asar` 文件

按 `win`+`r` 打开运行窗口后输入下面这串代码，点确定会打开一个文件夹，粘贴替换文件夹里的 `app.asar` 文件后重启客户端，在 TETR.​IO PLUS 的设置窗口内启用翻译功能即可[^4]

```text
%USERPROFILE%/AppData/Local/Programs/tetrio-desktop/resources
```

[^4]: 如果默认没有显示设置窗口，可以在 TETR.​IO 的主窗口按 `Ctrl`+`T` 来打开设置窗口

> [!WARNING]
> 从 v10 开始，客户端默认禁用 DevTools，且使用 [方法一](#方法一) 与 [方法二](#方法二) 可以拥有更好的体验，所以不再推荐以下两种方法
>
><details>
><summary>已弃用的方法</summary>
>
>#### 方法三
>
>直接在 DevTools 的 Console 中粘贴下面这串代码，回车后会自动加载脚本并启用翻译功能
>
>```JavaScript
>await import('https://greasyfork.org/scripts/466016-tetr-io 中文翻译/code/TETRIO 中文翻译.user.js')
>```
>
>#### 方法四
>
>直接在 DevTools 的 Console 中粘贴下面这串代码，回车后会自动加载脚本并启用翻译功能
>
>```JavaScript
>(() => {
>    const e = document.createElement('script')
>    e.setAttribute('src', 'https://greasyfork.org/scripts/466016-tetr-io 中文翻译/code/TETRIO 中文翻译.user.js')
>    document.head.appendChild(e)
>})()
>```
>
></details>

### 浏览器

#### 安装脚本管理器

| 浏览器 | 脚本管理器 |
| :-----------------------: | :----------------------------------------------------------: |
| 基于 Chromium 内核的浏览器 | [Tampermonkey](http://tampermonkey.net/) / [Violentmonkey](https://violentmonkey.github.io/) |
| 基于 Gecko 内核的浏览器 | [Tampermonkey](http://tampermonkey.net/) / [Violentmonkey](https://violentmonkey.github.io/) |
| Safari 浏览器[^5] | [Userscripts](https://apps.apple.com/us/app/userscripts/id1463298887) / [Macaque](https://apps.apple.com/us/app/macaque/id1595306197) / [Stay](https://apps.apple.com/cn/app/stay/id1591620171) |

[^5]: 由于没有 Apple 设备，无法确定能否在 Safari 浏览器上正常使用此脚本，如果有问题建议更换其他浏览器或使用客户端

#### 安装脚本

> [!IMPORTANT]
> 请在安装脚本管理器后再安装脚本

前往 [TETR.​IO 中文翻译 - Greasy Fork](https://greasyfork.org/zh-CN/scripts/466016) 点击 [安装此脚本](https://greasyfork.org/scripts/466016-tetr-io%E4%B8%AD%E6%96%87%E7%BF%BB%E8%AF%91/code/TETRIO%E4%B8%AD%E6%96%87%E7%BF%BB%E8%AF%91.user.js) 后确认安装即可

## 施工计划

- [x] 已知遗漏的内容的翻译补充
  - [x] 自定义游戏 -> 房间设置
  - [x] TETRA 频道
- [ ] 其他遗漏的翻译补充
- [ ] 术语润色
- [ ] 其他功能补充
  - [ ] 提供聊天翻译功能[^6]

[^6]: ~~真的能实现吗？~~ 考虑到聊天内容的翻译需要使用第三方翻译 API，我们作为免费项目无法提供开箱即用的解决方案，此功能的实现计划暂时搁置

## 为此项目贡献

目前大部分常用内容已经翻译，但仍需润色和补充，欢迎在 Issues 中提出需要翻译的内容或对术语的润色建议，不过更建议直接提交 PR 来完善翻译内容

如果您发现了没有被翻译的地方，且有兴趣对遗漏的翻译内容进行补充，可以前往 [tetrio-chinese](https://github.com/A-Minos/tetrio-chinese/tree/main/src/translates) 提交 PR 哦！

同时希望大家在翻译时可以参考 [俄罗斯方块中文维基](http://tetriswiki.cn) 中的词条对相关术语进行润色

## 鸣谢

### 主要开发团队

- [幻灭](https://github.com/huanmieSAA) - 项目创建者，主要负责项目的开发和翻译
- [渣渣](https://github.com/woshizhazha120) - 提供客户端的魔改集成和现代化重构
- [呵呵](https://github.com/shoucandanghehe) - 为字体生成提供支持
- [MianSoft](https://github.com/MianSoft) - 文档编写、测试和反馈

### 贡献者墙

<a href="https://github.com/huanmieSAA/iotranslate/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=huanmieSAA/iotranslate" />
</a>

使用 [contrib.rocks](https://contrib.rocks) 生成
