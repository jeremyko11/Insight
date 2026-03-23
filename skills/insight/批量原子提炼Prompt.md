# 批量原子提炼Prompt

请帮我把下面这段文字，提炼成insight人性原子库的原子条目。

## 原子定义

原子就是**可独立复用的人性洞见乐高**，每条原子是一个独立的JSON对象，包含以下字段：

```json
{
  "id": "编号",
  "knowledge": "一句话反常识、能戳人的洞见",
  "original_source": "原文出处",
  "topics": ["婚姻", "心理", "职场"],
  "type": "anti-pattern",
  "confidence": "high"
}
```

## 字段说明

| 字段 | 说明 |
|------|------|
| id | 编号规则：`年份_类型缩写_序号`，例如 `2026_viral_001` |
| knowledge | 一句话，清晰、戳人，不啰嗦 |
| original_source | 原文出处，例如「某小红书爆款笔记」「《被讨厌的勇气》」 |
| topics | 数组，适用话题：婚姻,心理,社会心理,社会观察,人性暗黑,情感,热点,两性,原生家庭,职场,职场人性 |
| type | 分类：principle(公理级)/anti-pattern(破误区)/viral-insight(病毒性洞见)/case(案例) |
| confidence | high/medium/low |

## 输出要求

- 每条原子占一行，合法JSON
- 不要多余说明，直接输出JSON数组
- 尽量多提炼，原文中每个独立洞见都提炼成一条
- 保持knowledge简短，一句话说清楚

---

## 原文开始：

（把你要提炼的原文贴在这里）

---

## 输出示例（参考格式）

```json
{"id": "2026_principle_001", "knowledge": "人性永远先自我保护，再谈爱与责任", "original_source": "insight公理", "topics": ["人性"], "type": "principle", "confidence": "high"}
{"id": "2026_viral_001", "knowledge": "为什么越听话的员工走得越早？因为公司只喜欢用听话的，不喜欢给听话的涨工资", "original_source": "职场观察", "topics": ["职场"], "type": "viral-insight", "confidence": "high"}
```
