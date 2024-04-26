掌握基本 git/github 本地远程版本控制

掌握基于 gihub pull request 的团队项目开发

 origin; master; branch; branch types; commit; commit message types;
 push; pull; marge

掌握基于 gihub pull request 的团队项目开发
origin; master; branch; branch types; commit; commit message types; push; pull; marge Github PR。操作基本可通过 vs code 实现
fork，源仓库至个人远程仓库
clone，个人仓库至本地
branch，创建 docs branch。有点麻烦，但还是掌握了吧
commit，docs branch 中修改提交
branch，切换回 master branch
upstream，关联源仓库
pull，更新拉取源仓库至 master branch
branch，切换回 docs branch
merge，将 master branch merge 至 docs branch。目的：如果有冲突，要在 branch 解决而不是 master branch
branch，切换回 master branch，再从 master merge docs branch。此时 master/docs 冲突已经在 docs branch 解决，因此可直接合并。master/docs branch 汇聚为最新提交节点
push，可直接向源仓库 push pull request。等待源仓库合并代码
push，可将修改推送至个人远程仓库，但源仓库还未 merge，仅为个人修改内容
pull，收到源仓库 merge 通知后，更新本地 master branch，并再次 push 至个人远程仓库
此时，master branch; origin/master; upstream/master，同步
del branch，删除完成使命的 docs branch

HTML

div; span; p; h1; br; hr; table; ul; img;

Emmet

>; +; ^; (); *; $; lorem;
markdown