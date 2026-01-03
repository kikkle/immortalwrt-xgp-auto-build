# 正在开发与调试中，小白误用

第一次使用前请先阅读 [README.md](https://github.com/zzzz0317/immortalwrt-xgp-auto-build/blob/main/README.md)

通过转接板连接的 PCIe 5G 模块在刷机后需要断电（直接拔DC插头，拔市电那头要多等几秒电容放电）一次，否则大概率找不到模块，转接板硬件原因导致模块在重启时不能正常下电。

MBIM 模式若无法正常拨号请在 QWRT模组管理 -> 拨号总览 -> 模组配置 -> 高级设置 中指定 APN，详见 [QModem Issues #129](https://github.com/FUjr/QModem/issues/129)。第一次启动检测到 T99W373 模块时会自动禁用 QModem 拨号以防止产生巨量日志（MBIM 模式自动拨号找不到 APN），请您在适当调整设置后手动启用。