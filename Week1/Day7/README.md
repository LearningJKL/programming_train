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

### D7 Week1 整理

| 项 | 内容 |
|----|------|
| **目标** | 仓库看起来像正式小项目 |
| **条件** | D1–D6 已完成 |
| **任务** | Markdown：目录结构、依赖列表、截图、≥3 条命令 |
| **要求** | 不是作业草稿口吻 |
| **结果** | `docs/week1.md` 或更新根 `README.md` |
| **验收** | 外人 5 分钟能看懂怎么跑 Week1 |
| **程度** | 仓库看起来像项目，不是作业草稿 |

---
