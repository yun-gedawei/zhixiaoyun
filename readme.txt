git 使用命令#把当前目录变成Git可以管理的仓库：
git init把文件添加到仓库git add readme.txt用命令git commit告诉Git，
把文件提交到仓库，-m后面输入的是本次提交的说明git commit -m "wrote a readme file"
git status命令可以让我们时刻掌握仓库当前的状态
git diff顾名思义就是查看difference，git diff readme.txt用HEAD表示当前版本，
上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，
所以写成HEAD~100git reset --hard HEAD^cat readme.txt版本号没必要写全，前几位就可以了，
Git会自动去找。当然也不能只写前一两位，因为Git可能会找到多个版本号，就无法确定是哪一个了。git reset --hard 3628164
你回退到了某个版本，关掉了电脑，第二天早上就后悔了，想恢复到新版本怎么办？找不到新版本的commit id怎么办？在Git中，总是有后悔药可以吃的。
当你用$ git reset --hard HEAD^回退到add distributed版本时，再想恢复到append GPL，就必须找到append GPL的commit id。
Git提供了一个命令git reflog用来记录你的每一次命令：
git diff    #是工作区(work dict)和暂存区(stage)的比较git diff --cached    
#是暂存区(stage)和分支(master)的比较
checkout -- readme.txt   --很重要，没有--，就变成了“切换到另一个分支”的命令，我们在后面的分支管理中会再次遇到git checkout命令
删除命令rm ***文件git rm **文件
