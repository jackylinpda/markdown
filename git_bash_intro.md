# Github使用经验总结

## 使用Github简单流程
1. 在[Github](https://github.com)上新建远程仓库。
1. 在本地安装[Git Bash](https://github.com/git-for-windows/git/releases/download/v2.17.0.windows.1/Git-2.17.0-64-bit.exe)（在Windows下操作github命令行工具）
1. 在Git Bash下执行以下命令，进行远程仓库克隆：
```bash
git clone https://github.com/jackylinpda/markdown.git
```
1. 在对本地仓库中的文档进行修改后，再用以下命令将本地修改或添加文件同步到远程仓库中：
```bash
git add .
git commit -m '首次添加文件'
git push origin master
```
## 使用Github技巧



1. 编辑.bashrc实现自动切换目录及添加常用命令快捷方式：
```bash
vi ~/.bashrc
cd /e/markdown/
alias ve='source ~/ENV3.6/Scripts/activate'
alias de='deactivate'
```

1. 使用sh脚本实现一键式提交修改到远程库
只需要新建一个upfile.sh文件，内容如下，后续直接调用即可，如：
./upfile.sh 增加github技巧
```bash
#!/bin/bash
git add .
git commit -m "$1"
git push origin master
```

