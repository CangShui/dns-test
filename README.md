DNS 测试脚本介绍
这个脚本是一个用于测试公共DNS服务器性能的专业工具。它从指定来源获取DNS服务器列表，对多个测试域名进行解析速度和准确性测试，并生成Excel报告。
​

主要功能
脚本支持IPv4、IPv6或混合模式测试，使用多线程并发加速测试过程。核心测试包括DNS解析延迟统计（平均、最小、最大）和Google IP准确性验证。
​

从public-dns.info等来源获取DNS服务器列表

测试标准域名如google.com、facebook.com等

使用GeoIP数据库（可选）过滤Google IP

生成排序Excel报告，按性能指标排名

使用步骤
运行脚本后，按提示输入参数：选择DNS来源、IP模式（1:IPv4, 2:IPv6, 3:混合）、线程数、测试域名数量、延迟阈值等。脚本自动使用ThreadPoolExecutor并发测试，并显示进度条。
​

默认配置高效：64线程、3个测试域名、最小延迟10ms。测试完成后输出最佳DNS服务器信息和.xlsx文件。
​

依赖安装
脚本需预装以下Python库：

pandas, openpyxl（Excel处理）

dnspython（DNS解析）

tqdm（进度条）

requests（获取DNS列表）

maxminddb（可选，GeoIP查询）

使用pip安装：pip install pandas openpyxl dnspython tqdm requests maxminddb。
​

输出示例
Excel包含列：DNS服务器、平均延迟、最小/最大延迟、DNS名称。绿色高亮优质服务器。最佳DNS显示在控制台，如"最佳DNS：8.8.8.8, 平均15.2ms"。
​
