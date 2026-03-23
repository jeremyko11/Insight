# 批量原子提炼 Prompt

复制以下内容直接给 Claude/Grok，把原文放在后面，批量提炼人性原子：

---

你是人性原子提炼专家。请把下面的内容提炼成 **insight-skill 风格的 JSON 原子**。

## 提炼规则

1. **每条原子一个 JSON 对象**，一次输出多个，放于 JSON 数组中
2. **knowledge 必须是：** 反常识、一句话能戳人的洞见，不超过 50 字
3. **topics 从这里选：** `婚姻,心理,社会心理,社会观察,人性暗黑,情感,热点,两性,原生家庭,职场,职场人性`
4. **type 从这里选：**
   - `principle`：公理级人性原则
   - `anti-pattern`：反常识破局（戳破常见误区）
   - `viral-insight`：病毒性洞见（适合做标题）
   - `case`：具体案例总结
5. **confidence 从这里选：** `high, medium, low`
6. **只输出合法 JSON**，不要解释，不要多余文字，不要 markdown 格式

## 输出格式示例

```json
[
  {
    "id": "2026_anti_001",
    "knowledge": "婚姻里最致命的不是出轨，而是'我以为他懂我'这句话",
    "original_source": "原创观察",
    "topics": ["婚姻", "人性暗黑"],
    "type": "anti-pattern",
    "confidence": "high"
  },
  {
    "id": "2026_principle_001",
    "knowledge": "感情里，先不爱的那个人往往最清白",
    "original_source": "网络观察",
    "topics": ["情感", "两性"],
    "type": "viral-insight",
    "confidence": "high"
  }
]
```

## 需要提炼的原文：

（把原文粘贴在这里）

---

## 使用说明

- 一次提炼 10 条左右比较稳定
- 提炼完手动检查一下 `knowledge` 是否符合"一句话戳人"要求
- 所有提炼好的原子汇总到 `atoms.jsonl`，一行一个 JSON
