---
layout: code
title: atelier
---
这里存放着技术备忘。

# 写博客

## 流程

目前有两个博客，一个做日记本用，另一个是前者的部分投影。写作和部署过程如下：

- 在私密文件夹写作。创建 post 使用 `rake post[<title>]` 。
- 运行 `$bash copycat.sh` ，将草稿拷贝到转运仓库。 
  ```
  cp ~/github/idelem/_posts/* ./todo/
  ```  
- 部署到 github pages。
  ```
  git add .
  git commit -m "<message>"
  git push
  ```
- 本地测试 `jekyll serve --port 5000` 。

---

## 掉过的坑

heroku 部署是个天坑，首页文章链接全部失效，大概换方法部署了三四次也没有成功。github page 只需上传源文件，就地渲染，缺点是慢。

---

## include

首页显示 .md 文档内容：
{% raw %}
```
{% capture content %}{% include about.md %}{% endcapture %}
{{ content | markdownify }}
```
{% endraw %}
刚才折腾的时候，发现这一段被直接渲染了，显示了 `about.md` 的内容。解决方案是在代码块加入 `raw` 标签。具体就不写了，因为这个标签在此文件中显示不出来……

理论上，本页面应该由首页 include 一个目录下面的文档才比较方便，还可以添加多说 [inline comments](http://yuche.me/mutilple-threads-duoshuo/) 。可惜我实在是太懒了，或许某一天会做吧。

---
## 未来计划
就是展望一下。
- 悬浮在侧边的页面导航
- 更好的 atelier
- 真正的 forum（github API!）
- 修改分割线

---

# forum (BETA)

## CSS

多说 css 已开源。目前停留在外部添加条目阶段。

修改尺寸一定要加 `!important` 。

---

# git
## 删除本地缓存

```
git rm --cache <path>
```
此命令不会删除目录，必须使用 `<path>/*` 。

---

## .gitignore

```
git touch .gitignore
```



