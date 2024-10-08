<p align="center">
  <img width="100px" src="https://user-images.githubusercontent.com/35565811/214613019-6fd702b7-445e-4663-8471-f47005241724.png" align="center" alt="GitHub Readme Stats" />
 
  <p align="center">
  </p>

  <p align="center">
    <a href="https://cdn.jsdelivr.net/gh/vanchkong/proxy-rules@release/applications-rules.txt">Clash 应用规则列表</a> |
    <a href="https://cdn.jsdelivr.net/gh/vanchkong/proxy-rules@release/custom-direct-rules.txt">Clash 自定义直连列表</a> |
    <a href="https://cdn.jsdelivr.net/gh/vanchkong/proxy-rules@release/custom-proxy-rules.txt">Clash 自定义代理列表</a> 
    <br>
    <a href="https://cdn.jsdelivr.net/gh/vanchkong/proxy-rules@release/applications-rules.list">Loon 应用规则列表</a> |
    <a href="https://cdn.jsdelivr.net/gh/vanchkong/proxy-rules@release/custom-direct-rules.list">Loon 自定义直连列表</a> |
    <a href="https://cdn.jsdelivr.net/gh/vanchkong/proxy-rules@release/custom-proxy-rules.list">Loon 自定义代理列表</a>
  </p>

</p>

### 工具介绍

- 当用户更新规则后，使用 Github Actions 自动将规则缓存到免费 CDN 上
- 用户在 github 上更新规则后，在 clash 或 Loon 上点击刷新即可拉取更新

### 如何自定义

1. fork 本仓库：[复刻 vanchkong/proxy-rules](https://github.com/vanchkong/proxy-rules/fork)
2. 触发 GitHub Action 中的 `Generate Rules for Clash` 工作流
3. 编辑 `*-rules.*` 以自定义规则
4. 在对应的 Clash 或 Loon 上刷新配置文件

Tips:

> a. 可通过访问进行验证 `https://cdn.jsdelivr.net/gh/{你的GITHUB用户名}/proxy-rules@release/`  
> c. **该仓中以 rules.\* 结尾的文件，都会缓存到 jsdelivr CDN 中，可以自定义！**

### CDN 缓存没有更新怎么办？

> 这是因为 jsdelivr CDN 缓存的原因，一般来说是 24 小时刷新缓存，但是这样太慢了！  
> 不过 jsdelivr CDN 也提供手动刷新缓存的方法：

```
# 假设你的文件 URL 是这样：
https://cdn.jsdelivr.net/xxx/xxx...

# 那么把域名中的 cdn 改为 purge 即可：
https://purge.jsdelivr.net/xxx/xxx...
```

然后访问这个文件新 URL 就会提示你刷新成功！

### 覆写

> 我还准备了 [clash 的 扩展脚本](./clash.js)、[Loon 的 覆写配置](./loon.conf)，
