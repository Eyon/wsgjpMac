# wsgjpMac
曲线解决管家婆云ERP进销存版在 Mac 系统中不能打印的问题。


## 需求：

在 Mac 系统中能够打印管家婆云 ERP 进销存版生成的单据，并且自动将单据截图同步到 Dropbox(方便在微信上给客户发送单据)。



## 实现原理：

将管家婆云 ERP 进销存版生成的单据导出为 Excel 数据到用户下载目录，程序搜索用户下载目录内最新的文件（刚刚导出的 excel 数据表），读取该 excel 中的数据并写入写入HTML生成一个网页，最后程序打开网页自动截图保存到 Dropbox 特定目录。

当然，该脚本在装有 Python 的 Windows 平台同样可用。


## 使用流程：

### 在管家婆单据页面点击打印——导出数据到 Excel

![](http://ww1.sinaimg.cn/large/6fefdebdly1fqsmbb6dt1j20wa0imn1u.jpg)

执行这一步操作后，会自动在用户默认下载文件夹中生成一个最新的 excel 文件。

### 在终端运行程序 python gjp
