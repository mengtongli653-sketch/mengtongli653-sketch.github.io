# 随想

有想法就写。GitHub Pages + Jekyll + minima 主题搭建的个人博客。

线上地址:https://mengtongli653-sketch.github.io/

## 在 GitHub 网页端新建一篇文章

1. 打开仓库,进入 `_posts` 目录。
2. 点击 "Add file" → "Create new file"。
3. 文件名必须是 `年-月-日-英文短标题.md`,例如:
   - `2026-08-01-weekend-thoughts.md`
   - 中英双语文章,英文版文件名加 `-en` 后缀,例如
     `2026-08-01-weekend-thoughts-en.md`
4. 文件开头写 front matter(前后各三个短横线),再写正文,格式参考 [模板.md](模板.md):

   ```
   ---
   layout: post
   title: "文章标题"
   date: 2026-08-01 12:00:00 +0800
   lang: zh-CN
   ---

   正文内容……
   ```

   英文版把 `lang` 改成 `en`,标题后缀加上 `(EN)`,例如 `title: "Weekend Thoughts (EN)"`。

5. 直接在网页上写正文,拉到底部点 "Commit changes"。几分钟后线上站点会自动更新。

## 把文章设为草稿(不公开)

在 front matter 里加一行:

```
published: false
```

带这一行的文章不会出现在线上站点的列表和 RSS 里,但文件仍然保存在仓库里。写完准备发布时删掉这一行再提交即可。

## 本地预览

需要先安装 Ruby 和 Bundler。

```bash
bundle install
bundle exec jekyll serve
```

然后浏览器打开 http://localhost:4000 查看效果。改文章后保存,页面会自动重新生成(刷新浏览器即可看到)。

## 目录说明

- `_config.yml` —— 站点配置(标题、语言、主题等)
- `index.md` —— 首页,自动列出所有文章
- `about.md` —— 「关于」页面
- `_posts/` —— 所有文章存放目录
- `模板.md` —— 写新文章时复制这个文件的内容
