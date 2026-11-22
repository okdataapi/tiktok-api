# TikTok API: video search, comments, creators, hashtags, ads and transcripts

**TikTok data API · TikTok video search · TikTok comments · TikTok creator profiles and followers · TikTok Ads Library and Creative Center · TikTok Shop · TikTok transcripts.**

Examples for the [okdata](https://okdata.online/?src=gh-tiktok-api) TikTok API: 17 live endpoints behind one API key, pay per call from $0.002. No TikTok login, no cookies and no browser, so there is no account to get blocked.

[Sign up free ($0.10 of trial credit)](https://okdata.online/signup/?src=gh-tiktok-api) · [All TikTok endpoints](https://okdata.online/apis/tiktok/?src=gh-tiktok-api) · [Use it from Claude, Cursor or any MCP client](https://okdata.online/mcp/?src=gh-tiktok-api)

## Endpoints

| Endpoint | What it returns | Price | Path |
|---|---|---|---|
| [TikTok video search](https://okdata.online/apis/tiktok/videos/search/?src=gh-tiktok-api) | Videos matching keywords worldwide, with plays, likes, comments and shares. | $0.002 a call | `GET /v1/tiktok/videos/search` |
| [TikTok video detail](https://okdata.online/apis/tiktok/videos/get/?src=gh-tiktok-api) | One video by ID or link. | $0.002 a call | `GET /v1/tiktok/videos/get` |
| [TikTok video comments](https://okdata.online/apis/tiktok/videos/comments/list/?src=gh-tiktok-api) | Comments on a video with likes and reply counts. | $0.002 a call | `GET /v1/tiktok/videos/comments/list` |
| [TikTok account profile](https://okdata.online/apis/tiktok/users/get/?src=gh-tiktok-api) | Followers, likes, video count and bio of an account. | $0.002 a call | `GET /v1/tiktok/users/get` |
| [TikTok Ads Library search](https://okdata.online/apis/tiktok/ads/search/?src=gh-tiktok-api) | Search TikTok's public Ads Library (ads shown in Europe) by keyword or by advertiser name: advertiser, headline, videos and images, first and last day shown and the library's bracket of people reached. A transparency record of all ads, not the Creative Center's showcase. | $0.004 a call | `GET /v1/tiktok/ads/search` |
| [TikTok Creative Center top ads](https://okdata.online/apis/tiktok/creative_center/ads/search/?src=gh-tiktok-api) | Search the Top Ads of TikTok's Creative Center by keyword: the ad's video, caption and brand, for one country over the last 7, 30 or 180 days. With view=full also likes, click-through rate, budget level, objective and industry. A showcase of ads that did well, without run dates. | $0.002 a call | `GET /v1/tiktok/creative_center/ads/search` |
| [TikTok Shop product search](https://okdata.online/apis/tiktok/shop/products/search/?src=gh-tiktok-api) | Search TikTok Shop products by keyword: title, current and original price, units sold, rating, number of reviews, image and shop. | $0.004 a call | `GET /v1/tiktok/shop/products/search` |
| [TikTok Shop product detail](https://okdata.online/apis/tiktok/shop/products/get/?src=gh-tiktok-api) | One TikTok Shop product by ID or link: title, price and discount, units sold, rating, number of reviews, all images, and the shop with its rating and followers. | $0.002 a call | `GET /v1/tiktok/shop/products/get` |
| [TikTok Shop product reviews](https://okdata.online/apis/tiktok/shop/products/reviews/list/?src=gh-tiktok-api) | Buyers' reviews of a TikTok Shop product: stars, text, the variant bought, photos and whether the purchase is verified. | $0.002 a call | `GET /v1/tiktok/shop/products/reviews/list` |
| [TikTok video transcript](https://okdata.online/apis/tiktok/videos/transcript/get/?src=gh-tiktok-api) | What is said in a TikTok video, by ID or link: the whole text and timed segments, from the video's captions (TikTok's own, often auto-generated). lang picks the captions' language; a video without captions in it comes back not found and is charged like any lookup. | $0.002 a call | `GET /v1/tiktok/videos/transcript/get` |
| [TikTok comment replies](https://okdata.online/apis/tiktok/comments/replies/list/?src=gh-tiktok-api) | The replies to a comment, by the comment's ID and its video's ID, 20 a page: text, replier, likes, time posted and which comment each one answers. A comment that does not exist reads like one without replies: an empty page, not a 404. | $0.002 a call | `GET /v1/tiktok/comments/replies/list` |
| [TikTok account search](https://okdata.online/apis/tiktok/users/search/?src=gh-tiktok-api) | Find TikTok accounts by keyword, 30 a page: handle, name, avatar, followers, following, video count and likes received. | $0.002 a call | `GET /v1/tiktok/users/search` |
| [TikTok account videos](https://okdata.online/apis/tiktok/users/videos/list/?src=gh-tiktok-api) | The videos an account posted, by handle, 10 a page, newest or most popular first: caption, plays, likes, comments, shares, saves and time posted. Pinned videos are marked as such (ext.is_pinned). | $0.002 a call | `GET /v1/tiktok/users/videos/list` |
| [TikTok Creative Center top ad](https://okdata.online/apis/tiktok/creative_center/ads/get/?src=gh-tiktok-api) | One Top Ad of TikTok's Creative Center by its ID: the ad's video and cover, caption, brand, landing page, and under ext its likes, comments, shares, length, objective, industry and the countries it ran in. A showcase entry, without run dates. | $0.002 a call | `GET /v1/tiktok/creative_center/ads/get` |
| [TikTok Shop seller products](https://okdata.online/apis/tiktok/shop/sellers/products/list/?src=gh-tiktok-api) | The products a TikTok Shop seller in the United States has on sale, by the seller's ID, a page at a time (TikTok sets the size, often 10 to 20): title, current and original price, rating, number of reviews, units sold and image. | $0.002 a call | `GET /v1/tiktok/shop/sellers/products/list` |
| [TikTok account followers](https://okdata.online/apis/tiktok/users/followers/list/?src=gh-tiktok-api) | The accounts following a TikTok account, newest followers first, 20 a page, by handle or account ID: handle, name, bio, avatar, followers, following, video count, likes received, and (under ext) the follower's country or region and language. | $0.002 a call | `GET /v1/tiktok/users/followers/list` |
| [TikTok hashtag videos](https://okdata.online/apis/tiktok/hashtags/videos/list/?src=gh-tiktok-api) | The videos under a hashtag, by its name, about 20 a page in TikTok's order: caption, author, plays, likes, comments, shares, saves, hashtags and time posted, with length, cover and music under ext. | $0.002 a call | `GET /v1/tiktok/hashtags/videos/list` |

## Quick start

1. Sign up at the [okdata console](https://okdata.online/signup/?src=gh-tiktok-api) with your email and copy the key that starts with `okd_`.
2. Make a call:

```bash
export OKDATA_API_KEY=okd_...
curl -G "https://api.okdata.online/v1/tiktok/videos/search" \
  -H "Authorization: Bearer $OKDATA_API_KEY" \
  --data-urlencode 'query=ai agents'
```

The Python version is [examples/quickstart.py](examples/quickstart.py) (standard library only, and it fetches a second page too): `python3 examples/quickstart.py`.

Every endpoint answers in the same shape: the list is in `data.items`, `page.next_cursor` goes back as `cursor` for the next page, what the call cost is in `meta.billing.amount`, and a field the platform does not provide is null with the reason in `meta.unavailable`.

## Use it from AI (MCP)

Claude Code:

```bash
claude mcp add --transport http --scope user okdata https://api.okdata.online/mcp --header "Authorization: Bearer $OKDATA_API_KEY"
```

Cursor, Windsurf, VS Code and other clients with remote MCP:

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

Then ask in plain words, for example "TikTok video search: ai agents". The agent uses the free `find` and `describe` tools to pick the endpoint and see its price, then `call` to fetch the data.

## FAQ

**Do I need a TikTok account?** No. The data is public content, fetched on the server; your own account is never involved.

**How is it billed?** Each endpoint has its own price, listed above for one call; endpoints billed per item count what comes back. New accounts get $0.10 to try; after that, top-ups start at $10 and never expire, with no subscription. Pricing: https://okdata.online/pricing/?src=gh-tiktok-api · Billing details: https://okdata.online/docs/billing/?src=gh-tiktok-api

**Why not TikTok's own APIs?** The Display API reads only the accounts that log in to your app, and the Research API is for approved academic and non-profit researchers. This returns what anyone can see on TikTok: search results, other creators' videos and profiles, comments, hashtags and ads.

**Can I page through results?** Each page of a list is one call: pass `page.next_cursor` back as `cursor` for the next one. A cursor stays valid for 24 hours.

**What happens when a call fails?** Every error has a fixed `code`, a `message`, and says whether you were charged (`charged`) and whether to retry (`retry`). All error codes: https://okdata.online/docs/errors/?src=gh-tiktok-api

## 中文说明

**TikTok 数据 API · TikTok 视频搜索 · TikTok 评论采集 · TikTok 达人数据 · TikTok 广告库 · TikTok 字幕。**

okdata 的TikTok接口示例：17 个接口在线可用，一个 API Key 调用，按次计费（$0.002 起），不用登录平台账号、不用 Cookie。中文文档：https://okdata.online/zh/apis/tiktok/?src=gh-tiktok-api · 注册：https://okdata.online/zh/signup/?src=gh-tiktok-api · 接入 AI（MCP）：https://okdata.online/zh/mcp/?src=gh-tiktok-api

## License

MIT. The data comes from the okdata API; its terms apply to API use.
