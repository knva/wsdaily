## Go 版本武神活跃号日常

- 自动师门
- 自动副本(进出小树林)
- 追捕扫荡
- 领取签到奖励、节日奖励  
- 结束自动挖矿
- 支持定时、多账号

### 使用方法
    去[releases](https://github.com/BenZinaDaze/wsdaily/releases)下载最新编译好的程序,修改配置文件,开箱即用。

### 配置

    ./conf.yaml
    cron 定时  Cron语法
    logins 账号组
        -login 账号1
         password 密码1
         server 区 1 2 3 4 99 100
        -login 账号2
         password 密码2
         server 区 1 2 3 4 99 100

### 自行编译

#### Linux
    示例:
        make build os=windows arch=amd64
    参数:
        os：操作系统 默认windows
            可选参数：darwin,freebsd,linux,windows
        arch：架构 默认amd64
            可选参数：386,amd64,arm
    例如：
        编译MAC可执行程序
        make build os=darwin
        编译linux arm可执行程序
        make build os=linux arch=arm
#### Win
    自行查找GOLANG在windowns下如何交叉编译