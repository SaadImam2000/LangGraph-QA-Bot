# LangGraph-QA-Bot
An enterprise-grade AI assistant built with LangGraph, featuring RAG (Retrieval Augmented Generation), intelligent tool routing, conversation memory, caching, rate limiting, and production-ready optimizations.

✨ Features
Core Capabilities

🧮 Calculator Tool - Safe mathematical expression evaluation
📚 RAG System - Document Q&A with confidence scoring and source attribution
📄 File Reader - Read text files with security validation
🔍 Memory Search - Intelligent conversation history search with relevance ranking
💬 Natural Chat - Context-aware conversational AI

Production Features

⚡ Response Caching - LRU cache with TTL for faster responses
🛡️ Rate Limiting - Prevent abuse with configurable limits
📊 Metrics Tracking - Monitor performance and usage patterns
🎯 Intent Detection - Smart routing to appropriate tools
🔄 Error Recovery - Robust error handling with retry logic
📈 Confidence Scoring - Know when to trust RAG results

🚀 Quick Start
Installation
bash# 
Clone repository
git clone https://github.com/SaadImam2000/langgraph-qa-bot.git
cd langgraph-qa-bot

# Install dependencies
pip install -r requirements.txt

# Run the application
langgraph_bot.py

Google Colab

!pip install -r requirements.txt
!python langgraph_bot.py

📋 Requirements

Python 3.9+
8GB+ RAM (16GB recommended)
GPU optional (CPU mode works but slower)

🎯 Usage Examples

Calculator
User: Calculate (155 * 8 + 42) / 7
Bot: ✅ Result: 183.142857

Document Q&A
User: What are the company's work hours?
Bot: Regular hours are 9:00 AM to 5:00 PM, Monday through Friday...
     🟢 Sources: sample_policy.txt

Memory Search
User: What did we discuss about benefits?
Bot: 🔍 Found 3 matching messages:
     Message 2/10 - You: Tell me about benefits

⚙️ Configuration
Environment Variables
bash# Optional: Disable Gradio analytics
export GRADIO_ANALYTICS_ENABLED=False

# Optional: Custom cache settings
export CACHE_MAX_SIZE=100
export CACHE_TTL_SECONDS=3600

📊 Performance

Average Latency: <100ms (cached), 2-5s (uncached)
Cache Hit Rate: 60-80% in typical usage
Throughput: 10+ queries/second
Memory: ~4GB with Phi-3 model

🔧 Troubleshooting
Out of Memory

Reduce model size: Use google/flan-t5-base instead of Phi-3
Decrease chunk size in RAG: chunk_size=400
Clear cache frequently: Click "Clear Cache" button

Slow Responses

Enable response caching (default)
Use smaller embedding model
Reduce max_steps: max_steps=10

PDF Upload Issues

Check file size (<10MB)
Ensure text-based PDF (not scanned images)
Use PDF/A format when possible

🤝 Contributing
Contributions welcome! Please:

Fork the repository
Create feature branch (git checkout -b feature/amazing-feature)
Commit changes (git commit -m 'Add amazing feature')
Push to branch (git push origin feature/amazing-feature)
Open Pull Request

See CONTRIBUTING.md for detailed guidelines.

📄 License
This project is licensed under the MIT License - see LICENSE file.

🙏 Acknowledgments

Built with LangChain and LangGraph
Uses Gradio for web interface
Powered by Hugging Face Transformers

Star ⭐ this repo if you find it useful!
