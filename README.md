# gh-demo-site

一个用于验证 GitHub 部署链路的最小静态站点，由 GitHub Actions 自动构建并发布到 GitHub Pages。

## 结构

```
index.html                     页面本体
.github/workflows/deploy.yml   构建 + 发布流水线
```

## 部署流程

1. 推送任意改动到 `main`
2. Actions 自动检出代码 → 打包 → 发布到 Pages
3. 站点地址：在仓库 Settings → Pages 中查看

## 本地预览

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

## 常用命令

```bash
gh workflow run deploy.yml      # 手动触发一次部署
gh run list --limit 5           # 查看最近运行
gh run watch                    # 实时跟踪当前运行
```
