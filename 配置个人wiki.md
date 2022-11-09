## 配置个人Wiki 
将静态页面托管到托管网站：[GitHub Pages site](https://docs.github.com/cn/pages/getting-started-with-github-pages/creating-a-github-pages-site)
或者[AmazonS3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)
### 1、创建一个github项目
访问不了github项目解决：
1) ping github.com
如果是超时
找一个公共SDN查询工具查询 ttl最小的ip 添加到hosts里
不过很多ip是动态的 一会就变了
2) 或者 访问： chrome://net-internals/#hsts
domain security policy
Delete domain security policies
输入域名 点击delete
Query HSTS/PKP domain
输入域名 点击query
就可以访问了》》》》)

### 2、利用gh-pages分支，将静态页面提交到这个分支，通过 Github用户名.github.io/reposity_name 直接访问静态页面
1) 使用[mkdocs](https://mkdocs.zimoapps.com/#_14)
先安装pyhton pip 再安装mkdocs
命令：
* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
  mkdocs.yml    # The configuration file.
  docs/
  index.md  # The documentation homepage.
  ...       # Other markdown pages, images and other files.
工具可以快速生成纯静态页面，让后将此页面上传到github 的gh-pages分支。
