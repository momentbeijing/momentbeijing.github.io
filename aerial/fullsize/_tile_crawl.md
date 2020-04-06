## tile爬虫
从代码中找到地图服务的xyz地址
然后确定想要的z, 一般是最清楚的
然后找到xy范围 一个一个tile下载

## 拼接
然后用python的PIL拼在一起
可以适当压缩图片

## georef
qgis - raster - georeferencer
打开你的图, 然后开一个ref的地图, 我用的osm坐标, 所以用的bing的aerial map
一个点一个点找ref 开两个屏幕方便很多
北京老城区我开了9个点, 效果不错
输出成tif 已经完成一大半

## 切片
先压缩jpg减小体积
然后用tile里带的代码压缩

## 经验
先看看图片分辨率再决定要不要georef