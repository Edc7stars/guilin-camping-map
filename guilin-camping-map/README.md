# 🏕️ 桂林露营地电子导览地图

一个精美的桂林市露营地导览地图网页应用，支持地图浏览、营地搜索、行政区筛选等功能。

## 📁 项目结构

```
guilin-camping-map/
├── index.html              # 主地图页面
├── data/
│   ├── camps.json          # 营地数据
│   └── regions.json        # 行政区配置
├── assets/
│   └── images/
│       └── map-main.png    # 地图图片
├── admin/
│   └── tools.html          # 数据管理工具
├── css/                    # 样式文件（预留）
└── README.md
```

## 🚀 快速开始

### 本地运行

1. **方法一：直接打开**
   - 双击 `index.html` 文件在浏览器中打开

2. **方法二：使用本地服务器**
   ```bash
   # 如果有 Python
   python -m http.server 8000
   
   # 如果有 Node.js
   npx serve
   ```
   然后访问 `http://localhost:8000`

3. **方法三：VS Code Live Server**
   - 使用 VS Code 的 Live Server 插件打开

## ✨ 功能特点

### 🗺️ 地图浏览
- 支持鼠标滚轮缩放、拖拽移动
- 支持触摸屏手势操作
- 平滑惯性滚动效果
- 双击标记可放大查看

### 🔍 营地搜索
- 左侧列表实时显示营地信息
- 支持按名称、类型搜索
- 点击卡片查看详细信息

### 🏛️ 行政区筛选
- 顶部行政区快捷按钮
- 点击行政区自动定位到该区域
- 显示行政区标记和名称

### 📊 集群显示
- 营地密集区域自动聚合
- 显示集群数量
- 点击集群可放大查看

## 📝 数据管理

### 管理工具 (admin/tools.html)

访问管理工具可以进行以下操作：

1. **导入数据**
   - 上传 JSON 文件
   - 粘贴 JSON 数据
   - 支持拖拽上传

2. **编辑营地**
   - 修改营地信息
   - 更新坐标
   - 调整所属行政区

3. **删除营地**
   - 单个删除
   - 批量管理

4. **导出数据**
   - 导出完整 JSON 数据
   - 下载导入模板

## 📋 数据格式

### camps.json

```json
{
  "version": "1.0",
  "lastUpdated": "2026-04-13",
  "camps": [
    {
      "id": 1,
      "name": "营地名称",
      "lon": 110.5231,
      "lat": 24.7832,
      "x": 1683.94,
      "y": 3606.23,
      "folder": "桂林市/阳朔县",
      "address": "详细地址",
      "type": "帐篷营地",
      "price": "价格",
      "description": "详细描述..."
    }
  ]
}
```

### regions.json

```json
{
  "version": "1.0",
  "lastUpdated": "2026-04-13",
  "regions": {
    "阳朔县": {
      "x": 1624,
      "y": 3433,
      "scale": 4
    }
  }
}
```

## 🛠️ 自定义地图

### 更换地图图片

1. 将新地图图片放入 `assets/images/` 目录
2. 修改 `index.html` 中的图片引用：
   ```html
   <img src="assets/images/your-map.png" alt="地图" class="map-image" id="mapImage">
   ```

3. 更新 `data/camps.json` 中的坐标数据

## 🌐 部署

### GitHub Pages

1. 将项目推送到 GitHub 仓库
2. 进入仓库 Settings → Pages
3. 选择 branch 为 `main`
4. 访问 `https://yourusername.github.io/repo-name`

### Vercel / Netlify

1. 连接 GitHub 仓库
2. Vercel/Netlify 会自动识别静态网站
3. 一键部署

### 阿里云 OSS

1. 创建 OSS bucket，设置为公共读
2. 上传所有文件
3. 配置静态网站托管

## 📱 响应式设计

- ✅ 桌面端优化
- ✅ 平板端适配
- ✅ 移动端触摸操作

## 🔧 技术栈

- **前端**: HTML5 + CSS3 + JavaScript
- **字体**: Google Fonts (Noto Sans SC)
- **图标**: Emoji 表情符号
- **地图交互**: 原生 JavaScript

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📧 联系方式

如有问题，请通过 GitHub Issues 联系。

---

**祝你使用愉快！🏕️**
