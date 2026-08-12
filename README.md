# 门店净利润看板

企业微信移动端 H5 Demo，用于查看总部、分公司、门店经营利润数据。

## 当前页面

- 默认入口：`/profit-overview`
- 一级页面：`/profit-overview`
- 二级页面：`/branch/beijing/stores`
- 三级页面：`/store/BJ10001`

## 启动方式

```bash
pnpm install
pnpm dev
```

如果系统没有全局 Node，请使用 Codex 自带 Node 运行。

## 本地双击预览

不要双击根目录的 `index.html`，它是 Vite 开发入口，需要开发服务器编译。

如果只想本地双击查看 Demo，请打开：

```text
双击打开预览.html
```

或直接打开：

```text
dist/index.html
```

## 当前已实现

- 一级页面：总部 24 家分公司层级经营表
- 一级页面：全国合计行、展开销售额/业务毛利/费用总额子行
- 一级页面：点击分公司名称或门店数量进入二级
- 北京分公司 88 家门店固定模拟数据
- 750px 设计稿 + rem 适配
- 二级页面顶部经营概览
- 搜索门店名称 / 编码
- 筛选：门店性质、经营状态、盈亏状态、租赁状态
- 排序：默认、业务累计、财务累计、最新月份、业务财务差额
- 字段快速定位：门店信息、累计利润、1—4月、5—8月、9—12月
- 同一张原生 table 横纵向滚动
- 左侧序号和门店名称冻结
- 顶部双层表头冻结
- 1—12月全部在同一张表中，8—12月保留并显示“—”
- 点击门店名称进入三级门店经营详情页
- 点击金额或档案字段打开底部详情弹层
- H5 内部全屏表格模式
- 三级页面：单家门店 1—12 月经营详情表
- 三级页面：月份列冻结、表头冻结、累计行动态计算
- 三级页面：手机销量、销售额、业务毛利、费用、成本、业务/财务净利润
- 三级页面：复用二级门店基础信息，所有门店可进入详情

## 目录说明

- `index.html`：Vite 开发入口 HTML
- `dist/index.html`：打包后的成品 HTML
- `src/views/BranchStoreProfitView.vue`：二级页面主视图
- `src/views/ProfitOverviewView.vue`：一级页面主视图
- `src/views/StoreDetailView.vue`：三级页面主视图
- `src/components/profit/BranchProfitTable.vue`：一级层级经营表格
- `src/components/profit/StoreProfitTable.vue`：核心冻结表格
- `src/components/profit/StoreOperatingTable.vue`：三级月度经营详情表格
- `src/components/profit/StoreBasicInfo.vue`：三级门店基础信息区
- `src/mock/branchProfitOverview.ts`：24 家分公司模拟数据
- `src/mock/branchStoreProfit.ts`：北京 88 家门店模拟数据
- `src/mock/storeOperatingDetail.ts`：三级页面稳定模拟经营明细
- `src/services/profit.ts`：数据访问层，后续替换真实接口
- `docs/需求说明.md`：当前需求整理

## 文件位置

当前项目所有开发文件、源码、配置、说明文档和打包后的 HTML 都在：

```text
/Users/minsu/Documents/门店净利润看板
```
