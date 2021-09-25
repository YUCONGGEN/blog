#### 1. 安装Git
`Git`是目前世界上最先进的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理。`Git`的作用是将本地的网页文件传到`github`上。
- Git[下载地址](https://git-scm.com/download)
- Git[教程](https://www.liaoxuefeng.com/wiki/896043488029600)
**windows：** 到git官网上下载.exe文件,Download git,安装选项全部默认即可。
#### 2. 安装node.js
`Hexo`是基于`node.js`编写的，所以需要安装一下`node.js`和里面的`npm`工具。
**windows：** 到[Node.js官网](http://nodejs.cn/download/)下载`.exe`文件，安装选项全部默认。安装好之后，按`Win+R`打开cmd命令提示符，输入`node -v`和`npm -v`，若出现版本号，则说明安装成功。
#### 3. 添加npm国内源
使用阿里的国内镜像进行加速下载
```bash
npm config set registry https://registry.npm.taobao.org
```
#### 4. 安装Hexo
前面`git`和`nodejs`安装好后，就可以安装`hexo`了，你可以先创建一个文件夹`MyBlog`，用来存放自己的博客文件，然后`cd`到这个文件夹下（或者在这个文件夹下直接鼠标右键`git bash`打开）。
比如我的博客文件都存放在`C:\MyBlog`目录下。
在该目录下右键点击`Git Bash Here`，打开`git`的控制台窗口，以后我们所有的操作都在`git`控制台进行，就不用`Windows`自带的`cmd`了。
定位到该目录下，输入`npm install -g hexo-cli`安装`Hexo`。可能会有几个报错，不用理会。
```bash
npm install -g hexo-cli
```
安装完后输入`hexo -v`验证是否安装成功。
接下来初始化一下`hexo`,即初始化我们的博客网站。例如我的在`C:\MyBlog`文件夹下的命令行中，输入`hexo init`初始化文件夹
```bash
hexo init
```
新建完成后，指定文件夹`MyBlog`目录下有：
- `node_modules`: 依赖包
- `public`：存放生成的页面
- `scaffolds`：生成文章的一些模板
- `source`：用来存放你的文章
- `themes`：主题**
- `_config.yml`: 博客的配置文件**
到此为止，本地的Hexo基础环境搭建完成了。
#### 5. 安装myblog
下载源代码到本地文件下
```bash
git clone https://github.com/YUCONGGEN/myblog.git
```
将下载好的`myblog`全部复制到`MyBlog`目录下，如果复制过程中出现重复文件，点击替换。
最后使用 `npm i` 或者 `npm install` 安装依赖环境包即可。
>如果安装依赖环境出错，可以参考[这篇文章](https://blog.csdn.net/Seven71111/article/details/103364738)。
最后执行 `hexo clean` 和 `hexo s -g` 启动Hexo本地预览，即可看到效果。
