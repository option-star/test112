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
