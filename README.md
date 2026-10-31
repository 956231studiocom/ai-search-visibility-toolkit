# AI Search Visibility Toolkit — 免费模板集

让 LLM（ChatGPT / Perplexity / Gemini / Claude）能正确读到并引用你的站点。
本仓库是可直接复制的**模板 + 清单**，无依赖、无 SDK。

> 由 [https://956231studio.com](https://956231studio.com) 维护。在线免费体检：https://956231studio.com/geo-landing/

## 1. `llms.txt` 模板

见 [`llms.txt.example`](./llms.txt.example)。要点：
- 用 Markdown 标题结构，`H1` = 你的实体名
- 每个链接一行，附一句「这页讲什么、权威在哪」
- 只收**稳定、公开、无登录墙**的 URL

## 2. AI 爬虫 `robots.txt` 片段

见 [`robots.ai-snippet.txt`](./robots.ai-snippet.txt)。
放行不等于被收录，但**误禁一定不被收录** —— 最常见的事故是 CDN/WAF 顺手拦了 AI 爬虫 UA。

## 3. JSON-LD：Organization + FAQPage

见 [`jsonld-organization.json`](./jsonld-organization.json) 与 [`jsonld-faq.json`](./jsonld-faq.json)。
实体消歧的关键：`sameAs` 指向你真实存在的外部档案（GitHub / 社交）。

## 4. 可引用答案块写法

AI 摘录的是**判断句 + 数字 + 边界条件**，不是形容词。

- ✗ 「我们提供行业领先的解决方案」
- ✓ 「一次体检覆盖 12 项可自动检测的 AI 可见性信号，输出 3 份交付物：基线快照 / 修复清单 / 30 天复测。」

## 5. 上线前自检清单

- [ ] `robots.txt` 未拦截 GPTBot / PerplexityBot / ClaudeBot / Google-Extended
- [ ] `/llms.txt` 返回 200 且为 `text/plain`
- [ ] 首屏正文（非 JS 渲染后）含品牌实体全称
- [ ] 每页唯一 `canonical`
- [ ] 至少一个 JSON-LD 块且 `@type` 正确
- [ ] `sitemap.xml` 已提交 + IndexNow 已推
- [ ] 联系方式全站口径一致

---
*免费非商用可随意取用；转载保留本仓库链接即可。联系：956231@qq.com*
