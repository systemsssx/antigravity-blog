# Antigravity 两份排查记录：登录 illegal location 与 400 报错

> 中文技术博客 · 单文件 HTML · 零外部依赖 · 支持亮/暗主题

在线预览（GitHub Pages）：<https://systemsssx.github.io/antigravity-blog/>

## 内容

### 合并版首页 · 两篇合二为一

[index.html](index.html) —— 《Antigravity 两份排查记录：登录 illegal location 与 400 报错》

- **第一部分**：登录报 illegal location，无法登录
  - TL;DR（结论先行） / 问题现象 / 三道关卡的判定模型 / 实际操作步骤
- **第二部分**：代理开着，Antigravity 却报 400
  - 引言与复现日志 / 拆解漏掉的流量 / 为什么系统代理救不了它
  - 解法一：全局 TUN 接管 / 怎么确认 TUN 生效 / 解法二：修好回环
  - 排查流程图 / 边界与风险 / 结语与一页速查表

### 单独版本（原稿）

- [第一部分单独版：Antigravity 中国区账号复活实录 —— 从 hasValidAuth 补丁到账号验证](posts/antigravity-region-bypass.html)
- [第二部分单独版：代理开着却报 400 —— Antigravity 漏网流量与 TUN 回环排查实录](posts/antigravity-400-tun.html)

> 单独版可脱离首页独立阅读；合并版对内容做了统一排版与编号，是推荐入口。

## 目录结构

```text
.
├── index.html                                  # 合并版博客（仓库首页 / Pages 首页）
├── posts/
│   ├── antigravity-region-bypass.html          # 第一部分单独版
│   └── antigravity-400-tun.html                # 第二部分单独版
├── README.md
└── .nojekyll                                   # 跳过 Jekyll，直接静态托管
```

## 技术说明

- **单文件**：全部 CSS / JavaScript 内联，不引用任何外部字体、图片或 CDN，断网也能正常阅读。
- **主题**：页面右上角可切换亮色 / 暗色主题，选择会记录在本地浏览器中。
- **编码**：UTF-8（无 BOM），适配桌面与移动端。
- **部署**：GitHub Pages 直接托管仓库根目录，`.nojekyll` 跳过 Jekyll 处理。

## 本地查看

```powershell
start .\index.html
```

## 声明

本文为个人技术研究与排查记录，所有操作均在自己的设备与账号环境下进行。文中涉及第三方软件的内容仅供学习参考，请遵守相应软件的服务条款与所在地法律法规。
