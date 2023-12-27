------
这个项目可以部署在 Cloudflare Workers 上，参考 Cloudflare 的许可协议，不违反现有规定。（而且现有的 Workers 反向代理也不少）

userID是 VLESS 连接时的 UUID，proxyIP用于解决 Cloudflare Workers 无法直接连接 Cloudflare 服务器的问题（据描述，是 Cloudflare 的 bug，导致无代理/中转时无法访问使用 Cloudflare CDN 的网站），参考 issue162。

复制源码到新建的 Workers 代码中即可，推荐使用环境变量UUID和PROXYIP来设置这两个配置项。部署完成后，访问Workers地址/UUID即可获得配置信息。
