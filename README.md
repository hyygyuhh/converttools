# Studio One守护者 官网

专业音频知识产权保护方案官方网站。

## 功能特性

- .song 工程文件加密（.song 转 .song.ylcev）
- Studio One 全版本软件封装
- VST 插件加密保护
- 工程文件远程锁 / 远程删除 / 强制下线
- 机器码绑定设备授权
- 云端管理后台

## 技术栈

- 纯 HTML / CSS / JavaScript（无构建步骤）
- Apple 液态玻璃 UI 设计
- 响应式布局
- SEO 优化（Open Graph、JSON-LD 结构化数据）

## 部署方式

### GitHub Pages（自定义域名）

1. 将本仓库推送到 GitHub
2. 进入仓库 Settings → Pages → Source: GitHub Actions
3. 自定义域名 `converttools.site` 已通过 CNAME 文件配置
4. 在域名 DNS 服务商添加以下记录：
   - A 记录：`@` → `185.199.108.153`
   - A 记录：`@` → `185.199.109.153`
   - A 记录：`@` → `185.199.110.153`
   - A 记录：`@` → `185.199.111.153`
   - CNAME 记录：`www` → `<your-username>.github.io`
5. 推送到 `main` 分支自动触发部署

### 本地预览

```bash
cd audio-guard-website
python3 -m http.server 8000
# 打开浏览器访问 http://localhost:8000
```

## 文件结构

```
├── index.html          # 主页面
├── favicon.svg         # 网站图标
├── og-image.jpg        # 社交分享图
├── wechat-qr.png       # 微信二维码
├── robots.txt          # 搜索引擎爬虫规则
├── sitemap.xml         # 站点地图
├── CNAME               # GitHub Pages 自定义域名
├── .nojekyll           # 禁用 Jekyll
├── .gitignore
└── .github/workflows/deploy.yml  # 自动部署工作流
```

## 上线前检查清单

- [ ] 替换 ICP 备案号占位文本
- [ ] 配置 DNS 解析指向 GitHub Pages
- [ ] 在 GitHub Pages 设置中开启 Enforce HTTPS
- [ ] 提交 sitemap.xml 到 Google Search Console / 百度站长平台
- [ ] 替换统计数字为实际数据（如有需要）
