
原工程
https://github.com/bestony/hexo-generator-podcasts/


1.
用_feed.xml替换掉template/feed.xml

2.注意feed.xml这里hardcode一下，以后有空我会解决这个bug，主要nodejs代码不熟。

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

_config.yml 这个地方代码失效，因为直接在feed.xmlhardcode了
```
category: 
    - Arts
    - Design
```


好了这样就解决podcast的验证问题了




