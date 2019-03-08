# gitlab-markdown-index
> gitlab文档目录自动生成工具

此node模块是一个命令行工具，它遍历所有markdown文件的给定目录（扩展名为`.md`），并将提取所有内容的目录，输出至`stdout`。

## 安装

全局安装markdown-index。

```
npm install -g gitlab-markdown-index
```

## 用法

给gitlab-markdown-index一个要遍历的目录，并将索引的内容输出到`stdout`。

```
markdown-index directory/fulla/markdowns > index.md
```

## git集成

客户端pre-commit钩子

```bash
vim .git/hooks/pre-commit

echo '生成index.md开始...'
gitlab-markdown-index . > index.md
git add index.md
echo '生成index.md结束...'
```

或服务器端post-update钩子
```bash
vim .git/hooks/post-update

gitlab-markdown-index . > index.md
```


## 协议

MIT
