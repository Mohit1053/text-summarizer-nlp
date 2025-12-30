# 🛒 Product Recommendation System

[![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)](https://python.org/)
[![Sentence Transformers](https://img.shields.io/badge/Sentence_Transformers-2.0+-red)](https://www.sbert.net/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An intelligent product recommendation system using semantic similarity and sentence transformers. Analyzes conversation context to recommend relevant products across multiple categories.

## ✨ Features

- 🔍 **Semantic Understanding** - Uses sentence transformers for context analysis
- 🛍️ **Multi-Category Products** - Technology, entertainment, fashion, health, food
- 📊 **Cosine Similarity Matching** - Accurate product relevance scoring
- 💬 **Conversation Analysis** - Extracts intent from natural language
- 🎯 **Keyword Matching** - Hybrid approach for better accuracy
- 📈 **SamSum Integration** - Text summarization capabilities

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- ~500MB for sentence transformer model

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/product-recommendation.git
   cd product-recommendation
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the system**
   ```bash
   python product_recommendation_system.py
   ```

## 📁 Project Structure

```
product-recommendation/
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   ├── ISSUE_TEMPLATE.md
│   └── PULL_REQUEST_TEMPLATE.md
├── src/
│   ├── product_recommendation_system.py  # Main recommendation engine
│   └── SamSum.py                          # Text summarization
├── data/
│   └── samsum_data/                       # Training data
├── .gitignore
├── .env.example
├── requirements.txt
├── LICENSE
├── CONTRIBUTING.md
├── CHANGELOG.md
└── README.md
```

## 🛍️ Product Categories

| Category | Example Products |
|----------|------------------|
| Technology | Smartphones, Apps |
| Entertainment | Netflix, Concerts |
| Fashion | Clothing, Accessories |
| Health | Supplements, Ergonomic furniture |
| Food | Meal delivery services |
| Books | E-readers, Book subscriptions |

## 🔧 How It Works

1. **Input Processing** - Receives conversation or query text
2. **Embedding Generation** - Creates semantic embeddings using `all-MiniLM-L6-v2`
3. **Similarity Calculation** - Computes cosine similarity with product database
4. **Keyword Enhancement** - Boosts matches based on keyword overlap
5. **Ranking** - Returns top-N most relevant products

## 💻 Usage Example

```python
from product_recommendation_system import ProductRecommendationSystem

recommender = ProductRecommendationSystem()

# Get recommendations from conversation
conversation = "I've been feeling tired lately and need more energy for work."
recommendations = recommender.get_recommendations(conversation)

for product in recommendations:
    print(f"{product['name']}: {product['score']:.2f}")
```

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md).

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Your Name**

- GitHub: [@yourusername](https://github.com/yourusername)

---

<p align="center">Made with ❤️ and Sentence Transformers</p>
