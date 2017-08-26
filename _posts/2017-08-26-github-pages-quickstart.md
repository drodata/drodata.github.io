---
layout: default
title: 快速上手 GitHub Pages
---

按照[官方的快速上手教程][github-pages]操作。操作后仓库的目录结构如下：

```
├── index.html
└── README.md
```

在仓库的设置页面：

![设置主题](/img/change-github-pages-theme.png)

点击 **Change theme**, 选择一个主题并 **Select theme**, 之后会发现仓库自动生成了一个 commit, 在根目录下新增了文件 `_config.yml`, 此时目录结构为：

```
├── _config.yml
├── index.html
└── README.md
```

现在再在目录下新建目录 `_posts`, .md 文章都存放在该目录下。新建第一篇文章，使得目录变成：

```
├── _config.yml
├── index.html
├── _posts
│   ├── 2017-08-25-hello-world.md
└── README.md
```

文章内容如下：

```
---
layout: default
title: Hello World
---

这里开始书写正文。支持 GFM.
```

下面修改最开始创建的 index.html 内容如下：

```
---
layout: default
title: 我的Blog
---

<ul>
    {% for post in site.posts %}
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>
```

全部结束后 commit.

## 小结

比 GitBook 好用。

[jekyll-doc-on-github]: https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/
[github-pages]: https://pages.github.com/
