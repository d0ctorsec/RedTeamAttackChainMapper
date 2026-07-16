![RedTeamAttackChainMapper](https://socialify.git.ci/d0ctorsec/RedTeamAttackChainMapper/image?forks=1&language=1&name=1&owner=1&stargazers=1&theme=Light)

**0x00前言：最近打攻防时因为攻击链路比较复杂，想着找一款好的拓扑生成工具，发现要么部署麻烦、要么操作麻烦、要么开会员，网上居然没有佬专门解决攻防资产管理的问题，没办法自己用AI写了一个开箱即用的拓扑绘制页面，觉得效果很好就分享出来了。**

<h3 align="center">觉得有帮助给个 Star 咯 🌟</h3>

## 0x00.简介

```markdown
# 拖拽式攻击路径可视化工具，浏览器打开即用，无需联网，就这么简单。
1. 浏览器打开 `attack-path-tool.html`
2. 从左侧拖拽节点到画布
3. 右键节点 → 连线 → 点击目标
4. 点选节点/连线，右侧编辑IP、备注、凭据等
5. Ctrl+S 保存,下次使用加载对应json即可，当前项目也支持自动保存
```

![image-20260715214830639](https://raw.githubusercontent.com/d0ctorsec/RedTeamAttackChainMapper/refs/heads/main/README.assets/image-20260715214830639.png)

## 0x01.怎么用

```markdown
**画攻击路径图** — 从左侧拖拽节点到画布，右键连线，直观展示从外网入口到域控的完整攻击链，方便制订攻击方向
**记录跳板机** — 标记哪些主机已控、哪些是跳板、哪些是高价值目标
**记录凭据** — 每个节点可记录拿到的账号密码/Hash，一目了然
**标注横向移动方式** — PTH、SSH、RDP、SMB、WMI 等18种方式可选，支持MITRE ATT&CK标签
**导出截图** — 一键导出PNG，直接贴到渗透测试报告里
```

![iShot_2026-07-15_22.08.00](https://raw.githubusercontent.com/d0ctorsec/RedTeamAttackChainMapper/refs/heads/main/README.assets/iShot_2026-07-15_22.08.00.gif)

**保存和加载** — 项目存为 `.atk.json` 文件，下次打开继续编辑

![image-20260715221642935](https://raw.githubusercontent.com/d0ctorsec/RedTeamAttackChainMapper/refs/heads/main/README.assets/image-20260715221642935.png)

## 0x02.后续

```markdown
后续会基于实战加入一些小众的需求，目前实现成这样已经完全够用了。
```

### v1.1.0更新

**新增-隧道连接线**：隧道独立为虚线，支持填写隧道工具、隧道类型、隧道地址凭据
**新增-自动保存功能**：编辑时自动保存，不会丢失进度兼容chrome、firefox等浏览器

**修复-图标显示不清晰问题**

![image-20260716001751829](https://raw.githubusercontent.com/d0ctorsec/RedTeamAttackChainMapper/refs/heads/main/README.assets/image-20260716001751829.png)

### v1.2.0更新

**新增-搜索功能**：可全局搜索对应资产，自动展开资产详情

**修复-修复导出图片无法显示背景问题**
