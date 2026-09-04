# 西安智启网络官网

西安智启网络科技有限公司（Xi'an Zhiqi Network Technology Co., Ltd.）的 iOS 研发官网。默认英文版，附完整中文版。

- 计划域名：`www.zhiqiapps.com`（待注册）
- 网站类型：纯静态，无构建步骤
- 英文：`index.html` / `privacy.html` / `terms.html`
- 中文：`zh/index.html` / `zh/privacy.html` / `zh/terms.html`
- 仓库：`git@github-page:songjiang20218/110zigong.git`

## 营业执照信息（已写入页面）

| 项目 | 内容 |
| --- | --- |
| 公司名称 | 西安智启网络科技有限公司 |
| 统一社会信用代码 | 91610131MAKLEN7L8Y |
| 成立日期 | 2026 年 7 月 30 日 |
| 注册地址 | 陕西省西安市高新区高新路 2 号丽华科技大厦 21 层 2101 室 H387 号 |

法定代表人（王苗苗）与注册资本未公开在页面上，如 Apple 审核需要可自行补充。

## 本地预览

```bash
python3 -m http.server 4173
```

然后访问 `http://127.0.0.1:4173/`。

## 上线前必做

1. 注册域名后，DNS 配置：`www` 做 CNAME 指向 `songjiang20218.github.io`，根域 `zhiqiapps.com` 配 A 记录指向 GitHub Pages 的 4 个 IP（`185.199.108-111.153`），由 GitHub 自动跳转到 www。`CNAME` 文件已写为 `www.zhiqiapps.com`，与全站 canonical 一致。
2. 开通 `hello@zhiqiapps.com` 企业邮箱，否则先把站内邮箱换成真实可用地址。
3. 如需办 ICP 备案，在页脚补备案号并链接到 `https://beian.miit.gov.cn/`。
4. 若确定办公电话，可补进联系区，便于 Apple Developer 组织账号核验。

## 换域名的做法

域名如果换成别的，全站替换即可：

```bash
grep -rl "zhiqiapps.com" . --exclude-dir=.git | xargs sed -i '' 's/zhiqiapps\.com/新域名/g'
```

## 素材说明

- `assets/mark.svg`：品牌标记，「启」= 电源/启动符号，橙色渐变。
- `assets/ios-studio-hero.webp`：首屏主视觉，AI 生成的原创图，与 109 站同源；若需要与其它站点明显区分，可另行替换同名文件。
