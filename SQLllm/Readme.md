## 安装说明
1. 安装依赖：
```bash
pip install -r requirements.txt
```
2. 配置环境变量：
    - 在`.env`文件中设置你的DeepSeek API密钥和其他配置：

### 数据库初始化说明

1. 确保MySQL服务器已启动并正在运行

2. 在`.env`文件中配置正确的数据库连接信息：
   ```env
   DB_HOST=localhost
   DB_NAME=school
   DB_USER=your_username
   DB_PASSWORD=your_password
   DB_PORT=3306
   ```
## DeepSeek API设置

1. 获取API密钥：
   - 访问DeepSeek官网注册账号
   - 在开发者设置中生成API密钥
   - 将API密钥复制到`.env`文件中

2. 测试API连接：
```bash
python example_deepseek.py
```
如果配置正确，你将看到示例SQL查询的生成结果。

## 运行应用

1. 启动Web服务器：
```bash
python run run.py
```

2. 访问应用：
   打开浏览器访问 http://localhost:5000
