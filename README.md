
```
```
# 18comic-Download(禁漫天堂)
### python多线程下载禁漫天堂comic 18comic.vip

这是最初由 TG: [@Core_i0](https://t.me/Core_i0) 开发的项目。因被官方联系而终止。
我从中途fork后，进行了一些改动，修复了bug等。

经过我横向比较，当前18comic的爬虫程序有很多。其中有些甚至已经支持到了按标签爬虫。但是他们都没有使用多线程。其代码中有import process却没有实际使用，估计因为同样的原因。
我由于网络较差，很容易出现断流，因此不会放弃多线程下载。
当前版本中已启用了最大线程控制（默认最大数量20），_请不要随便增加最大线程数_，以免对服务器造成过大负载。_喝水不忘挖井人_


## 使用方法: 
1. 执行py文件。将会提示输入漫画地址。
可输入以下格式的网址：
```
https://18comic.org/album/232758/%E7%B4%97%E5%A4%9C%E8%88%87%E6%97%A5%E8%8F%9C-bang-dream-ezr%E5%80%8B%E4%BA%BA%E6%BC%A2%E5%8C%96-ryu-minbs-%E6%B5%81%E6%B0%91-%E7%B4%97%E5%A4%9C%E3%81%95%E3%82%93%E3%81%A8%E6%97%A5%E8%8F%9C%E3%81%A1%E3%82%83%E3%82%93-bang-dream
https://18comic.org/photo/232758/
```

2. 其他额外选项
接下来，程序可能会询问，“发现包含多个章节，是否全部下载”。此时按1全部下载的话，将会在各个章节目录下生成一个index.html，以连续方式阅读该章节漫画，并包含目录。（如果选0只下载当前章节的话，则不会生成index.html）

3.等待下载完成
程序将自动以所含漫画页数或最大线程限制的最小值开始下载。如果出现下载失败的图片页，程序将重复尝试。
该章节完成将自动开始下一章节的下载，直到全部章节完成。
全部章节完成后才会开始生成html文件。



## 更新历史：（原作者开发到2.2版本后终止）
```
2021/01/20更新:version：2.0 解决了下载图片被分割的问题,原网站对源图片资源进行了反爬虫，现在下载comic images正常了。
2021/01/31更新:version：2.1 增加下载多章节功能。
2021/02/08更新:version：2.2 将多进程下载改成多线程下载。解决多进程闪退，error，因过密集io操作使系统发生死锁问题。进一步提高下载速度。
2021/02/24更新:version：2.3 加入线程池和线程上限。多集下载自动生成含目录的html。修复了诸多bug
```


## 必看声明:
- 安装所需依赖库(直接运行脚本的话，打包好的exe可执行文件不需要安装依赖库)
```
pip3 install bs4 Pillow tqdm concurrent
```
