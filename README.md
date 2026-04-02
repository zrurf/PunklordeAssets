# PunklordeAssets

**只要把它输入游戏文档，再白痴的玩家也能让朋克洛德的秩序崩盘瓦解。** 

## 简介
Punklorde的在线资产托管仓库。

## 目录结构

```bash
/data/              # 数据目录
- /Calendar/        # 校历数据
- /MotionProfile/   # 运动预设
- /VirtualPath/     # 虚拟路径
/schema/            # 数据Schema（JSON Schema）
```

## ⚠ 破坏性改动警告
本仓库的数据集随着[**Punklorde**](https://github.com/zrurf/Punklorde)主软件的更新而更新，因此schema会有改动，而破坏性改动可能会导致某一提交前的**Punklorde**构建失效，请参阅以下破坏性改动，以便迁移到新版本**Punklorde**。

> **当前Punklorde最新提交与本仓库兼容，无重大破坏性改动**

## 贡献数据
你可以参考已有的数据和Schema来贡献数据。所有数据可直接提PR。以下是注意事项。

### 校历数据
校历数据存储在`/data/Calendar`目录下。命名规则是`/data/Calendar/<school>/<semester>.semester.json`，`semester`为学期编号，需要符合以下格式:

学期编号格式为`<year><semester>`，其中`year`为学年（**注意不是自然年**），`semester`为学期编号，如`20251`表示2025-2026学年秋季第一学期。

### 运动轨迹
运动轨迹存储在`/data/MotionProfile`目录下。命名规则是`/data/MotionProfile/<school>/<place>/<name>.motion.json`，创建完成后，请在索引文件`/data/MotionProfile/index.json`中添加该运动预设。并且在`catalog.json`中添加目录索引。

> **注意** ：对于CQUPT的运动预设数据，你需要在`ext`字段（额外数据字段）中添加`placeName`和`placeCode`字段，分别表示地点名称和地点代码，可以由抓包获取。

### 虚拟路径
虚拟路径存储在`/data/VirtualPath`目录下。命名规则是`/data/VirtualPath/<school>/<place>/<name>.path.json`，创建完成后，请在索引文件`/data/VirtualPath/index.json`中添加该虚拟路径。并且在`catalog.json`中添加目录索引。

> **注意** ：国内轨迹坐标请使用`GCJ02`坐标系。