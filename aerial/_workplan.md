# Workplan

0406: 
尝试投影 
继续切图
- gif示范
- 让网页使用jekyll模板
调整seo, 按照wuhan来优化
- 写一个博客, 让大家留言交流
发朋友圈之类的


longterm:
根据网页center(api)
展示数据
找老师合作
写文档, 展示历史全貌
google translate


现在有个地图 可以更好的展示数据了
方法1: 单个的html

方法2: embed到post中: xx.md `{% include map/map.html %}`

比如:
原来是西直门/原所有人/哪年被拆/拆除主体/拆除原因/当前用途/当前所有人/地理位置/地图编码

大地图的解决方案
1. 大图片缩放 
http://ignitersworld.com/lab/imageViewer.html

2. 做成真地图 用baidu或者google的地图api, 叠加底图 
2.1 一张大图 http://lbsyun.baidu.com/index.php?title=jspopularGL/guide/groundOverlay
做完了, 具体参见satellite文件夹
下一步需要调整图片曝光曲线, 更好的同时展示底图和图层
然后放到网上

baidu gps:     
  var SW = new BMapGL.Point(116.3488,39.8735);
  var NE = new BMapGL.Point(116.456,39.9618);

google: 
  W:116.335963w,  S:39.865712° N
  E: 116.443325°W,  N:39.954054°N


2.2 tile 
http://lbs.baidu.com/jsdemo.htm#g0_2
http://lbsyun.baidu.com/jsdemo.htm#webgl5_1 我可以ref到inbeijing的api
tile需要切图 有点烦

百度API
http://lbsyun.baidu.com/apiconsole/auth#/home
key不能用
credential放在github的方法
manual http://lbsyun.baidu.com/index.php?title=jspopularGL/guide/groundOverlay

2.3 用openstreetmap之类的自己提供地图服务
osm介绍 https://switch2osm.org/why-switch/
建筑物3d:https://osmbuildings.org/documentation/viewer/
leaflet raster layer: canvas, imageoverlay, tiles, etc.
https://leafletjs.com/reference-0.7.7.html#imageoverlay
可以bring to back, set opacity, etc.
上传aerial https://docs.openaerialmap.org/uploader/uploader-form/

# 突出大体量建筑
1. 地图调整
https://developer.baidu.com/map/custom/
元素 -> 建筑物 -> 颜色

2. osmbuilding
https://osmbuildings.org/documentation/viewer/

3. 龙鹰的building数据库
http://www.xuetangx.com/courses/course-v1:TsinghuaX+70000662+2018_T2/courseware/95eee3f97b2c4fe88540288c43517c9a/dd0895df151e4776ab5a8b521ea35abb/
Buildings2017 建筑物
parcels2011 地块
functionzone 功能区
residentialcommunity 住宅小区
点数据 - 土地交易2013
点数据 - 房价
点数据 - 公司/写字楼/兴趣点

baidu gps:     
    var SW = new BMapGL.Point(116.3488,39.8735);
    var NE = new BMapGL.Point(116.4560,39.9618);
