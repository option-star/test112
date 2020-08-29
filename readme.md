# Git

## 初始化Git仓库/(仓库)
- 这个仓库会存放，git对我们项目代码进行备份的文件
- 在项目目录右键打开 git bash
- 命令: `git init`


## 自报家门
- 就是在git中设置当前使用的用户是谁
- 每一次备份都会把当前备份者信息存储起来
- 命令：
    + 配置用户名 `git config --global user.name "lilaoban"`
    + 配置邮箱  `git config --global user.email "2713554182@qq.com"`

## 把大象放到冰箱要几步
1. 打开冰箱门
    + `git add ./readme.md`
2. 放大象
    + `git commit -m "这是一些说明"`
3. 关上冰箱

## 把代码存储到.git仓库中
- 1.把代码放到仓库的门口(暂存区)
    + `git add ./readme.md` 所指定的文件放到大门口
    + `git add ./`  把所有的修改文件添加到大门口
- 2. 把仓库门口的代码放到里面的房间中去
    + `git commit -m "这是对这次添加的东西的说明"`

## 可以一次性把我们修改的代码放到房间里(版本库)
- `git commit --all -m "一些说明"`
    + --all 表示把所有的修改文件提交到版本库中

## 查看当前的状态
- 可以用来查看当前代码有没有被放到仓库中去
- 命令：`git status`

## git 中的忽略文件
- .gitignore,在这个文件中可以设置要被忽略的文件或者目录。
- 被忽略的文件不会被提交仓库里去。
- 在.gitignore中可以书写要被忽略的文件的路径，以/开头，
    一行写一个路径，这些路径所应对的文件都会被忽略，
    不会被提交到仓库中
    + 写法
        * `/.idea` 会忽略.idea文件
        * `/js` 会忽略js目录里的所有文件
        * `/js/*.js` 会忽略js目录下所有的js文件

## 查看日志
- `git log` 查看历史提交的所有日志
- `git log --oneline` 可以看到简洁版的日志

## 回退到指定的版本
- `git reset --hard Head~0`
    + 表示回退到上一次代码提交时的状态
- `git reset --hard Head~1`
    + 表示回退到上上次代码提交时的状态
- `git reset --hard [版本号]`
    + 可以通过版本号精准的回退到某一次提交的状态
- `git reflof`
    + 可以看到每一次切换版本的记录：可以看到所有提交的版本0


## 分支
- 默认是有一个分支master

### 创建分支
- `git branch dev`
    + 创建了一个dev的分支
    + 在刚创建时dev分支里的东西和master分支里的东西是一样的

### 切换分支
- `git checkout dev`
    + 切换到指定的分支，这里切换到名为dev的分支
    `git branch`可以查看所有分支

### 合并分支
- `git merge dev`
    + 合并分支内容，把当前分支与指定的分支(dev),进行合并
    + 当前分支指的是`git branch`命令输出的前面有*号的分支
- 合并时如果有冲突，需要手动去处理，处理后还需要再提交一次

### GitHub
- 不是git，只是一个网站
- 只不过这个网站提供了允许别人通过git上传代码的功能

### 提交代码到github(当作git服务器来用)
- `git push [地址] master`
    + 会把当前分支的内容上传到远程的master分支上
    + 实例：`git push https://github.com/option-star/test112.git master`