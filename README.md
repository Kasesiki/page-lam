# page-lam
个人开发简约匿名留言板, 模板实现0依赖，极限LCP可达0.07s, lighthose性能，无障碍，最佳做法，SEO均满分

可以作为网页初学者项目学习使用, 使用alpine.js框架

单html文件实现，需自行填写<%- title %>，<%- flows %>， <%- alpine %>模板内容

title为标题，flows为一个值类型为[String, String, String, int, int]的数组，alpine为alpine.js v3.15.11的.min.js文件

网页还调用了一个api和一个字体文件，字体文件可以自动回退，api只是通过offset来获取更旧时间的消息，在原版实现中，每次api返回的limit为20条，可以自行修改，和在预览连接中自行分析

预览：https://www.lyxnxia.space/lam

简单而不粗糙，实现了完美自适应加动态响应效果，在多端测试表现良好

<img width="2560" height="1393" alt="image" src="https://github.com/user-attachments/assets/c4bfa187-99d9-43c5-b46b-6922ac65ff36" />

<img width="1171" height="1392" alt="image" src="https://github.com/user-attachments/assets/9e5354fa-41bc-4313-93bd-b725c7f71544" />

对于Lighthouse的无障碍测试中，对比度方面出现：`背景色和前景色没有足够高的对比度。`的问题，是因为文字动效采用opacity透明度做动效导致检测有误，实际为rgb(89,89,89)已经达到WACG AAA标准
