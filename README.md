<img width="1390" height="1426" alt="image" src="https://github.com/user-attachments/assets/95e77b7f-29eb-4a53-bd92-e6187c1d17f9" />



主要功能
脚本支持IPv4、IPv6或混合模式多线程并发测试DNS服务器可用性、延迟、污染情况。
​

依赖安装：
pip install pandas openpyxl dnspython tqdm requests maxminddb

打包成exe：
pyinstaller --onedir --console --name "DNSTest" --distpath ./dist --icon "NONE" --clean dnstest.py
