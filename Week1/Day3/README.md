> 面向空间信息 / GIS / 遥感方向，用可展示的小仓库积累项目经历。  
> 建议仓库根目录结构见文末。

---

## 通用约定

| 项目 | 说明 |
|------|------|
| 每天结束标准 | 代码可运行 + 至少 1 张截图或输出文件进入 `docs/screenshots/` |
| 样例数据 | 优先公开小数据（Natural Earth、OSM 导出、自建小 GeoJSON）；没有真实数据可人造 10–50 条 |
| 环境 | Python 3.10+，建议 conda / venv；Windows 可用 |
| 工作方式 | 按日打勾；缺一天用周末补同编号，不跳编号堆到最后 |

### 建议仓库目录

```
gis-30days/
  data/ raw/ processed/
  src/ week1/ week2/ week3/ week4/
  docs/ screenshots/
  web/          # Week3 前端
  api/          # Week3/4 后端
  README.md
```
## 第 1 周：数据清洗 + 矢量基础

### 第 1 周总览

| 编号 | 主题 | 技术栈 | 核心交付物 |
|------|------|--------|------------|
| D1 | CSV 清洗 + 折线图 | Python（pandas）+ HTML/JS（Chart.js）或纯 Python 出图 | 清洗后 CSV + 折线图 |
| D2 | 读矢量数据 | Python + geopandas | 元信息打印截图 |
| D3 | 投影转换并导出 | Python + geopandas | 转换后 GeoJSON/Shapefile |
| D4 | 属性查询 + 空间筛选 | Python + geopandas | 筛选结果文件 |
| D5 | 专题图出图 | geopandas + matplotlib | 带图例标题的 PNG |
| D6 | 命令行小工具 | Python（argparse） | `tool.py` + README 命令 |
| D7 | Week1 整理 | Markdown | 目录、依赖、截图、3 条命令 |

---

### D3 投影转换并导出

| 项 | 内容 |
|----|------|
| **目标** | 转到目标 CRS 并导出 |
| **条件** | D2 同一份数据；目标如 `EPSG:4326`（或本地投影如 `EPSG:4547`） |
| **任务** | 转换前打印 CRS → `to_crs` → 再打印 → `to_file`（GeoJSON 或 Shapefile） |
| **要求** | 转换前后 CRS 各打印一次；导出文件可被 QGIS 打开 |
| **结果** | `data/processed/xxx_4326.geojson` |
| **验收** | QGIS 加载无错；属性还在 |
| **程度** | 转换前后各打印一次 CRS；文件能被 QGIS 打开 |


---
