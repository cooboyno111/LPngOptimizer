# LPngOptimizer

8a，16a，16b属于弱有损压缩，8a模式基本能给予有限体积内最好的png画质。

8b有损压缩 效果也不差体积小。

8c强有损压缩 体积最小。

none模式为无损压缩。

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

8a 当发现使用pngquant效果太差的时候使用rgb555方式FloydSteinberg方法抖动图片

8b 直接使用pngquant输出

8c 限定为64色调色板输出，某些PNG极限压缩软件大概就是这个模式

16a 使用rgb555方式FloydSteinberg方法抖动图片，此模式能成为很好的png32/24的代替品，体积比16b稍小。

16b 使用rgb565方式FloydSteinberg方法抖动图片，此模式能成为很好的png32/24的代替品，大量的手机和电脑屏幕色彩分量仅为6bit。

none 不做预处理直接使用zopflipng优化图片

效果 压缩 gfmn.png

src 275781 (269K)

8a 187313 (182K)

8b 74085 (72K)

16a 187313 (182K)

16b 204561 (199K)

none 272753 (266K)

拿limitPNG放在首页的三张测试图举例

vuelogo.png 8a（11460B-3498B）vs limitPNG （11460B-7898B）

ss.png 8a（338566B-274615B）vs limitPNG （338566B-286711B）

熊猫图 8c 9302B
