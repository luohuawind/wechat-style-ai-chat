# wechat-style-ai-chat
一个极简的微信风格AI聊天界面，支持本地大模型、永久记忆存储。
# 年年 · 微信风格AI聊天


## 功能

- 💬 **微信风格UI**：绿色气泡（用户）、白色气泡（AI）
- 🧠 **永久记忆**：聊天记录自动保存到浏览器，刷新不丢失
- ⏎ **回车发送**：Enter发送，Shift+Enter换行
- 🤖 **本地模型**：通过llama.cpp调用本地大模型

## 如何运行

### 1. 启动本地模型服务

```bash
# 使用llama.cpp的server模式
./llama-server -m your-model.gguf --host 127.0.0.1 --port 8080
```

### 2. 打开应用

双击`index.html`，或在本地起一个HTTP服务：

```bash
python -m http.server 3000
```

然后打开 `http://localhost:3000`

## 项目结构

```
index.html    # 单文件应用，120行代码
```

## 技术栈

- HTML/CSS/JavaScript（原生）
- llama.cpp server（本地大模型）
- localStorage（聊天记录持久化）

## 亮点说明

- **代码极简**：120行实现完整AI聊天
- **停止词配置**：`stop: ["我："]` 防止模型自问自答
- **自动滚动**：新消息自动滚到底部

## 文件命名建议

```
niannian-chat.html
```

或者作为项目：

```
niannian-ai-chat/
├── index.html
└── README.md
```
