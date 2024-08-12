**English** | [中文](readme-zh_cn.md)

\>\>\> [Back to index](/readme.md)

## kookin

### Basic Information

- Plugin ID: `kookin`
- Plugin Name: Kook In
- Version: 0.1.6
  - Metadata version: 0.1.6
  - Release version: 0.1.6
- Total downloads: 38
- Authors: [Aimerny](https://github.com/Aimerny)
- Repository: https://github.com/Aimerny/KookIn
- Repository plugin page: https://github.com/Aimerny/KookIn/tree/main
- Labels: [`Information`](/labels/information/readme.md), [`Management`](/labels/management/readme.md)
- Description: A MCDR kook useful plugin

### Dependencies

| Plugin ID | Requirement |
| --- | --- |
| [kook_api](/plugins/kook_api/readme.md) | ^0.1.3 |
| [online_player_api](/plugins/online_player_api/readme.md) | ^1.0.0 |

### Requirements

| Python package | Requirement |
| --- | --- |

### Introduction

# KookIn

使用[KookAPI](https://github.com/Aimerny/KookAPI)实现的MCDR服务器管理插件

> 该插件的功能移植自[QQ Chat](https://github.com/AnzhiZhang/MCDReforgedPlugins/tree/master/src/qq_chat)插件

## 功能介绍

### MCDR端

1. 发送消息到指定Kook频道组
2. 将所有MC的聊天消息同步到指定Kook频道组中

### Kook端

1. 查看MC服务器中在线玩家列表
2. 离线时向服务器中发送消息
3. ~~管理服务器白名单(可直接通过cmd进行管理)~~
4. 远程执行服务端指令(仅管理员可用)
5. 远程执行MCDR指令(仅管理员可用)

## 开始
由于Kook没有对频道的唯一ID显式提供, 我们需要经过一些准备工作才能拿到对应的频道ID
1. 启动MCDR服务器并加载插件
2. 调用`!!kkchans <关键字>`指令获取机器人加入的所有频道名称与频道ID
3. 根据频道ID配置插件频道信息,重新加载配置

## 配置项

`$MCDR/config/kookin/conf.json`

| 配置项               | 配置说明       | 类型                 | 示例               |
| ----------------- | ---------- | ------------------ | ---------------- |
| admin_channel     | 服务器管理频道    | Array[channelInfo] | -                |
| public_channel    | 服务器公共频道    | Array[channelInfo] | -                |
| sync_chat_channel | 服务器消息同步频道  | Array[channelInfo] | -                |
| channel_name      | 频道名称备注     | string             | 频道A              |
| channel_id        | 频道ID       | string             | 获取方式见上           |
| admins            | 管理员        | Array[string]      | ["Aimerny#0476"] |
| server_name       | Kook展示服务器名 | string             | Survival         |

> 1. 只有使用`!!kk` 指令的消息才会被发送到服务器公共频道中
> 2. 在服务器公共频道中的消息只有使用/mc指令的消息才会发送到服务器中
> 3. 所有游戏内消息都会被发送至消息同步频道中,在消息同步频道中发送任何消息也会同步到游戏中
> 4. 在admins列表中的管理员发送离线消息时,游戏内为绿色,普通用户为灰色

## 指令预览

### MCDR端指令

```
!!kk <msg> #发送消息到指定Kook服务器
!!kkchans <search_key> #搜索当前机器人加入的频道Id,search_key为名称过滤
```

```
# kkchans 返回格式说明
[${服务器名称}]=>[${频道名称}]=>[${频道id}]
```

### Kook端指令

```
/help      =>   查询指令
/bind      =>   成员绑定
/whitelist =>   白名单管理
/list      =>   在线玩家列表
```

#### 绑定相关

```
/bind <mc_id>         => 绑定MC
/bind clear @Kook成员 => 清除指定用户绑定信息(管理员可用)
/bind list            => 查看已绑定列表(管理员可用)
```

#### 离线消息

```
/mc <msg> => 发送消息到服务器(需要先绑定账号)
```

#### 执行服务器指令

```
/cmd <command> => 执行服务器指令(管理员可用) # 例如: /cmd ban Aimerny | /cmd whitelist add Aimerny
/mcdr <mcdr_cmd> => 执行mcdr指令(管理员可用) # 例如: /mcdr !!kk 这是通过kook令服务器发送的消息 | /mcdr !!pb make 存档
```

### Download

> [!IMPORTANT]
> Read the README file in plugin repository before using it.

| File | Version | Upload Time (UTC) | Size | Downloads | Operations |
| --- | --- | --- | --- | --- | --- |
| [KookIn-v0.1.6.mcdr](https://github.com/Aimerny/KookIn/releases/tag/v0.1.6) | 0.1.6 | 2024/07/24 06:38:28 | 64.71KB | 9 | [Download](https://github.com/Aimerny/KookIn/releases/download/v0.1.6/KookIn-v0.1.6.mcdr) |
| [KookIn-v0.1.5.mcdr](https://github.com/Aimerny/KookIn/releases/tag/v0.1.5) | 0.1.5 | 2024/05/27 13:41:23 | 12.13KB | 21 | [Download](https://github.com/Aimerny/KookIn/releases/download/v0.1.5/KookIn-v0.1.5.mcdr) |
| [KookIn-v0.1.4.mcdr](https://github.com/Aimerny/KookIn/releases/tag/v0.1.4) | 0.1.4 | 2024/05/26 09:59:34 | 10.8KB | 3 | [Download](https://github.com/Aimerny/KookIn/releases/download/v0.1.4/KookIn-v0.1.4.mcdr) |
| [KookIn-v0.1.3.mcdr](https://github.com/Aimerny/KookIn/releases/tag/v0.1.3) | 0.1.3 | 2024/05/26 05:27:48 | 10.84KB | 2 | [Download](https://github.com/Aimerny/KookIn/releases/download/v0.1.3/KookIn-v0.1.3.mcdr) |
| [KookIn-v0.1.2.mcdr](https://github.com/Aimerny/KookIn/releases/tag/v0.1.2) | 0.1.2 | 2024/05/13 16:29:15 | 9.6KB | 1 | [Download](https://github.com/Aimerny/KookIn/releases/download/v0.1.2/KookIn-v0.1.2.mcdr) |
| [KookIn-v0.1.0.mcdr](https://github.com/Aimerny/KookIn/releases/tag/v0.1.0) | 0.1.0 | 2024/05/11 16:26:56 | 9.08KB | 2 | [Download](https://github.com/Aimerny/KookIn/releases/download/v0.1.0/KookIn-v0.1.0.mcdr) |

