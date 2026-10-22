# 卡客车轮胎参数查询 PWA

面向 OE 客户技术经理与大客户经理的手机端查询工具。当前内置数据来自：产品参数汇总_2023 v1.0 _simp.xlsx，共 100 条。

## 使用
1. 将整个文件夹部署到 HTTPS 静态站点（GitHub Pages、Azure Static Web Apps 或公司内部静态站点）。
2. 手机浏览器打开后，可“添加到主屏幕”。
3. 先选尺寸，再选花纹，即可查看全部参数；也可按 CAI、规格或花纹关键词搜索。
4. 首次访问后支持离线查询。

## 数据更新
更新 `data/tires.json` 中的数据及版本信息，修改 `service-worker.js` 中的 CACHE 版本，然后重新部署。更新后所有用户会从部署包读取最新数据。

## 数据规则
- 缺失值留空，App 显示“暂无”。
- 同一尺寸可有多个花纹或多个 CAI。
- 建议版本命名：`YYYY年第N版`，数据日期使用 `YYYY-MM-DD`。

Built by CHN/T  
technical contact: jing.li@michelin.com
