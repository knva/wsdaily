<!--
 * @Description: 
 * @Author: benz1
 * @Date: 2022-01-04 09:11:11
 * @LastEditTime: 2022-01-05 15:28:39
 * @LastEditors: benz1
 * @Reference: 
-->
## Go 版本武神活跃号日常

- 自动师门
- 自动副本(进出小树林)
- 追捕扫荡
- 领取签到奖励、节日奖励  
- 结束自动挖矿
- 支持定时、多账号
- 支持TG,PUSHPLUS推送

### 使用方法

去 [releases](https://github.com/BenZinaDaze/wsdaily/releases) 下载最新编译好的程序,修改配置文件。

    1. 定时启动
        ./wsdaily
    2. 立即运行一次
        ./wsdaily --mode run

### 配置

./conf.yaml

    # Crontab 定时
    cron: 0 30 6,14,22 * * *
    # 多账号,注意缩进,不需要单双引号. 区 1 2 3 4 测试为99
    # pushplus推送 http://www.pushplus.plus/ 获取  (非必需,但请不要乱填)
    pushplus_token: xxxxxxx
    # api token 通过 BotFather 获取  (非必需,但请不要乱填)
    pushtg_token: xxxxx
    # 用户id 通过 IDBot 获取  (非必需,但请不要乱填)
    pushtg_chat_id: xxxxxx
    # 黑名单 在名单内跳过日常,英文逗号分隔
    blacklist: 张三,李四
    logins:
        - login: xxxxx
          password: xxxxxx
          server: 1
        - login: xxxxx
          password: xxxxx
          server: 2

### 自行编译

#### Linux

    方法1. 安装go,自行编译.
    方法2. 安装go,使用make编译
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