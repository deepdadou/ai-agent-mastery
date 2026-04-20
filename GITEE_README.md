# AI 智能体操作秘籍

> **让 AI 为你打工，而不是你为 AI 打工！** 🤖💰

[![GitHub stars](https://img.shields.io/github/stars/deepdadou/ai-agent-mastery)](https://github.com/deepdadou/ai-agent-mastery)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

---

## 🚀 快速开始

### 1 分钟上手

```markdown
# 万能提示词模板

# 角色设定
你是 [具体角色]，擅长 [具体技能]

# 背景
[任务背景]

# 目标
[要明确达成的目标]

# 任务
[具体要做什么]

# 要求
- [要求 1]
- [要求 2]

# 输出格式
[希望 AI 以什么格式输出]
```

### 3 个核心思维

1. **AI 不是搜索引擎** - 给目标，不是给问题
2. **把 AI 当员工** - 给目标、资源、反馈
3. **迭代优于完美** - 分多轮改进

---

## 📚 内容概览

| 章节 | 内容 |
|------|------|
| 核心思维 | AI 使用的正确 mindset |
| 提示词法则 | MASTER 法则 + 万能模板 |
| 平台指南 | OpenClaw/Claude/扣子/文心/Kimi |
| 实战场景 | GitHub Bounty/智能合约审计/内容创作 |
| 效率技巧 | 提示词库/批量处理/链式调用 |
| 避坑指南 | 常见错误和解决方案 |

---

## 🎯 常用场景

### 💰 GitHub Bounty

```markdown
分析这个 GitHub issue，生成解决方案：
[粘贴 issue 内容]

要求：
1. 理解问题核心
2. 生成最小可行解决方案
3. 代码简洁便于 review
4. 添加测试用例
5. 写 PR 描述
```

### 🏆 智能合约审计

```markdown
审计这个合约的安全漏洞：
[粘贴代码]

重点检查：
1. 重入攻击
2. 整数溢出
3. 权限控制
4. 价格操纵

输出每个漏洞的：
- 严重程度
- 位置和描述
- 利用场景
- 修复建议
```

### 📝 内容创作

```markdown
写一篇关于 [主题] 的技术教程：

要求：
- 目标读者：[初学者/中级/高级]
- 字数：2000-3000 字
- 包含代码示例
- 结构清晰有目录
```

---

## 🛠️ 平台对比

| 平台 | 代码能力 | 中文理解 | 免费额度 | 推荐场景 |
|------|----------|----------|----------|----------|
| **Claude** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 有限 | 代码、复杂任务 |
| **文心一言** | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 较多 | 中文内容 |
| **扣子** | ⭐⭐⭐ | ⭐⭐⭐⭐ | 中等 | 工作流自动化 |
| **Kimi** | ⭐⭐⭐ | ⭐⭐⭐⭐ | 较多 | 长文本处理 |
| **OpenClaw** | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 本地部署 | 自动化任务 |

---

## ⚡ 效率技巧

### 1. 创建提示词库

```bash
mkdir ~/prompts

# 代码审查模板
cat > ~/prompts/code-review.md << 'EOF'
审查以下代码的安全性：
```$CODE
```

重点检查：
1. SQL 注入
2. XSS 攻击
3. 认证问题
EOF

# 使用时
sed "s|\$CODE|$(cat mycode.py)|" ~/prompts/code-review.md | claude
```

### 2. 批量处理

```bash
#!/bin/bash
# 批量审计智能合约

for contract in contracts/*.sol; do
  echo "审计 $contract..."
  claude "审计这个合约：$(cat $contract)" >> reports/$(basename $contract).md
done

echo "所有审计完成！"
```

### 3. 链式调用

```bash
# 第 1 步：生成代码
claude "生成一个 Python 脚本，功能是 XXX" > output.py

# 第 2 步：审查代码
claude "审查这个代码的安全问题：$(cat output.py)" >> review.md

# 第 3 步：生成测试
claude "为这个代码写测试：$(cat output.py)" > test.py
```

---

## ⚠️ 避坑指南

| ❌ 错误做法 | ✅ 正确做法 |
|----------|----------|
| 完全让 AI 写代码，不审查就提交 | AI 生成初稿，人工审查后提交 |
| 一次让 AI 做 10 件事 | 拆分成小任务，逐个完成 |
| 忽略 token 限制 | 定期总结，开始新对话 |
| 相信 AI 说的所有话 | 一定要测试验证 |
| 无节制使用付费 API | 根据任务选择合适模型 |

---

## 📖 完整文档

查看 [SKILL.md](SKILL.md) 获取 6000 字完整秘籍！

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

---

## 📄 许可证

MIT License

---

## 💬 联系

- GitHub: [@deepdadou](https://github.com/deepdadou)
- 问题反馈：[Issues](https://github.com/deepdadou/ai-agent-mastery/issues)

---

*让 AI 为你赚钱！* 💰🤖
