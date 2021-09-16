# <p align="center">HeyTap</p>

## 免责声明
- 本仓库发布的HeyTap项目中涉及的任何脚本，仅用于测试和学习研究，禁止用于商业用途，不能保证其合法性，准确性，完整性和有效性，请根据情况自行判断.

- 所有使用者在使用HeyTap项目的任何部分时，需先遵守法律法规。对于一切使用不当所造成的后果，需自行承担.对任何脚本问题概不负责，包括但不限于由任何脚本错误导致的任何损失或损害.

- 如果任何单位或个人认为该项目可能涉嫌侵犯其权利，则应及时通知并提供身份证明，所有权证明，我们将在收到认证文件后删除相关文件.

- 任何以任何方式查看此项目的人或直接或间接使用该HeyTap项目的任何脚本的使用者都应仔细阅读此声明。本人保留随时更改或补充此免责声明的权利。一旦使用并复制了任何相关脚本或HeyTap项目的规则，则视为您已接受此免责声明.

您必须在下载后的24小时内从计算机或手机中完全删除以上内容.

> 您使用或者复制了本仓库且本人制作的任何脚本，则视为`已接受`此声明，请仔细阅读



## 环境

[Python3](https://www.python.org/) >= 3.6.8

## 已实现功能
* [x] 每日签到
* [x] 每日浏览商品任务
* [x] 每日分享商品任务
* [x] 每日点推送任务
* [x] 赚积分活动
* [x] 天天积分翻倍
* [x] 天天领现金任务列表
* [x] 天天领现金定时红包
* [x] 早睡打卡
* [x] 积分大作战
* [x] 发信功能(太懒了，只实现一个)

## 文件说明
```text
│  HeyTap.py         # 欢太商城一键脚本
│  timingCash.py     # 欢太定时红包，建议配合Linux定时系统Crontab
|  dailyCash.py      # 每日现金任务
│  CheckInEarly.py   # 欢太商城，早睡报名或打卡，建议配合Linux定时系统Crontab
│  PointsBattle.py   # 积分大作战
|  config.py         # 账号信息
|  README.md         # 说明文档
```

## Windows
略

## Linux
```bash
yum install python3 -y

yum install git -y

git clone https://ghproxy.com/https://github.com/Mashiro2000/HeyTap.git   # 国内git较慢，故添加代理前缀

cd HeyTap

vi config.py
```

### 配置信息
编辑 `config.py`

#### 管理员配置
```json
admin = {
    "pushGroup" :{
        "pushToken": "",                            # Push Plus Token
        "pushTopic": ""                             # Push Plus群组编码
    },
    "mask":['', '']                                 # 屏蔽某些脚本的通知功能，如:['HeyTap','dailyCash']
}
```

#### 用户信息
```json
accounts = [
    {
        'user' : '',    # 备注
        'CK' : '',      # 用户环境变量 Cookie
        'UA' : ''       # 用户环境变量 User-Agent
    },
    {
        'user' : '',    # 备注
        'CK' : '',      # 用户环境变量 Cookie
        'UA' : ''       # 用户环境变量 User-Agent
    }
]
```

#### 环境变量
- CK和UA信息需自行抓包，欢太商城 -> 我的 -> 任务中心 -> 领券中心
- 抓包地址:`https://store.oppo.com/cn/oapi/users/web/checkPeople/isNewPeople`

#### 其它帮助
[crontab 帮助文档](https://www.runoob.com/w3cnote/linux-crontab-tasks.html)
