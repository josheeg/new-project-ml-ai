# new-project-ml-ai
git init

uv init --no-workspace
uv venv

uv add ruff mypy pytest pytest-cov pytest-asyncio pyinstaller pydantic python-dotenv build twine python-dotenv coverage hatchling mkdocs mkdocs-material sphinx sphinx-rtd-theme sphinx-autodoc-typehints setuptools httpx pandas hatchling flit-core


# Core Data Science & Wrangling
uv add pandas numpy scipy polars

# Visualization
uv add matplotlib seaborn plotly

# Modern Forecasting & Time Series Models
uv add statsmodels prophet neuralforecast darts sktime pmdarima lightgbm xgboost catboost

# Development Tools & Notebook Support
uv add --dev jupyter ipykernel notebook


# cpu

uv add tensorflow-cpu

uv add torch --index-url https://download.pytorch.org/whl/cpu

# LLMs, RAG & Orchestration
uv add langchain langchain-community llama-index openai anthropic guidance instructor

# Local Models & Hugging Face Stack
uv add transformers datasets accelerate diffusers sentence-transformers huggingface-hub

# Classical ML & AI Foundations
uv add scikit-learn numpy scipy pandas matplotlib

# Deep Learning Frameworks (Pick what you need)
uv add torch torchvision torchaudio                      # PyTorch
uv add tensorflow-cpu                                    # TensorFlow (CPU)
uv add jax jaxlib                                         # JAX

# Fine-Tuning & Model Optimization
uv add peft trl bitsandbytes vllm

uv add langchain langchain-community llama-index openai anthropic transformers sentence-transformers

uv add torch transformers datasets accelerate diffusers sentence-transformers peft

uv add scikit-learn pandas numpy matplotlib transformers torch openai

npx gitignore python

npx skills add bmad-code-org/BMAD-METHOD

bmad setup
