# Claude 续费一览

公开页面：https://claude.cancantt.com/

## 在网页上修改

打开 https://claude.cancantt.com/edit.html ，可以新增、修改、删除和排序账号，点“保存”后写回本仓库的 `accounts.json`，GitHub Pages 大约 1 分钟后更新。

第一次使用要填一个 GitHub 细粒度令牌（Fine-grained token），只授权本仓库、权限只开 Contents: Read and write。令牌只保存在当前浏览器里；换设备要重新填，点“退出”会清掉。令牌到期或泄露时，在 GitHub 设置里删掉再新建一个即可。

编辑页本身是公开的，但没有令牌只能看到登录框，改不了任何东西。

## 文件

- `index.html`：展示页，打开时读取 `accounts.json`
- `edit.html`：编辑页，通过 GitHub API 读写 `accounts.json`
- `accounts.json`：账号数据，也可以直接在 GitHub 网页上改

`accounts.json` 里每个账号的字段：

- `name` 名称、`owner` 使用者、`plan` 套餐、`card` 付款卡、`servers` 服务器
- `day`：每月续费日（按北京时间；当月没有这一天时按月底算）
- `price`：每月总价（含服务器），货币符号在顶层 `currency`
- `since`（可选）：首次开通日期 `YYYY-MM-DD`，开通当天显示“今天开通”并倒数到下个月，而不是“今天续费”

剩余天数不超过 3 天时数字标红（`index.html` 里的 `SOON_DAYS`）。页面带 `noindex`，不会被搜索引擎收录，但知道地址的人都能打开。
