---
home: true
heroImage: /images/icons/小C技术栈_扫码_搜索-标准色版.png
actionText: 快速上手 →
actionLink: /#命令
---

# 使用

::: tip
基于本仓库可快速创建你自己的文档网站。
[高亮语法支持列表](https://prismjs.com/#languages-list)
:::
::: tip
编译时自动帮你配置菜单栏和侧边栏，最多三层目录结构。
:::
::: tip
非常多的热心开发者开源主题[theme](/Theme.md)
:::

::: tip
如果觉得使用[VuePress](https://vuepress.vuejs.org)不便，
可使用静态博客写作客户端[gridea](https://github.com/getgridea/gridea)
:::

## 目录结构

```
// 官方标准目录结构 https://vuepress.vuejs.org/zh/guide/directory-structure.html
.
│  .gitignore           git忽略文件
│  package-lock.json    NPM依赖配置文件
│  package.json         项目配置文件
│  README.md            首页md文件
│  yarn.lock            yarn依赖配置文件
│  
├─.github               GitHub配置目录
│  └─workflows          Actions工作流目录
│          deloy.yml    项目的Actions部署配置
│          
├─.vuepress             用于存放VuePress的配置、组件、静态资源等。
│  │  config.js         VuePress配置
│  │  nav.js            除创建的目录之外，自定义添加的导航栏
│  │  push.js           自定义推送脚本
│  │  utils.js          侧边栏和菜单栏自动配置工具
│  │  
│  ├─public             静态资源目录
│  │  │  CNAME          CNAME文件指定域名，防止发布时被清空
│  │  │  manifest.json  5+App（HTML5 Plus移动App）的配置文件
│  │  │  
│  │  ├─files           可直接访问并下载的文件存放目录
│  │  │      
│  │  └─images          存放所有文档的图片目录
│  │      │  
│  │      └─icons       存放图标目录
│  │              
│  └─theme              主题存放目录
│              
├─docs                  编译后的静态资源文件输出目录
│
│
......其他自己的md文档或文件夹，都会打包到docs文件夹下，md文件会编译成html
```
### 也就是你只需要遵从以上目录结构来修改你自己的文档即可使用。
::: warning 注意
配置文件中的注释文字部分，请结合[VuePress官方文档](https://vuepress.vuejs.org/zh/config)一定理解其意义再修改配置！
:::

## 命令

``` bash
# 先克隆本仓库
git clone https://github.com/woytu/UseNotes.git

# 保留上面目录结构列出的文件和文件夹，其他的全部删除

# 使用前请自行安装Node.js环境

# 安装项目的全部依赖
npm install

# 这时创建并书写你自己的md文档

# 开始运行开发环境，然后访问窗口中的路径
npm run dev

# 修改.vuepress/public/CNAME中的域名

# 如果发布到GitHub请见：项目的Actions部署配置
# Actions教程：https://www.bajins.com/IDE/Git.html#actions

```

::: warning 注意
请确保你的 Node.js 版本 >= 8.6。
:::
