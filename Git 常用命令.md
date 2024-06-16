# Git 常用命令

## 配置用户信息

```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

## 克隆远程仓库

```bash
git clone <仓库地址>
```

### 查看仓库状态

```markdown
git status
```

### 添加文件到暂存区

```markdown
git add <文件名>
# 添加所有文件
git add .
```

### 从暂存区移除文件

```markdown
git reset HEAD <文件名>
```

### 提交暂存区的文件

```markdown
git commit -m "提交信息"
```

### 查看暂存区的文件

```markdown
git ls-files
```

### 查看提交历史

```markdown
git log
# 查看单行日志
git log --oneline
# 查看特定文件的提交历史
git log -- <文件名>
```

### 查看文件内容和更改

```md
# 查看文件的更改内容（工作区）
git diff <文件名>
# 查看文件的更改内容（暂存区）
git diff --cached <文件名>

```

### 查看文件在特定提交中的内容

```markdown
git show <提交ID>:<文件路径>
```

### 查看提交中的文件列表

```markdown
git ls-tree --name-only <提交ID>
# 查看最新提交中的文件列表
git ls-tree --name-only HEAD
```

### 查看文件详细更改历史

```markdown
git log -p -- <文件名>

```

回退并保留更改（软重置）

```markdown
git reset --soft  文件hash   保留工作区和暂存区的文件
```

强制回退并丢弃更改（硬重置）

```markdown
git reset --hard  文件hash   不保留工作区和暂存区的文件。相当于一键还原
```

混合回退

```markdown
git reset --mixed 文件hash    保留工作区的文件，不保留暂存区的文件   默认参数写的时候 可以不写 --mixed
```



### 创建和切换分支

```markdown
# 创建新分支
git branch <分支名>
# 切换到新分支
git checkout <分支名>
# 创建并切换到新分支
git checkout -b <分支名>
```

### 合并分支

```mariadb
git merge <分支名>
```

### 删除分支

```markdown
# 删除本地分支
git branch -d <分支名>
# 强制删除本地分支
git branch -D <分支名>

```

### 查看远程仓库

```md
git remote -v
```

### 添加远程仓库

```markdown
git remote add origin <远程仓库地址>
```

### 推送到远程仓库

```markdown
git push -u origin <分支名>
# 推送所有分支
git push --all origin
```

### 拉取远程仓库的更改

```markdown
git pull
```

### 拉取特定分支的更改

```mariadb
git pull origin <分支名>
```

### 删除远程分支

```markdown
git push origin --delete <分支名>
```

### 取消修改

```markdown
# 取消工作区中的修改
git checkout -- <文件名>
# 取消暂存区中的修改
git reset HEAD <文件名>
# 重置到某个特定提交
git reset --hard <提交ID>
```

### 查看文件提交历史

```
git log -- <文件名>·