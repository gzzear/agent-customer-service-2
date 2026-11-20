# 智能客服2 最终版项目源码（第62–73节）

本仓库是课程《Agent大型项目实战2：智能客服》第62–73节项目（问道星辰 / constomer）的最终完整源码，整理自课包原版 RAR。

**这是私有课程资料，仅供个人学习使用，请勿公开传播或二次分发。**

课程原版说明见 `README.original.md`。复制 `.env.example` 为 `.env` 后填写自己的密钥再运行。

## 目录结构

- `llm_backend/` 后端
  - `run.py`：启动入口，加载 FastAPI 应用 `main:app`
  - `main.py`：FastAPI 应用主体
  - `app/lg_agent/`：Multi-Agent / LangGraph 智能体
  - `app/services/`：业务服务（对话、检索、索引、模型工厂等）
  - `app/api/`、`app/core/`、`app/models/`、`app/schemas/`、`app/tools/`、`app/prompts/`
  - `app/graphrag/`：GraphRAG 组件、提示词与示例输入数据
  - `static/`：前端静态资源（Vue 构建产物）
  - `scripts/`：辅助脚本（如初始化数据库）
- `requirements.txt`：Python 依赖
- `.env.example`：环境变量模板（不要把真实 `.env` 提交进仓库）

## 课包原状说明

原课包中以下 Python 文件是空实现，已按原样保留：

- `llm_backend/app/lg_agent/kg_sub_graph/kg_builder.py`
- `llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/workflows/multi_agent/text2cypher.py`
- `llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/workflows/multi_agent/text2cypher_with_visualization.py`
- `llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/retrievers/cypher_examples/dynamic_schema_retriever.py`

另有空的 `__init__.py`：`llm_backend/app/services/__init__.py`、`llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/__init__.py`、`llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/ui/__init__.py`、`llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/ingest/__init__.py`、`llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/components/__init__.py`、`llm_backend/app/lg_agent/kg_sub_graph/agentic_rag_agents/retrievers/cypher_examples/__init__.py`。

整理时已去掉：Python 虚拟环境 `mygraphrag`、索引产物（output / cache / lancedb）、日志、`.env` 密钥文件、`__pycache__`、IDE 配置，以及课件广告文件/文件名后缀。源码里出现的硬编码 API Key 已替换为占位符 `YOUR_API_KEY`。
