# @leason/claude-code-config

为 claude-code-router 提供 ModelScope 默认配置的 Node.js 包。

## 前置要求

- Node.js >= 14.0.0
- ModelScope API Key（请从 [ModelScope](https://modelscope.cn/) 获取）

## 快速开始

### 1. 配置 API Key（必需）

**方式 1: 环境变量（推荐）**

```bash
export MODELSCOPE_API_KEY="your-api-key-here"
```

**方式 2: 也可以在安装后手动配置（详见配置章节）**

### 2. 安装

首先安装必要的前置依赖：

```bash
# 1. 安装 claude-code
npm install -g @anthropic-ai/claude-code

# 2. 安装 claude-code-router
npm install -g @leason/claude-code-router
```

然后选择以下任意一种方式安装本配置包：

**方式 1: 从 npm 仓库安装（推荐）**

```bash
npm install -g @leason/claude-code-config
```

**方式 2: 从源码安装**

```bash
# 克隆项目
git clone https://github.com/leason-wan/claude-code-config
cd claude-code-config

# 安装依赖并全局安装
npm install
npm install -g .
```

### 3. 运行配置

```bash
ccr-modelscope
```

### 4. 开始使用

```bash
ccr code
```

## 语言支持

本工具支持中英文双语，会根据系统语言自动选择：

- 中文环境（`LANG` 包含 `zh`）：显示中文提示
- 其他环境：显示英文提示

## 配置

默认配置文件目录为：`~/.claude-code-router/`。

- 主配置文件路径：`~/.claude-code-router/config.json`
- 插件目录路径：`~/.claude-code-router/plugins/`

运行 `ccr-modelscope` 后会自动生成上述目录和文件。

### 手动配置 API Key

如果在运行 `ccr-modelscope` 之前没有设置环境变量，可以手动编辑配置文件：

1. 进入配置目录：

   ```bash
   cd ~/.claude-code-router
   ```

2. 编辑配置文件：

   ```bash
   # macOS/Linux 系统
   nano config.json
   # 或使用您喜欢的编辑器
   ```

3. 将 `"api_key"` 字段替换为您的实际 ModelScope API Key

### 支持的模型

- `Qwen/Qwen3-Coder-480B-A35B-Instruct` - 默认模型，支持长上下文和流式输出

## 故障排除

### 常见问题

1. **API Key 无效**：确保您的 ModelScope API Key 有效，每天限额 2 千次
2. **命令未找到**：确保所有包都使用 `-g` 标志全局安装
3. **权限问题**：在某些系统上全局安装可能需要 `sudo` 权限

### 获取帮助

- 查看 [ModelScope 文档](https://modelscope.cn/docs)

## 功能特性

- 🌐 自动多语言支持（中文/英文）
- 🔧 一键配置 ModelScope 集成
- 🚀 支持流式响应
- 📝 智能请求转换
- 🔑 灵活的 API Key 配置方式

## 许可证

Apache-2.0
