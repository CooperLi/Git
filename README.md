## 日常操作遇到的问题

#### 本地分支上交到GitHub上
1. 进入本地项目文件夹下, 并且初始化仓库
    - git init
2. 添加相关文件到仓库
    - git add .
    - 可以先添加 .gitignore 文件, 方便日后管理
3. 提交本地文件
    - git commit -m "say sth."
4. 到GitHub上面, 添加远程仓库, 拷贝URL地址
5. 回到本地, 添加远程仓库
    - git remote add origin URL地址
    - git remote -v # 查看是否添加成果
6. 推送本地文件到GitHub
    - git push origin master
7. 如果远程比本地新, 如远程初始化中有README.txt而本地没有:
    - git pull origin master
7. 如果出现`fatal: refusing to merge unrelated histories`:
    - 是因为本地和远程两个仓库不同, 无法pull
    - git pull origin master --allow-unrelated-histories
