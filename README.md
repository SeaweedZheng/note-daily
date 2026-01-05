# note-daily


# git操作:

## 查看工作区的修改状态（最常用）
git status

## 查看具体修改的内容（显示文件的增删改详情）
git diff


## 方式1：添加指定文件到暂存区（推荐，精准控制提交内容）
git add 文件名1 文件名2

例如：git add README.md src/main.py

## 方式2：添加所有修改的文件到暂存区（适合修改文件较多时）
git add .

## 提交暂存区的内容到本地仓库（必须加-m填写提交说明，否则会打开编辑器）
git commit -m "提交说明：清晰描述这次修改的内容，比如'修复main.py的计算bug'

## （可选）如果提交后发现说明写错，修改最后一次提交的说明
git commit --amend -m "修正后的提交说明"


# #第一步：拉取远端仓库的最新代码（关键，防止推送时冲突）
git pull origin 分支名
例如：git pull origin main（main是默认主分支，也可能是master）

## 第二步：推送本地提交到远端仓库
git push origin 分支名
例如：git push origin main


## 特殊情况：如果是第一次推送本地分支到远端，可能需要加 -u 建立关联：
git push -u origin 分支名