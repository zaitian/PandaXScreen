# screen（组态大屏演示页）

静态演示目录，**不是完整的前端工程**（无 package.json，无构建脚本）。

## 内容

| 文件 | 说明 |
|---|---|
| `index.html` | 极简页面，内嵌 iframe 指向远程演示地址（`http://101.35.247.125:7790/`），仅作占位 |
| `连线.html` / `连线2.html` | SVG 折线锚点拖拽的交互 demo（组态连线效果试验） |
| `image/` | README 用截图与动图 |

## 运行

任意静态服务器即可（端口按需，项目里惯用 7790）：

```powershell
python -m http.server 7790 --bind 0.0.0.0
# 或 npx http-server -p 7790
```

访问 `http://127.0.0.1:7790/`。

## 注意

- PandaX 里的「组态大屏」是**商业版功能**，本目录不包含真实实现；前端 `PandaUi` 通过 `VITE_SCREEN_URL`（默认 `http://127.0.0.1:7790`）跳转过来
- 改动只涉及静态 HTML/CSS/JS，不要在这里引入 npm 依赖或构建流程
- `index.html` 的 iframe 指向外部服务器，离线环境下会显示空白，属预期行为
