
iterms2-rzsz配置
1.安装lrzsz
brew install lrzsz

2.将iterm2-send-zmodem.sh & iterm2-recv-zmodem.sh放到/usr/local/bin/

3.配置iterm2 Trigger
选择Profiles > Default > Advanced > Triggers > Edit
增加两项
# 发送 sz
Regular expression: rz waiting to receive.\*\*B0100 (注意这里是这样)
Action: Run Silent Coprocess
Parameters: /usr/local/bin/iterm2-send-zmodem.sh
# 接收 rz
Regular expression:\*\*B00000000000000
Action: Run Silent Coprocess
Parameters: /usr/local/bin/iterm2-recv-zmodem.sh



