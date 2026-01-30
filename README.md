# 🚀 AI-Powered PDF Document Summarizer

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.41.0-red)
![Groq](https://img.shields.io/badge/Groq-API-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

**Transform lengthy PDF documents into concise, AI-generated summaries**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Demo](#-demo) • [Contributing](#-contributing)

</div>

---

## 📋 Overview

AI PDF Summarizer is a powerful cloud-based application that leverages advanced Large Language Models (LLMs) to automatically generate intelligent summaries from PDF documents. Built with Streamlit and powered by Groq's ultra-fast AI models, it offers multiple summarization strategies to suit different needs.

### 🎯 Key Highlights

- **Lightning Fast**: Powered by Groq's optimized inference engine
- **Multiple AI Models**: Choose from GPT-OSS 120B, LLaMA 3 70B, and Gemma 7B
- **5 Summarization Strategies**: Extractive, Abstractive, Bullet Points, Question-Based, and Key Insights
- **Cloud-Based**: No local installation of AI models required
- **Export Options**: Download summaries as TXT or PDF
- **100% Free**: Uses Groq's free API tier

---

## ✨ Features

### 🤖 AI-Powered Summarization
- **Extractive Summarization**: Selects and combines key sentences from the original text
- **Abstractive Summarization**: Generates new, concise summaries in AI's own words
- **Bullet Point Summary**: Creates organized bullet-point lists of key information
- **Question-Based Analysis**: Answers critical questions about the document
- **Key Insights**: Extracts top takeaways and actionable insights

### 📊 Advanced Analytics
- Real-time word count and statistics
- Compression ratio calculation
- Processing time tracking
- Summary quality metrics

### 💾 Export Capabilities
- Download as formatted TXT file
- Export as professional PDF with metadata
- Copy-friendly text output

### 🎨 Modern UI/UX
- Clean, responsive interface
- Real-time processing indicators
- Premium gradient design
- Mobile-friendly layout

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|------------|
| **Frontend** | Streamlit 1.41.0 |
| **AI Engine** | Groq API (Cloud LLM) |
| **PDF Processing** | PyPDF2 3.0.1 |
| **PDF Export** | FPDF2 2.8.1 |
| **Language** | Python 3.8+ |

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- Groq API key (free from [console.groq.com](https://console.groq.com))

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/ai-pdf-summarizer.git
cd ai-pdf-summarizer
```

### Step 2: Create Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Configure API Key

Create a `.streamlit/secrets.toml` file in the project root:

```toml
GROQ_API_KEY = "your-groq-api-key-here"
GROQ_MODEL = "llama-3.3-70b-versatile"
```

**Get your free Groq API key:**
1. Visit [console.groq.com](https://console.groq.com)
2. Sign up for a free account
3. Navigate to API Keys section
4. Generate a new API key
5. Copy and paste it into `secrets.toml`

### Step 5: Run the Application
```bash
streamlit run app.py
```

The app will open in your browser at `http://localhost:8501`

---

## 🚀 Usage

### Basic Workflow

1. **Upload PDF Document**
   - Click on the file uploader
   - Select a PDF file from your device
   - Wait for text extraction to complete

2. **Configure Settings** (in sidebar)
   - Select AI model (GPT-OSS 120B, LLaMA 3 70B, or Gemma 7B)
   - Choose summarization type
   - Adjust summary length (short, medium, long)

3. **Generate Summary**
   - Click "🚀 Generate AI Summary" button
   - Wait for AI processing (typically 5-15 seconds)
   - Review the generated summary

4. **Export Results**
   - Download as TXT for plain text
   - Download as PDF for formatted document
   - Copy text directly from the interface

### Summarization Types Explained

| Type | Description | Best For |
|------|-------------|----------|
| **Extractive** | Selects key sentences from original | Preserving exact wording, academic papers |
| **Abstractive** | Creates new summary in AI's words | General use, easier reading |
| **Bullet Points** | Organized list format | Quick scanning, presentations |
| **Question-Based** | Answers key questions | Analysis, research |
| **Key Insights** | Top takeaways and implications | Decision-making, executive summaries |

---

## 📁 Project Structure

```
ai-pdf-summarizer/
│
├── app.py                      # Main Streamlit application
├── requirements.txt            # Python dependencies
├── README.md                   # Project documentation
├── .gitignore                  # Git ignore rules
│
├── .streamlit/
│   └── secrets.toml           # API keys (DO NOT commit)
│
├── backend/                   # Backend modules
│   ├── __init__.py
│   ├── groq_client.py        # Groq API client
│   ├── cloud_summarizer.py   # Summarization logic
│   ├── pdf_extractor.py      # PDF text extraction
│   ├── exporter.py           # Export functionality
│   └── utils.py              # Utility functions
│
└── frontend/                  # Frontend components
    ├── __init__.py
    ├── components.py         # UI components
    └── styles.py             # Custom CSS styling
```

---

## 🌐 Deployment on Streamlit Cloud

### Quick Deploy

1. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Deploy on Streamlit Cloud**
   - Go to [share.streamlit.io](https://share.streamlit.io)
   - Click "New app"
   - Select your repository
   - Set main file as `app.py`

3. **Add Secrets**
   - In Streamlit Cloud dashboard
   - Go to App Settings → Secrets
   - Add:
     ```toml
     GROQ_API_KEY = "your-groq-api-key"
     GROQ_MODEL = "llama-3.3-70b-versatile"
     ```

4. **Deploy!**
   - Click "Deploy"
   - Wait for deployment to complete
   - Share your app URL!

---

## 🔧 Configuration

### Available Models

| Model | Description | Speed | Quality |
|-------|-------------|-------|---------|
| `openai/gpt-oss-120b` | Open-source GPT variant | Fast | Excellent |
| `llama-3.3-70b-versatile` | Meta's latest LLaMA | Very Fast | Excellent |
| `gemma-7b-it` | Google's efficient model | Ultra Fast | Good |

### Customization Options

Edit `backend/cloud_summarizer.py` to:
- Adjust prompt templates
- Modify summary lengths
- Add custom summarization strategies
- Change temperature/token settings

---

## 📊 Performance

- **Average Processing Time**: 5-15 seconds per document
- **Supported PDF Size**: Up to 10MB recommended
- **Context Window**: ~12,000 characters per request
- **Compression Ratio**: Typically 70-90% reduction

---

## 🐛 Troubleshooting

### Common Issues

**1. API Connection Error**
```
❌ Groq API Not Connected
```
**Solution**: Check your API key in `.streamlit/secrets.toml`

**2. Model Decommissioned Error**
```
❌ The model 'llama3-70b-8192' has been decommissioned
```
**Solution**: Update to `llama-3.3-70b-versatile` in your code

**3. PDF Encoding Error**
```
❌ Error: 'latin-1' codec can't encode character
```
**Solution**: Already fixed in latest version using FPDF2

**4. Text Extraction Failed**
```
❌ Could not extract text from PDF
```
**Solution**: Ensure PDF contains readable text (not scanned images)

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

### Development Setup

```bash
# Install development dependencies
pip install -r requirements.txt

# Run tests
python -m pytest tests/

# Format code
black .
flake8 .
```

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Groq** for providing ultra-fast AI inference
- **Streamlit** for the amazing web framework
- **Meta AI** for LLaMA models
- **Google** for Gemma models
- All contributors and users of this project

---

## 📧 Contact

**Project Maintainer**: Your Name

- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)

---

## 🔮 Roadmap

- [ ] Support for multi-language summarization
- [ ] Add OCR for scanned PDFs
- [ ] Batch processing of multiple PDFs
- [ ] Custom summary templates
- [ ] Integration with cloud storage (Google Drive, Dropbox)
- [ ] Advanced analytics dashboard
- [ ] API endpoint for programmatic access
- [ ] Support for other document formats (DOCX, TXT, etc.)

---

## ⭐ Star History

If you find this project useful, please consider giving it a star! ⭐

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/ai-pdf-summarizer&type=Date)](https://star-history.com/#yourusername/ai-pdf-summarizer&Date)

---

<div align="center">

**Made with ❤️ and AI**

[Report Bug](https://github.com/yourusername/ai-pdf-summarizer/issues) • [Request Feature](https://github.com/yourusername/ai-pdf-summarizer/issues)

</div>
