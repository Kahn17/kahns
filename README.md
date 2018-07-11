#Git使用 个人笔记
- 创建新仓库: 创建新文件夹,打开,然后执行``git init ``

- 下载远程服务器的仓库:``git clone username@host:path/to/repository``

- 工作流: 本地仓库由Git维护的三个部分组成.1是``工作目录``,他持有实际的文件;2是``暂存区(index)``,是一个缓存区域,临时保存你的改动,最后是``head``,指向你最后一次提交的结果

- 添加到暂存区: ``git add <filename>`` 或者``git add *``
- 然后通过commit提交到head ``git commit -m "代码提交信息"
- 现在改动已经提交到``head``,但是没有提交到远程仓库.

- 推送改动: 当你的改动已经提交到本地仓库的``head``中,可以用一下命令提交到远程仓库 ``git push origin master`` ``master``可以替换成你想要推送的任何分支.
- 创建分支: 创建一个分支,并切换到分支上:``git checkout -b new_branch``
- 切换回主分支:``git checkout master``
- 删除新建的分支:``git branch -d new_branch``
- 除非你将分支推动到远程仓库,不然该分支就是仅仅自己可见.
- 上传分支: ``git push origin <branch>``
- 更新合并: 更新你的本地仓库到最新改动,执行:``git pull``
- 在你的工作目录中获取(fetch)并合并(merge)远端的改动.要合并其他分支到你的分支,执行``git merge <branch>
- 分支合并可能会出现冲突.修改文件冲突后,执行以下命令来标记为合并成功``git add <filename> 在合并改动之前,可以使用diff预览差异``   ``git diff my_branch target_branch``
- 可以为你的仓库打标签记录版本信息 ``git tag 1.0.0 1b2e1d63ff `` 1b2e1d63ff是ID的前10位字符 可以使用git log获取
- log: ``git log``查看本地仓库的历史记录
- ``git log --author=bob``查看某人的提交记录
- 替换本地改动:``git checkout -- <filename> 使用head最新的内容替换你工作目录中的文件.已添加到暂存区的改动以及新文件都不会受到影响.
- 假如你想酒气你在本地的所有改动和提交,可以到服务器上获取最新版本,并将你本地分支指向他``git fetch origin `` ``git reset --hard origin/master``


    
    
