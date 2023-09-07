## intro
gpu硬解正常,能睡眠(显示器是关了的,但是没确定是否真的睡眠)&唤醒

1. [opencore config.plist checker](https://sanitychecker.ocutils.me/)
2. open core 启动选择系统界面，按`space`可以选择external U盘，引导
3. 需要对想要安装macos的磁盘空间使用diskgenius格式化为APFS（uuid，gpt）
4. diskgenius也可以扩展ebf分区，数据保存镜像（记下uuid？不确定），删除ebf、mbr（windows用来标记用的，里面无内容），然后选择重建erf，save修改。然后导入保存的ebf镜像
5. 使用diskgenius新增ueif entry,指向oc里的openXXX.
7. https://github.com/osxfuse/osxfuse/wiki/NTFS-3G

## mouse lag
1. `Karabiner-Elements`问题,在`devices`中关闭鼠标对应events的监控即可.
2. 另外一个是尝试接入USB2插口.
3. 最重要的是显卡要没问题.

## rx550 spoofling
1. 参考 https://github.com/moqsien/hackintosh_p310s_b360_i5_10400f_rx550_lexa/blob/main/files/docs/Readme_CN.md
2. 其中显卡slot name可以从Hackintool中获取,参考https://www.a7mac.com/1037.html
3. config.plist中的`boot-args`中要加上`-radcodec` 支持硬解
