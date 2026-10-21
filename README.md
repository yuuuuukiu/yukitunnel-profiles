# YukiTunnel Profile Registry

Signed, declarative cloud firewall profiles for [YukiTunnel](https://github.com/yuuuuukiu/yukitunnel).

```
profiles/*.yaml       声明式 profile
index.json            CI 生成，勿手改
index.json.sig        ed25519 签名，CI 生成
```

## 客户端如何使用

`yuki-server` 内置公钥会验证本仓库的 `index.json.sig`。任何源（jsDelivr、
raw.githubusercontent、Cloudflare R2）都只是传输层，签名决定可信度。

## 如何新增/修改 profile

见 [yukitunnel 仓库的 docs/PROFILE-GUIDE.md](https://github.com/yuuuuukiu/yukitunnel/blob/main/docs/PROFILE-GUIDE.md)。

## 镜像

| 源 | 地址 |
| --- | --- |
| jsDelivr | `https://cdn.jsdelivr.net/gh/yuuuuukiu/yukitunnel-profiles@main` |
| GitHub raw | `https://raw.githubusercontent.com/yuuuuukiu/yukitunnel-profiles/main` |
| R2（可选） | `https://tunnel.yuuuuukiu.top` |

三个源必须字节一致；客户端会对每个源单独验签。
