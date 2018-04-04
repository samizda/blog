---
title: "第一次尝试 spacemacs"
layout: post
---
终于……在重启无数次之后，我可以在 emacs 中打开这个 .md 文档，开始写第一篇 emacs 使用感想了。可以想见，未来的路还很漫长……

## 安装 package 失败的问题

第一次启动 spacemacs，提示大部分 package 安装失败。此后 bash 无法启动。

经过排查，找到了[解决方案](https://github.com/syl20bnr/spacemacs/issues/8984)。原来是 melpa 响应过慢造成的。于是 `SPC-f e d` 打开配置文件 `~/.spacemacs` 修改：`dotspacemacs-elpa-timeout 300`。重启，顺利解决！

##  Pros/Cons
- (+) 在同一个 workspace 处理 git 和文档编辑的感觉非常好（真是低级的要求啊）
- (+) spacemacs 配色审美满分
- (+) 大部分机器自带 emacs，只需下载一份配置就能回到熟悉的工作环境
- (+) `SPC` 作为快捷键十分方便
- (+) 身随意动、如臂使指的流畅体验（当然，前提是熟练……）
- (+) 使用 evil mode，可以同时练习 vim 和 emacs
- (+) 可以预见未来使用的无限潜力
  - 把小说放在同一个 project？
  - 利用 org-mode？
  - 针对不同项目开启不同 layer？
- (-) 学习曲线陡峭！
- (-) 练习时稍有不慎，全盘爆炸
- (-) 快捷键有时有冲突；功能冗杂，新手不知自己在干什么

## 未来要解决
- 搞清 emacs 的一些基本机制，比如：
  - layer
  - mode
  - buffer
- 熟练运用切换窗口的基本按键
- 学习 elisp 并配置开发环境
- 写一篇从需求出发的纯·新手入门
- TBC...
