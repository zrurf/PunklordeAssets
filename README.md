# PunklordeAssets

**只要把它输入游戏文档，再白痴的玩家也能让朋克洛德的秩序崩盘瓦解。** 

## 简介
Punklorde的在线资产托管仓库。

## 目录结构

```bash
/data/          # 数据目录
- /MotionProfile/   # 运动预设
- /VirtualPath/     # 虚拟路径
/schema/        # 数据Schema（JSON Schema）
```

## 贡献数据
你可以参考已有的数据和Schema来贡献数据。所有数据可直接提PR。以下是注意事项。

### 运动轨迹
运动轨迹存储在`/data/MotionProfile`目录下。命名规则是`/data/MotionProfile/<school>/<place>/<name>.motion.json`，创建完成后，请在索引文件`/data/MotionProfile/index.json`中添加该运动预设。

> **注意** ：对于CQUPT的运动预设数据，你需要在`ext`字段（额外数据字段）中添加`placeName`和`placeCode`字段，分别表示地点名称和地点代码，可以由抓包获取。

### 虚拟路径
虚拟路径存储在`/data/VirtualPath`目录下。命名规则是`/data/VirtualPath/<school>/<place>/<name>.path.json`，创建完成后，请在索引文件`/data/VirtualPath/index.json`中添加该虚拟路径。

> **注意** ：轨迹坐标使用`GCJ02`坐标系。