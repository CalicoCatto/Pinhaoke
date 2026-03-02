# Pinhaoke - 北京大学课程搜索

北京大学 2026 年春季学期课程搜索工具，支持本科生与研究生全部课程的快速检索与筛选。

## 功能

- 按课程名或教师姓名搜索
- 多维度筛选：学生类别、课程类别、开课单位、上课时间（星期）、教室
- 中文 / English 语言切换
- 玻璃拟态 (Glassmorphism) 风格 UI

## 数据来源

- `pku_undergraduate_course_schedule_spring_2026.xlsx` — 本科生课程表（37 个类别，2833 门课）
- `pku_graduate_course_schedule_spring_2026.xlsx` — 研究生课程表（42 个类别，1377 门课）

## 使用方法

1. 运行数据解析脚本生成课程数据：

```bash
python3 build_data.py
```

2. 用浏览器打开 `index.html` 即可使用。

## 项目结构

```
build_data.py    # Excel → JSON 解析脚本
courses_data.js  # 生成的课程数据（JS 格式）
courses.json     # 生成的课程数据（JSON 格式）
index.html       # 搜索页面（单文件 SPA）
```
