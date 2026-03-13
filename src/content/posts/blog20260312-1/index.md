---
title: Git常用命令
published: 2026-03-12
description: 简单记一下会用到的git命令。
image: "./cover.jpeg"
tags: [Git]
category: 笔记
draft: true
---

## 🖥️ Git Bash 快捷键
Git Bash命令行界面基础操作：
- &zwnj;**复制**&zwnj;：选中文本后，鼠标左键单击即可复制
- &zwnj;**粘贴**&zwnj;：鼠标右键单击粘贴文本
- &zwnj;**清屏**&zwnj;：`Ctrl + L` 快速清理当前窗口
- &zwnj;**中断操作**&zwnj;：`Ctrl + C` 终止当前运行命令


## 🔧 Git 全局设置
```bash
# 配置用户名（显示在提交记录中）
git config --global user.name "Your Name"

# 配置邮箱（关联GitHub等平台账号）
git config --global user.email "your.email@example.com"

# 检查配置
git config --list
```

## 🔗 确认、提交与同步

由**vscode**的GUI操作更方便


## 🌐 互联网仓库协作

### 拉取远程仓库
```bash
# 克隆仓库到本地（自动创建目录）
git clone https://github.com/username/repo.git

# 克隆指定分支
git clone -b branch-name https://github.com/username/repo.git
```
### 分支管理
```bash
# 查看所有分支（本地+远程）
git branch -a

# 创建新分支（不切换）
git branch new-feature

# 创建并切换到新分支
git checkout -b new-feature
# 或（Git 2.23+）
git switch -c new-feature

# 切换到已有分支
git checkout existing-branch
# 或
git switch existing-branch

# 删除本地分支
git branch -d branch-name

# 强制删除未合并分支
git branch -D branch-name

# 删除远程分支
git push origin --delete branch-name
```

## ⏳ 时间线与回滚
```bash
# 查看提交历史（详细版）
git log --graph --oneline --decorate --all

# 回退到指定提交（保留修改）
git reset <commit-hash>

# 回退并丢弃所有修改（危险操作）
git reset --hard <commit-hash>

# 撤销未提交的修改
git checkout -- <file-path>

# 创建撤销提交（推荐方式）
git revert <commit-hash>
```
这部分可以用**vscode**处理，有GUI更方便


## 💻 本地仓库操作


### 初始化仓库
```bash
# 在当前目录初始化Git仓库
git init

# 初始化裸仓库（用于服务器共享）
git init --bare
```
### 分支高级操作
```bash
# 从指定提交创建新分支
git branch new-branch <commit-hash>

# 合并分支（将source分支合并到当前分支）
git merge source-branch

# 解决冲突后标记为已解决
git add <conflicted-file>

# 中止合并
git merge --abort

# 变基操作（将当前分支变基到target分支）
git rebase target-branch

# 交互式变基（修改提交历史）
git rebase -i <commit-hash>
```
这部分可以用**vscode**处理，有GUI更方便

### 分支替换策略
```bash
# 强制推送本地分支到远程（覆盖远程历史）
git push -f origin branch-name
# ⚠️ 慎用！会重写远程历史

# 更安全的替代方案：创建新提交覆盖
git push origin +branch-name

# 同步远程分支到本地（强制更新）
git fetch --all
git reset --hard origin/branch-name
```


## 📌 实用技巧


1. ‌忽略文件‌：创建.gitignore文件排除特定文件
2. ‌差异查看‌：git diff 查看未暂存修改
3. ‌暂存区管理‌：
```bash
git add -p  # 交互式暂存
git stash   # 临时保存修改
git stash pop # 恢复暂存
```
4. ‌远程仓库管理‌：
```bash
git remote add origin <url>  # 添加远程仓库
git remote -v               # 查看远程仓库
```