[English](readme.md) | **中文**

\>\>\> [回到索引](/readme-zh_cn.md)

## offline_whitelist_reforged

### 基本信息

- 插件 ID: `offline_whitelist_reforged`
- 插件名: OfflineWhitelistReforged
- 版本: 1.1.0
  - 元数据版本: 1.1.0
  - 发布版本: 1.1.0
- 总下载量: 346
- 作者: [Aimerny](https://github.com/Aimerny)
- 仓库: https://github.com/Aimerny/OfflineWhitelistReforged
- 仓库插件页: https://github.com/Aimerny/OfflineWhitelistReforged/tree/main
- 标签: [`管理`](/labels/management/readme-zh_cn.md)
- 描述: 离线服的白名单管理插件

### 插件依赖

| 插件 ID | 依赖需求 |
| --- | --- |
| [mcdreforged](https://github.com/Fallen-Breath/MCDReforged) | ^2.6.0 |

### 包依赖

| Python 包 | 依赖需求 |
| --- | --- |
| [mcdreforged](https://pypi.org/project/mcdreforged) | \>=2.6.0 |

```
pip install "mcdreforged>=2.6.0"
```

### 介绍

# OfflineWhiteListReforged

简单小巧的离线服白名单管理插件

## 使用方式
```
!!wr help - 显示帮助消息
!!wr list - 显示全部玩家的白名单
!!wr add <player> - 为<player>添加白名单
!!wr remove <player> - 移除<player>的白名单
!!wr on - 打开白名单
!!wr off - 关闭白名单
```

## 权限要求

使用MCDR的权限系统,权限要求由配置文件配置,默认如下
```json5
{
    "perms": {
        "on": 4, // owner
        "off": 4, // owner
        "list": 2, // helper
        "add": 3, // admin
        "remove": 3 //admin
    }
}
```
`help`: 无权限要求

`list`: helper及以上

`add`,`remove`: admin及以上

`off, on`: 仅owner(控制台权限等同于owner)

### 下载

> [!IMPORTANT]
> 使用插件之前，先阅读仓库中的 README。

| 文件 | 版本 | 上传时间 (UTC) | 大小 | 下载数 | 操作 |
| --- | --- | --- | --- | --- | --- |
| [OfflineWhitelistReforged-v1.1.0.mcdr](https://github.com/Aimerny/OfflineWhitelistReforged/releases/tag/v1.1.0) | 1.1.0 | 2024/08/02 18:28:34 | 5.16KB | 15 | [下载](https://github.com/Aimerny/OfflineWhitelistReforged/releases/download/v1.1.0/OfflineWhitelistReforged-v1.1.0.mcdr) |
| [OfflineWhitelistReforged-v1.0.0.mcdr](https://github.com/Aimerny/OfflineWhitelistReforged/releases/tag/v1.0.0) | 1.0.0 | 2023/06/15 09:30:39 | 4.31KB | 331 | [下载](https://github.com/Aimerny/OfflineWhitelistReforged/releases/download/v1.0.0/OfflineWhitelistReforged-v1.0.0.mcdr) |

