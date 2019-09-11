# LPngOptimizer

1 需要安装pngquant因为此程序对于8a,8b的输入参数需要用pngquant

sudo apt install pngquant

2 需要安装ImageMagick因为此程序对于16a,16b的输入参数需要用convert

sudo apt-get install imagemagick

3 使用 首先编译

javac LPngOptimizer.java

chmod +x zopflipng

使用

java LPngOptimizer 8a gfmn.png

java LPngOptimizer 8b gfmn.png

java LPngOptimizer 16a gfmn.png

java LPngOptimizer 16b gfmn.png

java LPngOptimizer none gfmn.png

使用时请保证zopflipng在同目录下并给予可执行权限

你会发现你拥有了一个超越limitPNG的神器。

参数

8a 当发现使用pngquant效果太差的时候使用rgb555方式FloydSteinberg图片

8b 直接使用pngquant输出

16a 使用rgb555方式FloydSteinberg方法抖动图片

16b 使用rgb565方式FloydSteinberg方法抖动图片

nono 不做预处理直接使用zopflipng优化图片

效果 压缩 gfmn.png
src 275781 (269K)
8a 187313 (182K)
8b 74085 (72K)
16a 187313 (182K)
16b 204561 (199K)
none 272753 (266K)
