# blog-source


# hexo

下面是如何操作的具体步骤：
1. 新建两个仓库，一个用来存放Hexo的源文件（例如命名为 blog-source），另一个用来存放生成的静态文件，用于托管你的博客 <username>.github.io。
   在你的电脑上通过 git clone 将这两个仓库都拉取下来。例如：

git clone https://github.com/[MrKrabXie](https://github.com/MrKrabXie/MrKrabXie.github.io)/blog-source.git
git clone  https://github.com/MrKrabXie/MrKrabXie.github.io

1. 这样你就在本地分别有了两个仓库的文件。
   在 blog-source 仓库中初始化并安装你的Hexo博客：

cd blog-source
hexo init .
npm install

1. 然后你可以在这里写博文，修改Hexo的配置，添加主题等。

hexo new

1. 当你添加或修改了博客内容后，你需要生成静态文件并且发布

hexo generate

1. 然后将这些生成的内容复制或者移动到 <username>.github.io 的仓库

cp -r ./public/* ../<username>.github.io

1. 然后到 <username>.github.io 的仓库，提交并且推送这些改动：

cd ../<username>.github.io
git add .
git commit -m "hexo updated"
git push origin master

就完成了！你的 <username>.github.io 仓库就会更新，你的博客就会展示出最新的内容。同时你的 blog-source 仓库保留了你的Hexo源文件，以备后续更新博文用。


hexo clean //清除缓存文件 (db.json) 和已生成的静态文件(public)
hexo generate //生成静态文件到public文件夹，简写为 hexo g
hexo server //开始服务器，简写为hexo s。默认情况下，此命令同时执行hexo generate