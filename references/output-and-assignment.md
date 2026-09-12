# 结论判据 · 现实动作 · HTML 记录模板

---

## 一、结论判据（四选一，必须选）

先看 Q1 与 Q2 的组合，它决定有没有必要往下走：

| Q1 行为证据 | Q2 现状代价 | 判读 |
|---|---|---|
| 有（有人已在付钱/已签字） | 有（现状有明显成本） | 需求成立 → 看 Q3/Q4 定 GO 还是收窄 |
| 有 | 无（现状不花钱不费时） | 矛盾。回到 Q1 核实那笔钱到底买的是什么 |
| 无 | 有（现状在硬扛） | 需求可能是真的，但你还没拿到证据 → 按 PARK 或收窄处理 |
| 无 | 无 | **KILL。** 不要再往下问 |

然后：

| 结论 | 判据 | 后续动作 |
|---|---|---|
| **GO** | Q1 有行为证据 **且** Q3 能点名具体人 **且** Q4 有本周可收款的点 | 直接进执行；现实动作是"把第一笔钱收进来" |
| **收窄后 GO** | 需求成立，但 Q4 的切口太宽（要求先搭架构/先拿牌照/先融资） | 只做最小点，其余项全部写进"挂起"并注明重启条件 |
| **PARK** | 需求可能真，但关键前提（通道/资质/对手方/审批）待核实且短期无法核实 | 写明**什么条件满足就重启**（要可观察，不写"条件成熟时"） |
| **KILL** | Q1 无行为证据 且 Q2 显示现状无代价 | 停。不要留"以后再看看"的尾巴 |

**禁止的结论措辞**：「还需要进一步论证」「建议再调研」「总体可行但要注意风险」「视情况而定」。出现这类措辞说明你还没做完诊断。

**PARK 的写法示例**
> PARK。重启条件：① 拿到 XX 银行关于结汇类目的**书面**定性；② 对手方主体全称与信用代码书面确认。两条任一未达成，不重启。

---

## 二、现实动作（assignment）

**这是交付核心，比结论更重要。** 一条。本周内能做完。能证伪或证实最承重的那条前提。

### 五条标准（缺一条就不合格）

1. **是动作，不是策略**
   - ✅「找 3 家已落地的同类主体，各问一句：你们第一笔钱是谁付的、走的什么科目。」
   - ❌「继续深入研究市场」「建立行业认知」「持续跟进」
2. **能拿到外部回应** —— 能被拒绝、能拿到报价、能拿到官方书面答复。自己内部能完成的不算。
3. **能证伪** —— 做完之后某条前提被明确证实或推翻，而不是"了解更多"。
4. **有明确对象** —— 具体机构、具体岗位、具体受理窗口。不写"相关方""有关部门""潜在客户"。
5. **不超过一周** —— 超过一周的拆成第一周能做完的那一小步。

### 动作模板

```
动作：<动词开头，一句话>
对象：<具体机构/岗位/窗口>
要拿到的东西：<可留痕的产出——书面答复 / 报价单 / 拒绝理由 / 签字件>
证伪哪条前提：<前提编号 + 那一条>
截止：<本周内的具体日期>
失败也算结果：<如果对方拒绝或答不出来，说明什么>
```

**"失败也算结果"这一栏必须填。** 一个不给拒绝留位置的动作用的是不可证伪的设计——那它不是体检，是仪式。

### 动作示例（对照用）

| 场景 | 不合格 | 合格 |
|---|---|---|
| 通道可行性 | 研究跨境数据出境路径 | 找已办成同类业务的一家主体，问当初的受理窗口与所需材料清单，拿到书面或截图 |
| 需求验证 | 再访谈几家潜在客户 | 向 3 家目标客户报同一份最小版本的价格，记录谁还价、谁不回复 |
| 资质前置 | 咨询 EDI 办理条件 | 向省通信管理局受理窗口提交一次材料预审，拿到补正清单 |
| 对手评估 | 分析竞对的战略意图 | 找到竞对与头部合作方的联合公告原文，逐条核对排他范围，标出与我方重叠的条款 |

---

## 三、HTML 记录模板

落盘路径：`<工作区>/立项反问-<主题>-<YYYYMMDD>.html`（日期用命令取，不手算）。

要求：**结论先行**（结论卡放在六问之前）、light 主题、可打印、来源标注三级、成品内不出现修订说明与版本标记。

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>立项反问 — {主题}</title>
<style>
  :root{ --ink:#1a1a1a; --ink2:#4a4a4a; --ink3:#7a7a7a;
    --line:#d8d5cc; --line2:#ebe8df;
    --bg:#ffffff; --bg2:#faf9f5; --bg3:#f3f1ea;
    --red:#a32d2d; --amber:#854f0b; --teal:#0f6e56; --blue:#185fa5; }
  *{box-sizing:border-box;}
  body{margin:0;padding:0;background:var(--bg);color:var(--ink);
    font-family:"Helvetica Neue",Helvetica,Arial,"PingFang SC","Microsoft YaHei",sans-serif;
    font-size:14px;line-height:1.75;}
  .wrap{max-width:960px;margin:0 auto;padding:56px 40px 80px;}
  header{border-bottom:2px solid var(--ink);padding-bottom:20px;margin-bottom:8px;}
  h1{font-size:26px;font-weight:600;margin:0 0 10px;letter-spacing:-.3px;}
  .sub{font-size:13px;color:var(--ink3);margin:0;}
  .meta{font-size:12px;color:var(--ink3);margin-top:14px;line-height:1.7;}
  .meta b{color:var(--ink2);font-weight:600;}
  h2{font-size:18px;font-weight:600;margin:48px 0 14px;padding-bottom:8px;border-bottom:1px solid var(--line);}
  h3{font-size:15px;font-weight:600;margin:28px 0 8px;}
  p{margin:8px 0;}
  ul,ol{margin:8px 0;padding-left:22px;}
  li{margin:4px 0;}
  code{font-family:Consolas,monospace;font-size:12px;background:var(--bg3);padding:1px 5px;border-radius:3px;}
  table{width:100%;border-collapse:collapse;margin:14px 0;font-size:12.5px;}
  th,td{border:1px solid var(--line);padding:8px 10px;text-align:left;vertical-align:top;}
  th{background:var(--bg3);font-weight:600;font-size:12px;}
  .callout{background:var(--bg2);border-left:3px solid var(--ink);padding:12px 16px;margin:16px 0;font-size:13px;}
  .callout.warn{border-left-color:var(--red);background:#fdf5f5;}
  .callout.ok{border-left-color:var(--teal);background:#f2faf7;}
  .callout.info{border-left-color:var(--blue);background:#f4f9fd;}
  .verdict{border:2px solid var(--ink);border-radius:8px;padding:20px 24px;margin:22px 0;background:var(--bg2);}
  .verdict .label{font-size:12px;color:var(--ink3);letter-spacing:.08em;}
  .verdict .value{font-size:24px;font-weight:600;margin:4px 0 10px;}
  .tag{display:inline-block;font-size:11px;padding:1px 7px;border-radius:10px;
    border:1px solid var(--line);color:var(--ink2);background:var(--bg2);white-space:nowrap;}
  .tag.conf{border-color:#0f6e56;color:#0f6e56;background:#f2faf7;}
  .tag.new{border-color:#185fa5;color:#185fa5;background:#f4f9fd;}
  .tag.todo{border-color:#854f0b;color:#854f0b;background:#fdf9f2;}
  .tag.flag{border-color:#a32d2d;color:#a32d2d;background:#fdf5f5;}
  footer{margin-top:56px;padding-top:16px;border-top:1px solid var(--line);font-size:11.5px;color:var(--ink3);}
  @media print{ body{font-size:11.5pt;} .wrap{max-width:none;padding:0;} h2{page-break-after:avoid;} }
</style>
</head>
<body>
<div class="wrap">

<header>
  <h1>立项反问 — {主题}</h1>
  <p class="sub">六问逐条诊断 · 前提清单 · 结论 · 现实动作</p>
  <div class="meta">
    <b>反问日期</b>　{YYYY-MM-DD}　　<b>阶段</b>　{A 纯设想 / B 已对接 / C 已付费 / D 合规工程}<br>
    <b>证据标注</b>　<span class="tag conf">既有已确认</span>
    <span class="tag new">本会话新检索</span>
    <span class="tag todo">待核实</span>
  </div>
</header>

<div class="verdict">
  <div class="label">结论</div>
  <div class="value">{GO / 收窄后 GO / PARK / KILL}</div>
  <p>{两三句话说清为什么。不写"仍需论证"。}</p>
</div>

<h2>一、六问逐条</h2>
<table>
  <thead>
    <tr><th style="width:14%">问题</th><th style="width:44%">回答</th>
        <th style="width:14%">证据等级</th><th style="width:28%">判定</th></tr>
  </thead>
  <tbody>
    <tr><td>Q1 需求真实性</td><td>{…}</td><td><span class="tag conf">既有已确认</span></td><td>{通过 / 红旗：…}</td></tr>
    <tr><td>Q2 现状替代</td><td>{…}</td><td><span class="tag new">本会话新检索</span></td><td>{…}</td></tr>
    <tr><td>Q3 绝望的具体性</td><td>{…}</td><td><span class="tag todo">待核实</span></td><td>{…}</td></tr>
    <tr><td>Q4 最窄切口</td><td>{…}</td><td>…</td><td>{…}</td></tr>
    <tr><td>Q5 观察与意外</td><td>{…}</td><td>…</td><td>{…}</td></tr>
    <tr><td>Q6 未来适配</td><td>{…}</td><td>…</td><td>{…}</td></tr>
  </tbody>
</table>
<p style="font-size:12.5px;color:var(--ink3)">未被问到的条目（按阶段路由跳过）：{列出编号}。</p>

<h2>二、前提清单</h2>
<table>
  <thead><tr><th style="width:6%">#</th><th style="width:52%">前提</th>
  <th style="width:18%">表态</th><th style="width:24%">处理</th></tr></thead>
  <tbody>
    <tr><td>1</td><td>{假设}</td><td>{同意 / 反对}</td><td>{保留 / 已修订为：…}</td></tr>
    <tr><td>2</td><td>{假设}</td><td>…</td><td>…</td></tr>
    <tr><td>3</td><td>{假设}</td><td>…</td><td>…</td></tr>
  </tbody>
</table>

<h2>三、现实动作</h2>
<div class="callout ok">
<p><b>动作</b>　{动词开头一句话}</p>
<p><b>对象</b>　{具体机构/岗位/窗口}</p>
<p><b>要拿到的东西</b>　{书面答复 / 报价单 / 拒绝理由 / 签字件}</p>
<p><b>证伪哪条前提</b>　{编号} — {那一条}</p>
<p><b>截止</b>　{本周内具体日期}</p>
<p><b>失败也算结果</b>　{对方拒绝或答不出来，说明什么}</p>
</div>

<h2>四、未决问题</h2>
<ul>
  <li>{…}</li>
</ul>

<footer>
本记录由六问立项反问生成，只做假设体检，不含方案与实施建议。
证据等级：既有已确认＝此前已核验；本会话新检索＝本轮检索所得，未经二次核验；待核实＝仅有口头或推断来源。
</footer>

</div>
</body>
</html>
```

### 交付自查（落盘前）

- [ ] 结论卡在六问之前（结论先行）
- [ ] 每条回答都带证据等级标签
- [ ] 被跳过的条目已列明，不是静默省略
- [ ] 现实动作六项字段全填，**"失败也算结果"不为空**
- [ ] 全文无修订说明、无版本号、无"新增/更新"标注
- [ ] light 主题，打印时表格不跨页断裂
