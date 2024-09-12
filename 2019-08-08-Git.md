# Git

[TOC]

## 配置

### 用户名和邮箱

```bash
git config --global user.name "user"
git config --global user.email "user@email.com"
```

查看配置信息

```bash
git config --list
git config user.name
```

### 更改本地初始化默认分支

Github 曾使用 `master` 作为默认分支，后使用 `main`

但本地初始化默认为 `master` 

#### 全局修改

全局方式修改默认分支

```bash
git config --global init.defaultBranch main
```

#### 初始化时

在初始化时指定默认分支为 `main`

```bash
git init -b main
```

#### 初始化后

修改本地默认分支 `master` 为 `main`

```
git branch -m master main
```



### SSH

#### 1 查看是否已经配置

```bash
ssh -T git@github.com
```

#### 2 配置git的账户和邮箱

```bash
# 配置用户名和邮箱
git config --global user.name "user"
git config --global user.email "user@email.com"
```

#### 3 生成ssh-key

```bash
ssh-keygen -t rsa -C "user@email.com"
```

#### 4 复制公钥（id_rsa.pub）

#### 5 去github的setting中配置

#### 6 验证是否已经配置成功

```bash
ssh -T git@github.com
```



## 操作

### 初始化仓库

```bash
git init 
```

### 设置远程地址

```bash
git remote add origin https://github.com/xxxx/xxxx.git
```

### 拉取远程仓库文件

```bash
git pull origin main
```

### 将本地main设置为远程main分支

```bash
git branch --set-upstream-to=origin/main main
```

### 将所有变更提交到本地仓库

```bash
git add .
```

### 提交注释

```bash
git commit -m '注释'
```

### 将本地仓库推送到远程仓库

```bash
git push
```

