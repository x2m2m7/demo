# demo

**沙盒仓库**。里面的内容随时可以丢弃。

## 这个仓库是干什么的

给 Git 的"危险操作"提供一个安全的练习场。真实项目的代码在另一个**私有**仓库里，不在这里。

## 给任何接手此仓库的 AI 会话

- 这是演练/试验仓库，**不是真实项目**，里面的文件没有价值。
- 在这里执行 `git reset --hard`、`git clean -fd`、`git push --force`、删除 `.git` 目录，都是**允许且安全**的。
- 弄坏了不用修，重新克隆即可（见下）。
- 不要把真实数据、密钥、个人信息放进这个仓库——它是公开的。

## 恢复方式

```bash
git clone https://github.com/x2m2m7/demo.git
```

或者本地直接：

```bash
rm -rf .git
git init -b main
git add -A
git commit -m "重置沙盒"
```

## 可以在这里练什么

| 练习 | 目的 |
|---|---|
| `reset --hard` 后用 `reflog` 找回 | 理解 reflog 的缓冲机制 |
| `clean -fd` 删未跟踪文件 | 体会它**没有**挽回机制 |
| 制造合并冲突再解决 | 学会处理冲突而不怕弄坏主线 |
| `push --force` 覆盖远程 | 理解 force push 的真实影响 |

## 历史

- 2026-10-21 建立，用于完成第一次 `git push` 演练。
