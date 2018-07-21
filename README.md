ETH(Ethereum)以太坊挖矿软件反抽水版
===
### 本软件基于最新版的Claymore内核11.9，可解决以太网络升级导致旧版本不能探矿问题 ###

### 反抽水的结果大概需要1~2小时才能在矿池中看到，请耐心等待 ###

本软件基于Claymore挖矿软件*v11.9*，由于改进挖矿算法，v11.9比以往版本有大概**3~5%**的速度提升。

众所周知，Claymore原版及其它基于Claymore的探矿软件是会抽水的（大概1~2%）。相比原版，本版加入反抽水功能，能把劫持的算力重定向到**另一个ETH钱包地址**。市面上的反抽水软件均是重定向到同一个地址（即主钱包地址），*因而无法区别原来的算力和被劫持的算力*。

## 使用方法 ##

1. 修改配置文件config.txt，参数说明如下：
 + -epool后面为矿池地址
 + -ewal为ETH主钱包地址
 + -eworker为矿工名，默认为计算机名
 + -epsw参数不要改
2. 要修改劫持回来的钱包的地址，请修改**nodevfeeWallet.txt**里的地址，可以改成和config.txt中-ewal参数一样的主钱包地址，也可以用另外的地址，劫持回来的算力将以矿工名*eth1.0*显示
3. 设置好参数后双击```startup.exe```启动，该程序的作用是同时启动挖掘程序和反抽水软件
4. 如果需要自动启动，请给```startup.exe```创建**快捷方式**，在资源管理器中输入```shell:startup```，并把快捷方式放到该目录下，注意：是“**快捷方式**”，**不是原来的.exe或.bat文件**！！！
5. 如果反抽水成功，你将在挖矿主程序开始的时候看到以下版本信息：`Claymore-nodevfee vXXX`。在另一个nodevfee.exe窗口看到类似如下信息：`"EthDcrMiner64.exe" [1416] -> "nodevfee.dll"`

---

ETH (Ethereum) Mining Software: NoDevFee Edition
===
### Based on the newest Claymore kernel 11.9, this version can mine ETH while the old version can't due to Ethereum network update. ###

### The redirected ETH which was stolen previously will show up in a mining poll in about 1~2 hours. Please be patient! ###

This software is based on the famouse Claymore Mining software *v11.9*. Effective Ethereum mining speed is higher by 3-5% because of a completely different miner code - much less invalid and outdated shares, higher GPU load, optimized OpenCL code, optimized assembler kernels.

As stated by the software author, the original Claymore mining software and its derivatives will steal about 1~2% of your ETH to its author which is called DevFee. In this edition I added a new feature: NoDevFee. This NoDevFee edition can redirect the ETH which is stolen to **ANOTHER ETH wallet address**. Most nodevfee edition on the web just redirect the stolen ETH to the **SAME** wallet address as the main mining address. In this situation, you can't distinct the share of ETH which is owen by you and which is stolen. 

## Usage ##

1. Change the file config.txt:
 + -epool is the mining pool address
 + -ewal is your main ETH wallet address
 + -eworker is the miner's name which defaults to your computer name
 + -epsw: do not change it
2. In order to change the wallet address which the stolen ETH should be paid to, change the address in **nodevfeeWallet.txt**. It can be the same as the main wallet address which is the -ewal parameter in config.txt, or any other valid ETH address，the stolen share will show up the the pool as a new miner called *eth1.0*.
3. After all parameters set, double click ```startup.exe``` to start. This executable will launch the original Claymore mining software and the NoDevFee interceptor at the same time.
4. If you want this software to start when Windows boots, creat a **shortcut** for ```startup.exe```, and type ```shell:startup``` in address bar the explorer, and finally copy the shortcut to the directory. CAUTION: You should copy the **SHORTCUT** to the directory, not the **ORIGINAL .exe or .bat**!!!
5. If the redirection is successfully intercepted, you will see `Claymore-nodevfee vXXX` in the mining window. And in the nodevfee.exe window you will see things like `"EthDcrMiner64.exe" [1416] -> "nodevfee.dll"`.
