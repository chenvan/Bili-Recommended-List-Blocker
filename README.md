# 屏蔽b站首页推荐中的指定up

## 功能:
- 在首页推荐和推广栏的视频卡片的右边会有一个屏蔽按钮，点击即可屏蔽该up主哦.
- 屏蔽了推广栏广告

github: https://github.com/kuzen/Bili-Recommended-List-Blocker

greasyfork: https://greasyfork.org/zh-CN/scripts/437528-bili-recommended-list-blocker

![20211224212815](https://s2.loli.net/2021/12/24/E4HL193jXkcWsdn.gif)
## PS: 
- 黑名单数据存储在浏览器中，不会因清除cookies而丢失
- 仅适配新版首页，旧版首页未适配！
- 首页右下角的按钮可打开插件设置
- 屏蔽图以base64形式保存在脚本中

## 找不到新版主页入口？  
浏览器F12打开控制台，然后输入以下内容回车即可！

```javascript
var a = new Date;
a.setTime(a.getTime() + 24 * 365 * 60 * 60 * 1e3);
document.cookie = "i-wanna-go-back" + "=" + escape(-1) + ";expires=" + a.toGMTString() + "; path=/; domain=.bilibili.com";
location.reload();
```

## TODO
- 添加屏蔽关键词
- 加快屏蔽速度

# 已知问题:
- 换一换按钮的处理逻辑在点击后1秒运行，如果网速较慢可能脚本先于b站加载，此时屏蔽会失效


# Reference:
部分样式参考了：https://github.com/ipcjs/bilibili-helper

图标来源：https://github.com/bytedance/iconpark

屏蔽图：https://t.bilibili.com/482652949960802810

头像：https://t.bilibili.com/441451749597806568