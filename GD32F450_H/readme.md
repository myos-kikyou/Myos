这是GD32F450_H(大容量512k Flash以上)的完整运行环境分支。

本运行环境系统工程内的非共享(不提供给应用程序操作寄存器)驱动有SDRAM驱动、TFT驱动，在操作系统内初始化完成后无需应用程序再次设置，所以不提供给应用程序共享，应用程序操作SDRAM可以直接地址操作，操作TFT请使用Myos提供的显示模块的API操作。

本运行环境包含GPIO、ADC(通用)、SPI(部分)、CAN(部分)、UART、cache(软件)的基础驱动包以及完整的Myos系统文件，可以支持多工程开发模式。

本运行环境为官方标准推荐环境，使用外部16M晶振倍频至192M的运行主频，所以在使用中可以不对当前项做更改。

本运行环境包含USB作为主机读写U盘的应用程序插件，位于文件包内的对应官方USB的MSC主机类例程，并包含对应的从U盘更新HEX文件到芯片内的代码，更新文件规则请查看MSC工程的代码。
