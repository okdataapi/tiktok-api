# TikTok 数据接口（TikTok API）：视频搜索、评论、达人、话题、广告、字幕

**TikTok 数据 API · TikTok 视频搜索 · TikTok 评论采集 · TikTok 达人数据 · TikTok 广告库 · TikTok 字幕。**

这个仓库是 [okdata](https://okdata.online/zh/?src=gh-tiktok-api) 的TikTok接口示例：17 个接口在线可用，一个 API Key 调用，按次计费（$0.002 起），失败不扣费。不用登录平台账号，不用 Cookie，不开浏览器，所以也不存在账号被风控的问题。

[免费注册拿 Key（送 $0.1 试用额度）](https://okdata.online/zh/signup/?src=gh-tiktok-api) · [全部接口文档](https://okdata.online/zh/apis/?src=gh-tiktok-api) · [接入 AI（MCP）](https://okdata.online/zh/mcp/?src=gh-tiktok-api)

## 接口清单

| 接口 | 说明 | 价格 | 路径 |
|---|---|---|---|
| [TikTok 视频搜索](https://okdata.online/zh/apis/tiktok/videos/search/) | 按关键词搜全球的 TikTok 视频，带播放、点赞、评论和分享。 | $0.002 / 次 | `GET /v1/tiktok/videos/search` |
| [TikTok 视频详情](https://okdata.online/zh/apis/tiktok/videos/get/) | 按 ID 或链接取一个视频。 | $0.002 / 次 | `GET /v1/tiktok/videos/get` |
| [TikTok 视频评论](https://okdata.online/zh/apis/tiktok/videos/comments/list/) | 视频评论，带点赞和回复数。 | $0.002 / 次 | `GET /v1/tiktok/videos/comments/list` |
| [TikTok 账号信息](https://okdata.online/zh/apis/tiktok/users/get/) | 账号的粉丝、获赞、作品数和简介。 | $0.002 / 次 | `GET /v1/tiktok/users/get` |
| [TikTok 广告库搜索](https://okdata.online/zh/apis/tiktok/ads/search/) | 按关键词或广告主名称搜 TikTok 公开广告库（在欧洲投放的广告）：广告主、标题、视频和图片、首次和最近投放日期，以及广告库给出的触达人数区间。这是全部广告的透明记录，不是创意中心的精选。 | $0.004 / 次 | `GET /v1/tiktok/ads/search` |
| [TikTok 创意中心热门广告](https://okdata.online/zh/apis/tiktok/creative_center/ads/search/) | 按关键词搜 TikTok 创意中心的热门广告：广告视频、文案和品牌，按国家和近 7、30 或 180 天。view=full 时另有点赞、点击率、预算档位、投放目标和行业。这是表现好的广告精选，没有投放日期。 | $0.002 / 次 | `GET /v1/tiktok/creative_center/ads/search` |
| [TikTok Shop 商品搜索](https://okdata.online/zh/apis/tiktok/shop/products/search/) | 按关键词搜 TikTok Shop 商品：标题、现价和原价、销量、评分、评价数、图片和店铺。 | $0.004 / 次 | `GET /v1/tiktok/shop/products/search` |
| [TikTok Shop 商品详情](https://okdata.online/zh/apis/tiktok/shop/products/get/) | 按 ID 或链接取一个 TikTok Shop 商品：标题、价格和折扣、销量、评分、评价数、全部图片，以及店铺和店铺评分、粉丝数。 | $0.002 / 次 | `GET /v1/tiktok/shop/products/get` |
| [TikTok Shop 商品评价](https://okdata.online/zh/apis/tiktok/shop/products/reviews/list/) | TikTok Shop 商品的买家评价：星级、内容、购买的款式、晒图，以及是否为已验证购买。 | $0.002 / 次 | `GET /v1/tiktok/shop/products/reviews/list` |
| [TikTok 视频字幕](https://okdata.online/zh/apis/tiktok/videos/transcript/get/) | 按视频 ID 或链接取 TikTok 视频里说的话：全文和带时间的分段，来自视频的字幕（TikTok 自己的，多为自动生成）。lang 指定字幕语言；视频没有这种语言的字幕时按找不到处理，不收费。 | $0.002 / 次 | `GET /v1/tiktok/videos/transcript/get` |
| [TikTok 评论回复](https://okdata.online/zh/apis/tiktok/comments/replies/list/) | 按评论 ID 和所在视频 ID 取这条评论下的回复，每页 20 条：内容、回复者、点赞、发布时间，以及每条回的是哪一条。评论不存在时和没有回复一样，返回空结果，不报 404。 | $0.002 / 次 | `GET /v1/tiktok/comments/replies/list` |
| [TikTok 账号搜索](https://okdata.online/zh/apis/tiktok/users/search/) | 按关键词找 TikTok 账号，每页 30 个：用户名、名称、头像、粉丝数、关注数、作品数和获赞数。 | $0.002 / 次 | `GET /v1/tiktok/users/search` |
| [TikTok 账号作品](https://okdata.online/zh/apis/tiktok/users/videos/list/) | 按用户名取账号发布的视频，每页 10 条，按最新或最热排：文案、播放、点赞、评论、分享、收藏和发布时间。置顶的视频会标出来（ext.is_pinned）。 | $0.002 / 次 | `GET /v1/tiktok/users/videos/list` |
| [TikTok 创意中心热门广告详情](https://okdata.online/zh/apis/tiktok/creative_center/ads/get/) | 按 ID 取 TikTok 创意中心的一条热门广告：广告视频和封面、文案、品牌、落地页，ext 里还有点赞、评论、分享、时长、投放目标、行业和投放国家。这是精选展示，没有投放日期。 | $0.002 / 次 | `GET /v1/tiktok/creative_center/ads/get` |
| [TikTok Shop 店铺商品](https://okdata.online/zh/apis/tiktok/shop/sellers/products/list/) | 按店铺 ID 取一家 TikTok Shop 美国站店铺在售的商品，一页一页取（每页多少由 TikTok 决定，通常 10 到 20 个）：标题、现价和原价、评分、评价数、已售件数和图片。 | $0.002 / 次 | `GET /v1/tiktok/shop/sellers/products/list` |
| [TikTok 账号粉丝列表](https://okdata.online/zh/apis/tiktok/users/followers/list/) | 按用户名或账号 ID 取关注某个 TikTok 账号的人，最新关注的在前，每页 20 个：用户名、名称、简介、头像、粉丝数、关注数、作品数、获赞数，ext 里还有粉丝的国家或地区和语言。 | $0.002 / 次 | `GET /v1/tiktok/users/followers/list` |
| [TikTok 话题作品](https://okdata.online/zh/apis/tiktok/hashtags/videos/list/) | 按话题名取话题下的视频，每页约 20 条，按 TikTok 给的顺序：文案、作者、播放、点赞、评论、分享、收藏、话题标签和发布时间，ext 里还有时长、封面和音乐。 | $0.002 / 次 | `GET /v1/tiktok/hashtags/videos/list` |

## 快速开始

1. 在 [okdata 控制台](https://okdata.online/zh/signup/?src=gh-tiktok-api) 用邮箱注册，拿到 `okd_` 开头的 Key。
2. 调一次接口：

```bash
export OKDATA_API_KEY=okd_...
curl -G "https://api.okdata.online/v1/tiktok/videos/search" \
  -H "Authorization: Bearer $OKDATA_API_KEY" \
  --data-urlencode 'query=ai agents'
```

Python 版在 [examples/quickstart.py](examples/quickstart.py)（只用标准库，会顺带演示翻页）：`python3 examples/quickstart.py`。

返回统一的结构：列表在 `data.items`，下一页用 `page.next_cursor` 传回 `cursor`，这次扣了多少钱在 `meta.billing.amount`，平台不提供的字段为 null 并在 `meta.unavailable` 里写明原因。

## 让 AI 直接用（MCP）

Claude Code：

```bash
claude mcp add --transport http --scope user okdata https://api.okdata.online/mcp --header "Authorization: Bearer $OKDATA_API_KEY"
```

Cursor、Cherry Studio、WorkBuddy 等支持远程 MCP 的客户端：

```json
{
  "mcpServers": {
    "okdata": {
      "url": "https://api.okdata.online/mcp",
      "headers": {
        "Authorization": "Bearer okd_..."
      }
    }
  }
}
```

接好以后直接用中文说需求，比如「TikTok 视频搜索：ai agents」。AI 会先用免费的 `find`、`describe` 找接口和看价格，再用 `call` 取数据。

## 常见问题

**要登录平台账号吗？** 不用。数据是公开内容，okdata 在服务端获取，你的账号完全不参与。

**怎么收费？** 每个接口单独定价，表里写的就是一次调用的价格；按条计费的接口按实际返回条数算。调用失败（包括超时）不扣费。新账号送 $0.1 试用额度，之后按需充值，没有订阅。价格页：https://okdata.online/zh/pricing/

**和官方开放平台有什么区别？** 官方开放平台只能读授权给你的账号自己的数据，而且要企业资质和审核；这里是平台上任何人都能看到的公开数据，比如搜索结果、别人的笔记或视频、评论、热榜。

**能翻页吗？** 列表接口每页一次调用，把 `page.next_cursor` 原样传回 `cursor` 就是下一页，24 小时内有效。

**出错了怎么办？** 每个错误都有固定的 `code`、中文说明 `message_zh`，以及会不会扣费（`charged`）和要不要重试（`retry`）。全部错误码：https://okdata.online/zh/docs/errors/

## English

Examples for the okdata TikTok API: 17 live endpoints behind one API key, pay per call from $0.002, failed calls free, no platform login or cookies. Sign up at https://okdata.online/signup/?src=gh-tiktok-api, docs at https://okdata.online/apis/, MCP at https://okdata.online/mcp/.

## License

MIT. The data comes from the okdata API; its terms apply to API use.
