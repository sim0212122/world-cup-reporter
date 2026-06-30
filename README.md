# 世界杯小记者 2026

给小朋友的世界杯互动追踪工具。纸质版 + 手机端配合使用。

## 怎么用

### 小朋友（纸质版）
1. 打开 `print.html` → 点击「打印」→ 用 A4 纸打印出来
2. 每场比赛开赛前，在「我猜」栏圈一个结果（主队赢/平局/客队赢）
3. 比赛结束后，在「结果」栏圈真实结果，填上比分

### 爸爸（手机端）
1. 手机浏览器打开网址（部署后获得）
2. 「赛程」Tab：查看所有比赛
3. 「预测」Tab：帮小朋友录入预测（或让小朋友直接点）
4. 比赛结束后录入比分，系统自动算分
5. 「战绩」Tab：看小朋友的预测统计和成就徽章

## 积分规则

| 结果 | 得分 |
|------|------|
| 猜对胜负 | +10 |
| 猜对平局 | +15 |
| 猜错了 | +3（参与就有分）|
| 没预测 | 0 |

## 更新赛程

当淘汰赛对阵确定后：
1. 编辑 `schedule.json`
2. 找到对应的比赛，修改 `home` 和 `away` 字段（填实际队名）
3. 同时修改 `homeFlag` 和 `awayFlag`（用国旗 emoji）
4. 提交到 GitHub，Pages 自动更新

## 部署到 GitHub Pages

```bash
# 1. 创建 GitHub 仓库（在 github.com 上操作）
#    仓库名：world-cup-reporter
#    设置为 Public

# 2. 本地推送
git init
git add .
git commit -m "世界杯小记者 v1"
git remote add origin https://github.com/sim0212122/world-cup-reporter.git
git push -u origin main

# 3. 启用 Pages
#    GitHub 仓库 → Settings → Pages → Source: main branch → Save
#    等几分钟，获得网址：https://sim0212122.github.io/world-cup-reporter/
```
