---
published: true
title: Down to a Sunless Merge
---

> Through ~~caverns~~ commits measureless to man. 

> Down to a sunless ~~sea~~ merge. 

深陷于一个地狱般的 merge。大概就是落后 master 70+ commits 的同时，我自己又有 ~9 commits。这里说说从地狱里爬出来的艰险路途上积累的一点人生经验。
- 如果你的 commit 只涉及到一个文件夹，恭喜你，you can `git checkout origin/master -- <filename>` the rest of the repo! 
- 不小心用 master 的版本覆盖了自己做的改动，怎么办？赶紧 `git checkout origin/<your-branch> -- <filename>`。
- 对于你改动过的文件，试着在 master branch 逐个 blame。（是的我知道这个办法很蠢……但目前也没有想出更好的替代方案）
