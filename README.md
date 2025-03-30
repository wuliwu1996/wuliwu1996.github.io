# Hexo 搭建个人博客的命令

## 1. `hexo new [layout] <title>`
新建一篇文章。

- 如果没有设置 `layout`，默认使用 `_config.yml` 中的 `default_layout` 参数。
- 使用布局 `draft` 可以创建草稿。
- 如果标题包含空格，请用引号括起来。

**示例**：
```bash
hexo new post "My First Post"
hexo new draft "Draft Post"
```

## 2. `hexo generate`
生成静态文件。

| 选项            | 描述                                                                 |
|-----------------|----------------------------------------------------------------------|
| `-d, --deploy`  | 在生成完成后自动部署。                                              |
| `-w, --watch`   | 监视文件变动，文件修改后自动重新生成。                              |
| `-b, --bail`    | 生成过程中如果发生任何未处理的异常则抛出异常。                      |
| `-f, --force`   | 强制重新生成静态文件。                                              |
| `-c, --concurrency` | 设置同时生成的文件的最大数量，默认无限制。                        |

**示例**：
```bash
hexo generate
hexo generate --deploy
hexo generate --watch
```

## 3. `hexo server`
启动本地服务器，默认访问地址为 `http://localhost:4000/`。

| 选项            | 描述                                                                 |
|-----------------|----------------------------------------------------------------------|
| `-p, --port`    | 重设服务器端口。                                                    |
| `-s, --static`  | 只使用静态文件。                                                    |
| `-l, --log`     | 启用日志，覆盖日志格式。                                            |

**示例**：
```bash
hexo server
hexo server -p 4001
hexo server --static
```

## 4. `hexo deploy`
部署你的网站。

| 选项            | 描述                                                                 |
|-----------------|----------------------------------------------------------------------|
| `-g, --generate` | 在部署前生成静态文件。                                              |

**示例**：
```bash
hexo deploy
hexo deploy --generate
```

## 5. `hexo clean`
清除缓存文件（如 `db.json`）和已生成的静态文件（`public` 文件夹）。

**示例**：
```bash
hexo clean
```

## 6. `hexo list <type>`
列出所有路由。

**示例**：
```bash
hexo list routes
```
# GIT无法推送问题
```bash
优先：git config --global http.sslVerify "false"
或者：
git config --global --unset http.proxy
git config --global --unset https.proxy
```
再不行，就把代理关掉（【设置】- 【网络和internet】-【代理】，关闭代理）