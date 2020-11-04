解决podcast 收录验证问题，验证网址
https://podba.se/validate/?url=https://fm.fanfq.com/feed/podcast/

解决后的效果如下
![preview](validate.png)


原工程
https://github.com/bestony/hexo-generator-podcasts/

以下是修改步骤

1.
用本工程源码中 `_feed.xml` 替换掉原工程 `template/feed.xml`

2.注意新的`feed.xml`这里是hardcode，以后有空我会解决这个bug，主要nodejs代码不熟。

```
<!-- 这个地方hardcode一下 -->
    <itunes:category text="Arts">
      <itunes:category text="Design"/>
      <itunes:category text="Visual Arts"/>
    </itunes:category>
    <itunes:category text="Technology">
      <itunes:category text="Tech News"/>
    </itunes:category>
```

hexo 的`_config.yml` 这个地方代码失效，因为直接在`feed.xml`hardcode了
```
category: 
    - Arts
    - Design
```


好了这样就解决podcast的验证问题了




