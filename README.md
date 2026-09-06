# 高中数学题库

> GitHub = 原题库（Source of Truth）
> Notion = 学习记录与动态分析数据库

本仓库用于长期保存高中数学原题、标准答案、解析、题目结构化数据及图片资源。

## 目录结构

```text
high-school-math-question-bank/
├── README.md
├── index.json
├── schema/
│   └── question-schema.json
├── 人教B版/
│   └── 高一上/
│       ├── 01-集合/
│       ├── 02-等式与不等式/
│       ├── 03-函数/
│       └── ...
├── questions/
│   ├── json/
│   ├── markdown/
│   └── latex/
└── assets/
    └── images/
```

## 三层数据结构

### 1. 原题层
保存题目本身及稳定信息：题干、选项、答案、解析、知识点、题型、难度、来源等。

### 2. 文件层
同一道题可以保存为 JSON、Markdown、LaTeX 三种格式。图片统一放在 `assets/images/`。

### 3. 学习记录层
Notion 不重复保存完整原题，而是通过 `question_id` 关联 GitHub 题目，记录：

- 作答情况
- 错误类型
- 错误原因
- 知识点掌握度
- 模型掌握度
- 复习次数
- 下次复习时间
- AI 筛选标签

## ID 规范

每道题必须拥有唯一、稳定的 `question_id`。

推荐格式：

`MATH-B-G1-01-024`

例如：

`MATH-B-G1-01-024`

表示：人教B版 / 高一 / 第01章 / 第024题。

## 重要原则

1. **GitHub 是原题的唯一来源。**
2. **Notion 不作为原题文件仓库。**
3. **同一道题的 JSON、MD、TeX 使用同一个 question_id。**
4. **题目一旦进入正式题库，question_id 不随 Notion 记录变化。**
5. **后续可以利用 GitHub + Notion + AI 自动完成题目筛选、错题分析和动态训练。**
