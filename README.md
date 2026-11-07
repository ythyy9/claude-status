# Claude 续费一览

公开页面：https://claude.cancantt.com/

只有一个文件 `index.html`。改账号、价格或续费日时，编辑其中 `ACCOUNTS` 一段后提交推送，GitHub Pages 约一分钟后更新。

- `day`：每月开通/续费日（按北京时间；当月没有这一天时按月底算）
- `since`（可选）：首次开通日期 `YYYY-MM-DD`，开通当天显示“今天开通”并倒数到下个月，而不是“今天续费”
- `price`：每月总价（含服务器），货币符号在 `CURRENCY`
- 剩余天数不超过 `SOON_DAYS` 时数字标红

页面带 `noindex`，不会被搜索引擎收录，但知道地址的人都能打开。
