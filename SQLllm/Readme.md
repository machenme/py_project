## 项目截图
<div align="center">
  <img src="https://github.com/machenme/py_project/blob/main/SQLllm/demo.png" alt="demo">
</div>



# SQL数据库助手项目文档

## 项目概述
这是一个基于Flask的Web应用，提供以下核心功能：
- 将自然语言描述转换为SQL查询
- SQL语句安全检查
- 数据库结构提取
- 数据库初始化与管理

## 项目结构
```
.
├── .gitignore
├── .python-version
├── app.py                # 主应用入口
├── db_schema_extractor.py # 数据库结构提取
├── demo.png
├── example_deepseek.py   # DeepSeek API示例
├── init_database.py      # 数据库初始化
├── llm_service.py        # LLM服务实现
├── pyproject.toml        # 项目配置
├── README.md
├── requirements.txt      # 依赖项
├── run.py                # 应用启动
├── school.sql            # 示例数据库
├── security.py           # SQL安全检查
├── security_test.py      # 安全测试
├── SQL数据库助手项目介绍.pptx
├── start.py              # 替代启动方式
├── static/               # 静态资源
├── templates/           # 模板文件
├── test_queries.py       # 查询测试
└── uv.lock
```

## 核心功能

### 1. SQL生成 (llm_service.py)
- 使用DeepSeek API将自然语言转换为SQL
- 支持数据库模式作为上下文
- 提供模拟响应模式

### 2. SQL安全检查 (security.py)
- 检测多种SQL注入模式
- 敏感表操作检查
- 查询复杂度限制
- 安全级别评估
- 生成详细安全报告

### 3. 数据库结构提取 (db_schema_extractor.py)
- 连接到MySQL数据库
- 提取表结构、主键、外键和索引信息
- 格式化数据库结构为适合LLM提示的文本

### 4. 数据库初始化 (init_database.py)
- 执行SQL文件初始化数据库
- 验证数据完整性
- 检查表记录数和关键数据分布

## 安装与使用

### 依赖项
```bash
pip install -r requirements.txt
```

### 启动应用
```bash
python run.py
```

## 安全测试
项目包含全面的SQL注入测试套件(security_test.py)，支持：
- 10种预设SQL注入测试用例
- 自定义SQL语句测试
- 彩色终端输出
- 详细安全报告

测试用例包括：
1. UNION注入
2. 注释攻击
3. 多语句执行
4. 条件操纵
5. 盲注入
6. 时间延迟攻击
7. 存储过程执行
8. 内联注释
9. LIKE通配符攻击

## 测试方法
```bash
python security_test.py
```

## 示例用法
参考example_deepseek.py和test_queries.py中的示例
