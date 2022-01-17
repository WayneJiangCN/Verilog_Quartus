### **GIT通用操作**

#### · 添加密钥

> 打开git bash

```bash
cd ~/.ssh/
git config user.email goodMorning@mofan.com
git config user.name --global mofan
    ssh-keygen -t rsa -C "goodMorning@mofan.com"
    
    Your identification has been saved in ls196071.
Your public key has been saved in ls196071..pub
The key fingerprint is:
SHA256:Jb55z9ojauIdlhF/SWS5ndqkRpbHOIkZPXlJ+RtX6ME 1448119477@qq.com
ssh  -T git@github.com
```

> 之后一路回车，按照提示的路径找到public key文件，复制内容到GitHub或者Gitee的SSH密钥里

[![IR5Voj.png](https://z3.ax1x.com/2021/11/16/IR5Voj.png)](https://imgtu.com/i/IR5Voj)

#### · 初始化仓库

> 首先在GitHub或者Gitee上新建一个Repository。在本地，安装完git后，建立一个仓库文件夹，右键点击进入git bash here,敲入以下指令即完成一个项目的克隆与部署。

```bash
git init
```

#### · Git初始配置

```bash
git config --global user.name "Raymond_Meng"
git config --global user.email "2391530014@qq.com"
```

#### · 关联远程仓库

```bash
git remote add origin <项目地址>
```

> 这里的项目地址就是你的Github或者Gitee项目主页的SSH或者HTTPS地址

[![IR4aqg.png](https://z3.ax1x.com/2021/11/16/IR4aqg.png)](https://imgtu.com/i/IR4aqg)

#### · 更新远程仓库到本地

```bash
git pull origin master(以及任何你想要更新的branches)
```

> 如果新建的远程仓库没有用README.md初始化可以不需要，本质其实就是如果需要推送更改到远程仓库，需要先将本地仓库与远程仓库更新合并。

#### · 提交项目

> 保存到缓存区

``` bash
git add . #如果只需要提交某一部分，可以git add 被拖入的项目名
```

> 描述本次提交的内容

```bash
git commit -m "要描述的内容"
```

> 推送到远端仓库上

```bash
git push origin master(以及任何你想要推送的branches)
```

#### · 克隆

```bash
git clone <项目地址>
```

> 这个主要是用来克隆整个代码仓库到本地，在本地进行开发

#### · 仓库后期推送的注意事项

> 1. 一定要有描述内容
>
> 2. 非必须不要强制提交
>
> 3. 更新仓库前确定本地修改的已经放入缓存区，防止被覆盖
>
> 4. 如果对Github git clone太慢，需要手动开启代理
>
>    ```bash
>    git config --global http.https://github.com.proxy http://127.0.0.1:19180 #端口号因人而异
>    git config --global https.https://github.com.proxy http://127.0.0.1:19180
>    ```

#### · 多人协作

>  settings -> manage access 选择成员成为collaborators
>
> 然后在接下来的协作中很重要的一点，就是先更新本地仓库，再push，不然是推不上去的。更新的时候，还是那句话，先放入缓存区，再commit，之后再pull，不然自己本地所有的修改都将被覆盖。

图床指令：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

​                                                                                                                                                                                                                ***by mc***

