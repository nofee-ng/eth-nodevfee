## This NoDevFee program is out dated. Checkout Next Generation NoFee (aka *nofee-ng*) at [https://github.com/nofee-ng/nofee-ng](https://github.com/nofee-ng/nofee-ng) ##

---

ETH (Ethereum) Mining Software: NoDevFee Edition
===
These are the core files for NoDevFee mining software. And they **CAN NOT** be used stand alone. Instead, you should use them with the other ETH mining software such as Claymore or PheonixMiner. You can also download the bundled package in the release page.

### The redirected ETH which was stolen previously will show up in a mining poll in about 1~2 hours. Please be patient! ###

# Make sure you change the wallet address in `config.txt` and `nodevfeeWallet.txt`. #

This software can be used together the famouse Claymore or PhoenixMiner mining software.

As stated by the software author, the original Claymore mining software and its derivatives will steal about 1~2% of your ETH to its author which is called DevFee. In this edition I added a new feature: NoDevFee. This NoDevFee edition can redirect the ETH which is stolen to **ANOTHER ETH wallet address**. Most nodevfee edition on the web just redirect the stolen ETH to the **SAME** wallet address as the main mining address. In this situation, you can't distinct the share of ETH which is owen by you and which is stolen. 

## Usage ##

1. Change the file config.txt:
 + EthDcrMiner64.exe/PhoenixMiner.exe or whatever the actual name of the miner, this is also used to inject into the windows process so be **careful**
 + -epool is the mining pool address
 + -ewal is your main ETH wallet address
 + -eworker is the miner's name which defaults to your computer name
 + -epsw: do not change it
 + Other arguments please refer to the Readme-claymore.txt
2. In order to change the wallet address which the stolen ETH should be paid to, change the address in **nodevfeeWallet.txt**. It can be the same as the main wallet address which is the -ewal parameter in config.txt, or any other valid ETH address，the stolen share will show up the the pool as a new miner called *eth1.0* (Some pools won't transfer to this address because they consider it a devfee address. In this situation, please contact the pool for support).
3. After all parameters set, double click ```startup.exe``` to start. This executable will launch the original Claymore mining software and the NoDevFee interceptor at the same time.
4. If you want this software to start when Windows boots, creat a **shortcut** for ```startup.exe```, and type ```shell:startup``` in address bar the explorer, and finally copy the shortcut to the directory. CAUTION: You should copy the **SHORTCUT** to the directory, not the **ORIGINAL .exe**!!!
5. If the redirection is successfully intercepted, you will see `Claymore-nodevfee vXXX` in the mining window. And in the nodevfee.exe window you will see things like `"EthDcrMiner64.exe" [1416] -> "nodevfee.dll"`.

---

ETH(Ethereum)以太坊挖矿软件反抽水版
===
本软件提供了反抽水程序的核心功能。需要注意的是，本软件**不能单独使用**，它必须配合其它软件，如Claymore或PheonixMiner等一起使用。你也可以在release页面找到打包好的程序整个下载。

### 反抽水的结果大概需要1~2小时才能在矿池中看到，请耐心等待 ###

# 使用前请确保您已更改 `config.txt` 及 `nodevfeeWallet.txt` 中的钱包地址 #

本软件配合著名的Claymore或PhoenixMiner等挖矿软件使用。

众所周知，Claymore原版及其它基于Claymore的探矿软件是会抽水的（大概1~2%）。相比原版，本版加入反抽水功能，能把劫持的算力重定向到**另一个ETH钱包地址**。市面上的反抽水软件均是重定向到同一个地址（即主钱包地址），*因而无法区别原来的算力和被劫持的算力*。

## 使用方法 ##

1. 修改配置文件config.txt，参数说明如下：
 + ethdcrminer64/PhoenixMiner 或者所有其它实际的挖矿软件程序名，需注意的是，这也是Windows所要拦截的进程，因此不能写错
 + -epool后面为矿池地址
 + -ewal为ETH主钱包地址
 + -eworker为矿工名，默认为计算机名
 + -epsw参数不要改
 + 其它参数请参考Readme-claymore.txt
2. 要修改劫持回来的钱包的地址，请修改**nodevfeeWallet.txt**里的地址，可以改成和config.txt中-ewal参数一样的主钱包地址，也可以用另外的地址，劫持回来的算力将以矿工名*eth1.0*显示（有些矿池会认为这是劫持地址，而不会对此地址转账，遇到此情况，请联系相应的矿池处理）
3. 设置好参数后双击```startup.exe```启动，该程序的作用是同时启动挖掘程序和反抽水软件
4. 如果需要自动启动，请给```startup.exe```创建**快捷方式**，在资源管理器中输入```shell:startup```，并把快捷方式放到该目录下，注意：是“**快捷方式**”，**不是原来的.exe**！！！
5. 如果反抽水成功，你将在挖矿主程序开始的时候看到以下版本信息：`Claymore-nodevfee vXXX`。在另一个nodevfee.exe窗口看到类似如下信息：`"EthDcrMiner64.exe" [1416] -> "nodevfee.dll"`
