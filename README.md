# LLM API Pricing · 主流大模型 API 价格表

> 13 家厂商、33 个主流模型的 API 官方标价（美元 / 每百万 token：输入、缓存命中、输出），每行都附官方来源。想按自己的用量算月费？用 **[og.cc.cd 大模型成本计算器](https://og.cc.cd/llm-cost-calculator/)**。
>
> Official API list prices for 33 models from 13 providers (USD per 1M tokens: input / cached input / output), each with its source. Estimate your own bill with the [LLM cost calculator on og.cc.cd](https://og.cc.cd/llm-cost-calculator/).

**价格核实日期 / Prices checked：2026-10-21**（数据与 og.cc.cd 的 Token 计数器、成本计算器同源）

## 目录

- [价格总表](#价格总表)
- [同一负载的月费排行](#同一负载的月费排行)
- [怎么读这张表](#怎么读这张表)
- [相关工具与指南](#相关工具与指南)
- [English](#english)
- [官方来源](#官方来源)

## 价格总表

单位：美元 / 每百万 token（标准档、非批量）。有长上下文分档的，表中为最低档，备注写明高档价格。“—”表示厂商未公布缓存价。

| 厂商 | 模型 | 输入 | 缓存命中 | 输出 | 备注 | 来源 |
|---|---|---|---|---|---|---|
| OpenAI | `gpt-6-astra` | $10 | $1 | $50 | 提示 >272K token：输入 2 倍、输出 1.5 倍 | [官方](https://developers.openai.com/api/docs/pricing) |
| OpenAI | `gpt-6.1-sol` | $2 | $0.10 | $10 | 提示 >272K token：输入 2 倍、输出 1.5 倍 | [官方](https://developers.openai.com/api/docs/pricing) |
| OpenAI | `gpt-6-luna` | $0.10 | $0.01 | $0.50 | 提示 >272K token：输入 2 倍、输出 1.5 倍 | [官方](https://developers.openai.com/api/docs/pricing) |
| OpenAI | `gpt-5.3-codex` | $1.75 | $0.175 | $14 |  | [官方](https://developers.openai.com/api/docs/pricing) |
| Anthropic | `Claude Fable 5.1` | $10 | $0.25 | $50 |  | [官方](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Anthropic | `Claude Opus 5.5` | $4 | $0.20 | $20 |  | [官方](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Anthropic | `Claude Sonnet 5.5` | $2 | $0.10 | $10 |  | [官方](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Anthropic | `Claude Haiku 5.5` | $0.10 | $0.01 | $0.50 | 提示 >100K：$0.50 / $2.50 | [官方](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Google | `gemini-4-argon` | $2 | $0.10 | $10 | 至 2026-11-30；2026-12-01 起 $4 / $20 | [官方](https://ai.google.dev/gemini-api/docs/pricing) |
| Google | `gemini-3.8-flash` | $0.75 | $0.075 | $3.75 | 至 2026-12-31；2027-01-01 起 $1.50 / $7.50 | [官方](https://ai.google.dev/gemini-api/docs/pricing) |
| Google | `gemini-3.5-flash-lite` | $0.30 | $0.03 | $2.50 |  | [官方](https://ai.google.dev/gemini-api/docs/pricing) |
| DeepSeek | `deepseek-v4-pro` | $1.32 | $0.044 | $3.96 | 高峰价（未命中缓存）；闲时半价 | [官方](https://api-docs.deepseek.com/quick_start/pricing) |
| DeepSeek | `deepseek-flash` | $0.30 | $0.006 | $1.20 | 高峰价（未命中缓存）；闲时半价 | [官方](https://api-docs.deepseek.com/quick_start/pricing) |
| 阿里通义千问 | `qwen3.8-max` | $2 | — | $6 | 百炼国际站（新加坡） | [官方](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 阿里通义千问 | `qwen3.7-plus` | $0.40 | $0.08 | $1.60 | 国际站标价（页面显示限时 8 折）；>256K：$1.2 / $4.8 | [官方](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 阿里通义千问 | `qwen3.8-flash` | $0.15 | — | $0.47 | 百炼国际站（新加坡） | [官方](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| 小米 MiMo | `mimo-v2.6-pro` | $0.435 | $0.0036 | $0.87 | 海外美元价；国内 ¥3 / ¥6 / 百万 | [官方](https://mimo.mi.com/docs/en-US/price/pay-as-you-go) |
| 小米 MiMo | `mimo-v2.6-flash` | $0.14 | $0.0028 | $0.28 | 海外美元价；国内 ¥1 / ¥2 / 百万 | [官方](https://mimo.mi.com/docs/en-US/price/pay-as-you-go) |
| 小米 MiMo | `mimo-v2.6-pro-ultraspeed` | $4.35 | $0.036 | $8.70 | 定制服务（需联系小米）；国内 ¥30 / ¥60 / 百万 | [官方](https://mimo.mi.com/docs/en-US/price/pay-as-you-go) |
| xAI | `grok-4.7` | $2 | $0.50 | $6 | 提示 ≥200K：$4 / $12 | [官方](https://docs.x.ai/developers/pricing) |
| xAI | `grok-4.3` | $1.25 | $0.20 | $2.50 | 提示 ≥200K：$2.50 / $5 | [官方](https://docs.x.ai/developers/pricing) |
| Mistral | `mistral-medium-3-5` | $1.50 | — | $7.50 |  | [官方](https://docs.mistral.ai/models/model-cards/mistral-medium-3-5-26-04) |
| Mistral | `mistral-small-2603` | $0.15 | — | $0.60 |  | [官方](https://docs.mistral.ai/models/model-cards/mistral-small-4-0-26-03) |
| 月之暗面 Kimi | `kimi-k3` | $3 | $0.30 | $15 | 缓存写入另计（$3 / 百万，5 分钟 TTL） | [官方](https://platform.kimi.ai/docs/pricing/chat) |
| 月之暗面 Kimi | `kimi-k2.6` | $0.95 | $0.16 | $4 |  | [官方](https://platform.kimi.ai/docs/pricing/chat) |
| 智谱 GLM | `glm-5.3` | $1.40 | $0.26 | $4.40 | Z.ai 国际站 | [官方](https://docs.z.ai/guides/overview/pricing) |
| 智谱 GLM | `glm-5.3-flash` | $0.15 | $0.03 | $0.50 | Z.ai 国际站 | [官方](https://docs.z.ai/guides/overview/pricing) |
| 字节豆包 | `seed-2-0-pro` | $0.50 | $0.10 | $3 | BytePlus ModelArk（seed-2-0-pro-260328）；>128K：$1 / $6 | [官方](https://docs.byteplus.com/en/docs/ModelArk/1544106) |
| 字节豆包 | `seed-2-0-mini` | $0.10 | $0.02 | $0.40 | BytePlus ModelArk（seed-2-0-mini-260428）；>128K：$0.20 / $0.80 | [官方](https://docs.byteplus.com/en/docs/ModelArk/1544106) |
| 腾讯混元 | `hy4-preview` | $0.834 | $0.042 | $2.501 | TokenHub 国际站 | [官方](https://intl.cloud.tencent.com/zh/document/product/1300/78937) |
| 腾讯混元 | `hy3` | $0.132 | $0.033 | $0.528 | TokenHub 国际站 | [官方](https://intl.cloud.tencent.com/zh/document/product/1300/78937) |
| MiniMax | `MiniMax-M3` | $0.30 | $0.06 | $1.20 | Standard 档；>512K：$0.60 / $2.40 | [官方](https://platform.minimax.io/docs/guides/pricing-paygo) |
| MiniMax | `MiniMax-M3.1-Flash` | $0.15 | $0.015 | $0.60 |  | [官方](https://platform.minimax.io/docs/guides/pricing-paygo) |

## 同一负载的月费排行

示例负载：每天 1,000 次请求 × 30 天，每次 2,000 输入 + 500 输出 token，不计缓存、不计闲时折扣（按上表单价计算）。

| # | 模型 | 厂商 | 月费（美元） |
|---|---|---|---|
| 1 | `seed-2-0-mini` | 字节豆包 | $12.00 |
| 2 | `mimo-v2.6-flash` | 小米 MiMo | $12.60 |
| 3 | `gpt-6-luna` | OpenAI | $13.50 |
| 4 | `Claude Haiku 5.5` | Anthropic | $13.50 |
| 5 | `hy3` | 腾讯混元 | $15.84 |
| 6 | `qwen3.8-flash` | 阿里通义千问 | $16.05 |
| 7 | `glm-5.3-flash` | 智谱 GLM | $16.50 |
| 8 | `mistral-small-2603` | Mistral | $18.00 |
| 9 | `MiniMax-M3.1-Flash` | MiniMax | $18.00 |
| 10 | `deepseek-flash` | DeepSeek | $36.00 |
| 11 | `MiniMax-M3` | MiniMax | $36.00 |
| 12 | `mimo-v2.6-pro` | 小米 MiMo | $39.15 |
| 13 | `qwen3.7-plus` | 阿里通义千问 | $48.00 |
| 14 | `gemini-3.5-flash-lite` | Google | $55.50 |
| 15 | `seed-2-0-pro` | 字节豆包 | $75.00 |
| 16 | `hy4-preview` | 腾讯混元 | $87.56 |
| 17 | `gemini-3.8-flash` | Google | $101.25 |
| 18 | `grok-4.3` | xAI | $112.50 |
| 19 | `kimi-k2.6` | 月之暗面 Kimi | $117.00 |
| 20 | `deepseek-v4-pro` | DeepSeek | $138.60 |
| 21 | `glm-5.3` | 智谱 GLM | $150.00 |
| 22 | `mistral-medium-3-5` | Mistral | $202.50 |
| 23 | `qwen3.8-max` | 阿里通义千问 | $210.00 |
| 24 | `grok-4.7` | xAI | $210.00 |
| 25 | `gpt-6.1-sol` | OpenAI | $270.00 |
| 26 | `Claude Sonnet 5.5` | Anthropic | $270.00 |
| 27 | `gemini-4-argon` | Google | $270.00 |
| 28 | `gpt-5.3-codex` | OpenAI | $315.00 |
| 29 | `mimo-v2.6-pro-ultraspeed` | 小米 MiMo | $391.50 |
| 30 | `kimi-k3` | 月之暗面 Kimi | $405.00 |
| 31 | `Claude Opus 5.5` | Anthropic | $540.00 |
| 32 | `gpt-6-astra` | OpenAI | $1,350.00 |
| 33 | `Claude Fable 5.1` | Anthropic | $1,350.00 |

换成你自己的请求量、token 数、缓存命中率：**[大模型成本计算器](https://og.cc.cd/llm-cost-calculator/)**。

## 怎么读这张表

- **输出比输入贵**：表中模型的输出单价多为输入的 2–6 倍，长回答比长提示更花钱。
- **缓存命中很便宜**：重复的系统提示/文档前缀命中缓存后按“缓存命中”列计费，远低于输入价（例如 GPT-6 系列是输入价的 1/10）。详见 [如何用提示缓存省 token](https://og.cc.cd/guides/reduce-token-usage-prompt-caching/)。
- **长提示有分档**：GPT-6 系列 >272K、Claude Haiku 5.5 >100K、grok >200K、通义 3.7-plus >256K、豆包 Seed >128K、MiniMax-M3 >512K 时整次请求按高档计价。
- **Claude 的 token 更多**：Anthropic 说明 4.7 及以后模型的分词比旧版多约 30%，同一段文字按 Claude 计的 token 数更高。
- **DeepSeek 有闲时半价**；Gemini 4 Argon 与 3.8 Flash 已公布涨价日期（见备注）。

## 相关工具与指南

- [主流模型 API 价格对比（详细解读）](https://og.cc.cd/guides/llm-api-pricing-comparison/)
- [大模型成本计算器](https://og.cc.cd/llm-cost-calculator/) · [Token 计数器](https://og.cc.cd/token-counter/)
- [如何估算 LLM API 成本](https://og.cc.cd/guides/estimate-llm-api-costs/) · [上下文窗口对比](https://og.cc.cd/guides/llm-context-window-comparison/)
- [API Key 申请大全](https://github.com/yijzhu/awesome-llm-api-keys) · [个人 AI 助理 / Agent 对比](https://github.com/yijzhu/awesome-personal-ai-agents)

---

## English

USD per 1M tokens, standard (non-batch) tier; lowest context tier shown, higher tiers in the notes. “—” = cached price not published.

| Provider | Model | Input | Cached input | Output | Notes | Source |
|---|---|---|---|---|---|---|
| OpenAI | `gpt-6-astra` | $10 | $1 | $50 | >272K-token prompts: 2× input, 1.5× output | [source](https://developers.openai.com/api/docs/pricing) |
| OpenAI | `gpt-6.1-sol` | $2 | $0.10 | $10 | >272K-token prompts: 2× input, 1.5× output | [source](https://developers.openai.com/api/docs/pricing) |
| OpenAI | `gpt-6-luna` | $0.10 | $0.01 | $0.50 | >272K-token prompts: 2× input, 1.5× output | [source](https://developers.openai.com/api/docs/pricing) |
| OpenAI | `gpt-5.3-codex` | $1.75 | $0.175 | $14 |  | [source](https://developers.openai.com/api/docs/pricing) |
| Anthropic | `Claude Fable 5.1` | $10 | $0.25 | $50 |  | [source](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Anthropic | `Claude Opus 5.5` | $4 | $0.20 | $20 |  | [source](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Anthropic | `Claude Sonnet 5.5` | $2 | $0.10 | $10 |  | [source](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Anthropic | `Claude Haiku 5.5` | $0.10 | $0.01 | $0.50 | >100K-token prompts: $0.50 / $2.50 | [source](https://docs.anthropic.com/en/docs/about-claude/pricing) |
| Google | `gemini-4-argon` | $2 | $0.10 | $10 | Through 2026-11-30; $4 / $20 from 2026-12-01 | [source](https://ai.google.dev/gemini-api/docs/pricing) |
| Google | `gemini-3.8-flash` | $0.75 | $0.075 | $3.75 | Through 2026-12-31; $1.50 / $7.50 from 2027-01-01 | [source](https://ai.google.dev/gemini-api/docs/pricing) |
| Google | `gemini-3.5-flash-lite` | $0.30 | $0.03 | $2.50 |  | [source](https://ai.google.dev/gemini-api/docs/pricing) |
| DeepSeek | `deepseek-v4-pro` | $1.32 | $0.044 | $3.96 | Peak rate (cache miss); off-peak is half | [source](https://api-docs.deepseek.com/quick_start/pricing) |
| DeepSeek | `deepseek-flash` | $0.30 | $0.006 | $1.20 | Peak rate (cache miss); off-peak is half | [source](https://api-docs.deepseek.com/quick_start/pricing) |
| Alibaba Qwen | `qwen3.8-max` | $2 | — | $6 | Model Studio International (Singapore) | [source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| Alibaba Qwen | `qwen3.7-plus` | $0.40 | $0.08 | $1.60 | List price, International; limited-time 20% off shown on page; >256K: $1.2 / $4.8 | [source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| Alibaba Qwen | `qwen3.8-flash` | $0.15 | — | $0.47 | Model Studio International (Singapore) | [source](https://www.alibabacloud.com/help/en/model-studio/model-pricing) |
| Xiaomi MiMo | `mimo-v2.6-pro` | $0.435 | $0.0036 | $0.87 | Overseas USD price; China: ¥3 / ¥6 per 1M | [source](https://mimo.mi.com/docs/en-US/price/pay-as-you-go) |
| Xiaomi MiMo | `mimo-v2.6-flash` | $0.14 | $0.0028 | $0.28 | Overseas USD price; China: ¥1 / ¥2 per 1M | [source](https://mimo.mi.com/docs/en-US/price/pay-as-you-go) |
| Xiaomi MiMo | `mimo-v2.6-pro-ultraspeed` | $4.35 | $0.036 | $8.70 | Custom service (contact Xiaomi); China: ¥30 / ¥60 per 1M | [source](https://mimo.mi.com/docs/en-US/price/pay-as-you-go) |
| xAI | `grok-4.7` | $2 | $0.50 | $6 | >=200K-token prompts: $4 / $12 | [source](https://docs.x.ai/developers/pricing) |
| xAI | `grok-4.3` | $1.25 | $0.20 | $2.50 | >=200K-token prompts: $2.50 / $5 | [source](https://docs.x.ai/developers/pricing) |
| Mistral | `mistral-medium-3-5` | $1.50 | — | $7.50 |  | [source](https://docs.mistral.ai/models/model-cards/mistral-medium-3-5-26-04) |
| Mistral | `mistral-small-2603` | $0.15 | — | $0.60 |  | [source](https://docs.mistral.ai/models/model-cards/mistral-small-4-0-26-03) |
| Moonshot Kimi | `kimi-k3` | $3 | $0.30 | $15 | Cache writes billed separately ($3 / 1M, 5-min TTL) | [source](https://platform.kimi.ai/docs/pricing/chat) |
| Moonshot Kimi | `kimi-k2.6` | $0.95 | $0.16 | $4 |  | [source](https://platform.kimi.ai/docs/pricing/chat) |
| Zhipu GLM | `glm-5.3` | $1.40 | $0.26 | $4.40 | Z.ai international | [source](https://docs.z.ai/guides/overview/pricing) |
| Zhipu GLM | `glm-5.3-flash` | $0.15 | $0.03 | $0.50 | Z.ai international | [source](https://docs.z.ai/guides/overview/pricing) |
| ByteDance Doubao | `seed-2-0-pro` | $0.50 | $0.10 | $3 | BytePlus ModelArk (seed-2-0-pro-260328); >128K: $1 / $6 | [source](https://docs.byteplus.com/en/docs/ModelArk/1544106) |
| ByteDance Doubao | `seed-2-0-mini` | $0.10 | $0.02 | $0.40 | BytePlus ModelArk (seed-2-0-mini-260428); >128K: $0.20 / $0.80 | [source](https://docs.byteplus.com/en/docs/ModelArk/1544106) |
| Tencent Hunyuan | `hy4-preview` | $0.834 | $0.042 | $2.501 | TokenHub international | [source](https://intl.cloud.tencent.com/zh/document/product/1300/78937) |
| Tencent Hunyuan | `hy3` | $0.132 | $0.033 | $0.528 | TokenHub international | [source](https://intl.cloud.tencent.com/zh/document/product/1300/78937) |
| MiniMax | `MiniMax-M3` | $0.30 | $0.06 | $1.20 | Standard tier; >512K: $0.60 / $2.40 | [source](https://platform.minimax.io/docs/guides/pricing-paygo) |
| MiniMax | `MiniMax-M3.1-Flash` | $0.15 | $0.015 | $0.60 |  | [source](https://platform.minimax.io/docs/guides/pricing-paygo) |

Monthly ranking above: 1,000 requests/day × 30 days, 2,000 input + 500 output tokens each, no caching. Plug in your own numbers with the **[LLM cost calculator](https://og.cc.cd/llm-cost-calculator/)**; read the analysis in the **[LLM API pricing comparison](https://og.cc.cd/guides/llm-api-pricing-comparison/)**.

## 官方来源

- openai — [https://developers.openai.com/api/docs/pricing](https://developers.openai.com/api/docs/pricing)
- anthropic — [https://docs.anthropic.com/en/docs/about-claude/pricing](https://docs.anthropic.com/en/docs/about-claude/pricing)
- google — [https://ai.google.dev/gemini-api/docs/pricing](https://ai.google.dev/gemini-api/docs/pricing)
- deepseek — [https://api-docs.deepseek.com/quick_start/pricing](https://api-docs.deepseek.com/quick_start/pricing)
- qwen — [https://www.alibabacloud.com/help/en/model-studio/model-pricing](https://www.alibabacloud.com/help/en/model-studio/model-pricing)
- mimo — [https://mimo.mi.com/docs/en-US/price/pay-as-you-go](https://mimo.mi.com/docs/en-US/price/pay-as-you-go)
- xai — [https://docs.x.ai/developers/pricing](https://docs.x.ai/developers/pricing)
- mistralm — [https://docs.mistral.ai/models/model-cards/mistral-medium-3-5-26-04](https://docs.mistral.ai/models/model-cards/mistral-medium-3-5-26-04)
- mistrals — [https://docs.mistral.ai/models/model-cards/mistral-small-4-0-26-03](https://docs.mistral.ai/models/model-cards/mistral-small-4-0-26-03)
- kimi — [https://platform.kimi.ai/docs/pricing/chat](https://platform.kimi.ai/docs/pricing/chat)
- glm — [https://docs.z.ai/guides/overview/pricing](https://docs.z.ai/guides/overview/pricing)
- seed — [https://docs.byteplus.com/en/docs/ModelArk/1544106](https://docs.byteplus.com/en/docs/ModelArk/1544106)
- hunyuan — [https://intl.cloud.tencent.com/zh/document/product/1300/78937](https://intl.cloud.tencent.com/zh/document/product/1300/78937)
- minimax — [https://platform.minimax.io/docs/guides/pricing-paygo](https://platform.minimax.io/docs/guides/pricing-paygo)

---

## 许可与署名

内容以 [CC BY 4.0](LICENSE) 发布，转载请注明来源：[og.cc.cd — AI 开发者工具箱](https://og.cc.cd/)。
本仓库只收录官方页面写明的事实；“未写明”表示我们核对的官方页面没有说明，不代表答案是否定的。价格、额度和地区政策随时会变，**付费前请以官方页面为准**。

发现过期或错误？欢迎提 [Issue](../../issues) 或 PR，并附上官方来源链接。

## License

Content is licensed under [CC BY 4.0](LICENSE). Please credit [og.cc.cd — AI Developer Toolbox](https://og.cc.cd/).
Only facts stated on official pages are listed; “not stated” means the official pages we checked do not say. Prices, quotas and region rules change — **always confirm on the official page before you pay**.

Spotted something outdated? Open an [issue](../../issues) or PR with the official source link.
