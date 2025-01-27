
```
 __    __     __  __     ______     ______   ______     ______     __
/\ "-./  \   /\ \_\ \   /\  ___\   /\__  _\ /\  __ \   /\  __ \   /\ \
\ \ \-./\ \  \ \____ \  \ \___  \  \/_/\ \/ \ \ \/\ \  \ \ \/\ \  \ \ \____
 \ \_\ \ \_\  \/\_____\  \/\_____\    \ \_\  \ \_____\  \ \_____\  \ \_____\
  \/_/  \/_/   \/_____/   \/_____/     \/_/   \/_____/   \/_____/   \/_____/
```

<div align="center"><h1> 真寻适配版 - mysTool - 米游社辅助工具插件</div>

<div align="center">
  <a href="https://github.com/ayakasuki/nonebot_plugin_mystool" target="_blank">
    <img alt="CodeFactor" src="https://www.codefactor.io/repository/github/ayakasuki/nonebot_plugin_mystool/badge?style=for-the-badge">
  </a>
  <a href="https://github.com/ayakasuki/nonebot-plugin-mystool" target="_blank">
    <img alt="最新发行版" src="https://img.shields.io/github/v/release/Aayakasuki/nonebot_plugin_mystool?logo=python&style=for-the-badge">
  </a>
  <a href="https://github.com/ayakasuki/nonebot-plugin-mystool" target="_blank">
    <img alt="最后提交" src="https://img.shields.io/github/last-commit/Ayakasuki/nonebot_plugin_mystool?style=for-the-badge">
  </a>
</div>

**版本 - v1.0.0**
 ```
📣 更新：更新到v1.0.0
    - 修复Windows, macOS多进程生成商品图片失败的问题 [#120](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/120) by @Night-stars-1
    - 支持使用人机验证打码平台处理人机验证任务 [#119](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/119) by @Night-stars-1
    - 原神便笺获取失败时更换为使用米游社iOS小组件API获取 [#119](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/119) by @Night-stars-1
    - 修复原神便笺和讨论区签到可能因为DS无效而失败的问题
    - 大量的代码重构，包括米游社API的客户端实现、用户数据相关、插件配置相关、API相关数据模型
    - 从显示用户账号绑定的手机号改为显示账号的米游社ID
    - 设置、兑换计划功能支持群聊使用
    - 登陆绑定只需要进行一次短信验证
    - 用户数据文件、插件配置文件 **格式更新，与 v1.0.0 之前的版本不兼容**
    - 修复添加兑换任务时出现的UID不存在错误
    - 修复商品图片生成完才发出后台正在生成提示的问题
    - 异常捕获更加准确
    - 改进了一些文本
📣 更新：更新到v0.2.9
📣 更新：
    - 每日签到、米游币任务执行时间在用户配置的基础上增加随机延迟
    - 修复大别野频道每日任务、签到执行失败的问题
    - 新增崩坏：星穹铁道的游戏签到
📣 更新：支持崩坏:星穹铁道的商品兑换。重新增加阻塞，否则真寻AI会跟着回复。
📣 更新：0.2.5更新
    - 修复重写配置文件 `pluginConfig.json` 不生效的问题
    - 修复单账户情况下无法增删兑换计划的问题
    - 修复 `/兑换` 命令可能与其他插件命令冲突的问题，同时 [🔗用法变更](增加删除兑换计划)
    - 精简接收的命令
    - 更正 `device_save` "设备保存" 日志文本的错误
📣 更新：修复多用户情况下登录操作会导致用户数据错位的问题([#18])
📣 更新：0.2.4更新-
        - 修复旧版config.py中目录与模块名称不一致导致报错
        - 适配真寻configs/config.yaml。主要设置迁移进config.yaml进行编辑。
        - 提醒：千万不要没事修改目录名称。如需更改，config.py中需要进行相应模块名更改。
```

### 功能和特性

- 短信验证登录，免抓包获取 Cookie
- 自动完成每日米游币任务
- 自动进行游戏签到
- 可制定米游币商品兑换计划，到点兑换
- 可支持多个 QQ 账号，每个 QQ 账号可绑定多个米哈游账户
- QQ 推送执行结果通知

### 使用说明

* 请在<mark>ENV.DEV</mark>文件修改<mark>SESSION_EXPIRE_TIMEOUT</mark>，这关乎你的选项超时时间。

* 可直接BOT在根目录运行代码安装
  
  ```
  git clone https://github.com/ayakasuki/nonebot_plugin_mystool.git ./extensive_plugin/nonebot_plugin_mystool
  ```

* 安装后请安装依赖！
 
  1.poetry模式：在BOT根目录 ```cd ./extensive_plugin/nonebot_plugin_mystool``` 后进行```poetry install```
 
  2.普通python运行 ：自行转换```pyproject.toml```为```requirements.txt```后```pip install -r requirements.txt```

* 第一次运行后，务必进入真寻BOT的config文件夹下的config.yaml进行编辑，否则将默认```米游社小助手帮助``` 进行触发命令！

### 

### 📖 插件具体使用说明

请查看 -> [🔗Wiki 文档](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki)

### ❓ 获取插件帮助信息

#### 插件命令

```
米游社小助手帮助
```

> ⚠️ 注意 此处没有使用 [🔗 插件命令头](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki/Configuration-Config#command_start)