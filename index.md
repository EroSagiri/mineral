---
title: 欢迎来到六月笔记
date: 2026-05-01
tags:
  - index
---

# 笔记索引

这里是我的个人知识库入口，用来连接日记、任务、旅行记录、碎片想法、概念笔记、图片集合和附件资源。

我几乎每天都会写日记，但日记不一定严格当天完成：有时会留到明天、后天补写，也有些日子可能不写。这个库以 Obsidian 作为主要写作入口，Web 页面用于浏览、搜索和公开展示。

## 实时心率
我佩戴佳明255手表连接手机，通过桥 [PulseBridge](https://github.com/EroSagiri/PulseBridge) 手机把实时的心率在这里呈现。这个是他的web部署页面 [Pulse](https://pulse.sighjune.com/)

**在此地留下一颗跳动的心**


<div style="display: flex; justify-content: center;">
  <iframe
    src="https://pulse.sighjune.com/embed.html?device=1552271651&layout=minimal&theme=dark&transparent=0&animate=0&status=0&name="
    title="实时心率"
    loading="lazy"
    width="140"
    height="70"
    style="max-width: 100%; border: 0; border-radius: 12px; overflow: hidden;"
  ></iframe>
</div>

## 快速入口

- [[daily/]]：每日记录，按日期保存。
- [[travel/]]：旅行、户外、路线和行程记录。
- [[fleeting/]]：碎片想法、随手记录、灵感和未整理念头。
- [[concepts/]]：概念、观点和长期沉淀。
- [[galleries/]]：图片集合、照片墙和相册索引。

## 写作流

一般情况下我每天都会写日记，写日记我现在一般都是直接发给ai agent工具，agent读取日记技能使尽量的减少格式改动只允许需要明确的错别字，加标签和尾部导航，通过 [bedrock-mcp](https://github.com/EroSagiri/bedrock-mcp) 工具调用知识库他运行在cloudflare上修改的是R2存储，所以他修改后我的客户端都会同步

当我打开在电脑或者手机打开obsidian通过社区插件自动同步R2到本地，然后我可以在笔记软件写其他的文章

每天一个特定时间 [mineral-publisher](https://github.com/EroSagiri/mineral-publisher) 会拉取R2全库然后冻结进入自动审核必要时人工审核确保哪些密钥隐私没有被提交，通过后自动提交到 [mineral](https://github.com/EroSagiri/mineral) 同时触发钩子在cloudflare通过 [quartz](https://github.com/EroSagiri/quartz) 构建page

实际体验下来可能就是日常写日记的话，对着 ai agent说，"今天日记一个换行日记正文"ai agent工具会自动处理，然后知识库里面就多出一篇日记了。写长文也可以打开obsidian沉浸式写一篇，他也会自动同步。还有自动备份整个知识库的机制。