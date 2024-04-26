## 掌握基本 git/github 本地远程版本控制
* 本地仓库是存储在本地计算机上的Git仓库，它包含了项目的完整历史记录和所有版本的文件。本地仓库可以进行版本控制、分支管理和代码提交等操作。
* 远程仓库是指存储在远程服务器上的Git仓库，它用于多人协作开发和备份代码。开发者可以将本地仓库的代码推送到远程仓库，也可以从远程仓库拉取最新的代码。远程仓库通常由代码托管平台（如GitHub、GitLab等）提供。远程仓库可以理解为托管文件的地方，并且可以和本地仓库进行关联，实现本地和远程仓库之间进行高效率更新。
## 掌握基于 gihub pull request 的团队项目开发

 origin; master; branch; branch types; commit; commit message types;
 push; pull; marge
 ### 基于git push
- 在本地开一个文件夹专门存放本项目的文件，方便后面推送。
- 在此文件夹下写自己想写的内容。
- 打开git push
- `git init` 在当前文件夹下创建一个本地仓库,这个仓库的工作区即这个文件夹和子文件。
- `git add *` 将工作区的文件添加到暂存区。
- `git commit -m"修改信息"`
- `git status` 仓库当前状态。
- `git remote add origin url` 关联远程仓库。这里面的origin是后面urld的别名,而url是远程库地址
- `git remote -v` 查看远程库信息。
- `git push -u origin master` 第一次推送master分支所有内容,并把本地的master分支和远程的master分支关联起来。
- `git push origin master`
- `git remote rm origin` 删除关联的(origin)远程仓库 
- `git remote -v` 查看远程库信息
- `git diff` 查看修改
- `git log` 显示从最近到最开始commit日志


## 掌握基于 gihub pull request 的团队项目开发
### origin; master; branch; branch types; commit; commit message types; push; pull; marge Github PR。操作基本可通过 vs code 实现
### fork，源仓库至个人远程仓库
### clone，个人仓库至本地
### ranch，创建 docs branch。有点麻烦，但还是掌握了吧
### commit，docs branch 中修改提交
### branch，切换回 master branch
### upstream，关联源仓库
### pull，更新拉取源仓库至 master branch
### branch，切换回 docs branch
### merge，将 master branch merge 至 docs branch。目的：如果有冲突，要在 branch 解决而不是 master branch
### branch，切换回 master branch，再从 master merge docs branch。此时 master/docs 冲突已经在 docs branch 解决，因此可直接合并。master/docs branch 汇聚为最新提交节点
### push，可直接向源仓库 push pull request。等待源仓库合并代码
### push，可将修改推送至个人远程仓库，但源仓库还未 merge，仅为个人修改内容
### pull，收到源仓库 merge 通知后，更新本地 master branch，并再次 push 至个人远程仓库
### 此时，master branch; origin/master; upstream/master，同步
### del branch，删除完成使命的 docs branch

## HTML

div; span; p; h1; br; hr; table; ul; img;

##Emmet

>; +; ^; (); *; $; lorem;


Emmet是一种强大的HTML和CSS的缩写系统，它可以极大地提高编码速度。

1. **> (子元素)**：使用 `>` 运算符将元素嵌套在彼此内部,最后一个在最后一层。例如，`div>ul>li` 会生成：
    ```
    <div>
      <ul>
        <li></li>
      </ul>
    </div>
    ```
2. **+ (兄弟元素)**：使用 `+` 运算符将元素以相同层级放在同一父元素上。例如，`div+p+bq` 会生成：
    ```
    <div></div>
    <p></p>
    <blockquote></blockquote>
    ```
3. **^ (返回上层)**：使用 `^` 运算符，你可以爬上树的一个层次，并更改上下文。例如，`div+div>p>span+em^bq` 会生成：
    ```
    <div></div>
    <div>
      <p><span></span><em></em></p>
      <blockquote></blockquote>
    </div>
    ```
4. **() (分组)**：`()` 操作符对复杂的子元素进行分组。例如，`div>(header>ul>li*2>a)+footer>p` 会生成：
    ```
    <div>
      <header>
        <ul>
          <li><a href=""></a></li>
          <li><a href=""></a></li>
        </ul>
      </header>
      <footer>
        <p></p>
      </footer>
    </div>
    ```
5. **\* (乘法)**：使用 `*` 操作符，你可以定义应该输出多少次该元素。例如，`ul>li*5` 会生成：
    ```
    <ul>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
    </ul>
    ```
6. **$ (编号)**：操作符可以生成重复元素，而 `$` 可以去元素进行编号。例如，`ul>li.item$*5` 会生成：
    ```
    <ul>
      <li class="item1"></li>
      <li class="item2"></li>
      <li class="item3"></li>
      <li class="item4"></li>
      <li class="item5"></li>
    </ul>
    ```
7. **lorem (文本)**：`lorem` 是一个特殊的关键字，它会生成一段“Lorem ipsum”样本文本。
`lorem`是Emmet中的一个特殊命令，它用于生成“Lorem ipsum”样本文本。"Lorem ipsum"是一种在排版设计领域常用的拉丁文文章，主要用于测试HTML模板在使用真实数据时的外观基本的`lorem`命令会生成一个包含30个词的样本文本。例如，输入`lorem`然后按下Tab键，会生成如下的30个词的样本文本
```
Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae esse at cum aliquid, voluptate mollitia enim totam? Laudantium aliquam exercitationem reprehenderit saepe veniam, alias cumque architecto dignissimos ullam recusandae provident.
```
你还可以在`lorem`后面添加一个数字，来指定生成的词的数量。例如，`lorem10`会生成一个包含10个词的样本文本¹[1]²[2]³[3]⁴[4]⁵[5]。
此外，你还可以在`lorem`后面添加`*`和一个数字，来生成多行样本文本。每行的词的数量由`lorem`后面的数字决定。例如，`lorem10*4`会生成4行样本文本，每行包含10个词。
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
    ```

##markdown