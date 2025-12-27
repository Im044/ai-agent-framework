# AI Agent Framework - Setup Steps

## Prerequisites
- Python 3.8+
- pip or conda
- Git
- Docker (optional, for containerized deployment)

## Installation Steps

### Step 1: Clone Repository
```bash
git clone https://github.com/Im044/ai-agent-framework.git
cd ai-agent-framework
```

### Step 2: Create Virtual Environment
```bash
# Using venv
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Or using conda
conda create -n ai-agent python=3.10
conda activate ai-agent
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Configure Environment
```bash
cp .env.example .env
# Edit .env with your API keys (OpenAI, etc)
```

### Step 5: Run Agent
```bash
python agent.py
```

## Docker Setup (Optional)

```bash
docker build -t ai-agent .
docker run -e OPENAI_API_KEY=your_key ai-agent
```

## Features Included
- Autonomous reasoning with Think-Act loops
- Tool integration (Search, Calculator, Memory)
- Vision capabilities (Image processing)
- Memory management and conversation history
- Multi-step reasoning
- LLM integration (OpenAI, Claude, LLaMA)

## Testing
```bash
pytest tests/
```

## Configuration
Edit `config.json` to customize:
- Model selection
- Tool availability
- Memory settings
- Reasoning depth

## Troubleshooting
- Missing dependencies: `pip install -r requirements.txt`
- API errors: Check your API keys in .env
- Memory errors: Reduce max_steps in agent configuration
