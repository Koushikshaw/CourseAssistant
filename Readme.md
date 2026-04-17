# Agentic AI Course Assistant — Streamlit Deployment

## Files in this repo

| File | Purpose |
|------|---------|
| `capstone_streamlit.py` | Streamlit UI — run this |
| `agent.py` | Shared agent module (state, nodes, graph) |
| `requirements.txt` | Python dependencies |
| `pdfs/` | Your course PDF files (add them here) |

---

## Local Setup

```bash
# 1. Clone your repo
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO

# 2. Install dependencies
pip install -r requirements.txt

# 3. Create .env with your Groq API key
echo "GROQ_API_KEY=your_key_here" > .env

# 4. Add your PDFs
mkdir pdfs
# copy your 12 PDF files into pdfs/

# 5. Run
streamlit run capstone_streamlit.py
```

---

## Deploy to Streamlit Cloud (Free)

1. **Push to GitHub**
   ```bash
   git init
   git add capstone_streamlit.py agent.py requirements.txt pdfs/
   git commit -m "Agentic AI capstone"
   git push origin main
   ```

2. **Go to [share.streamlit.io](https://share.streamlit.io)**
   - Sign in with GitHub
   - Click **"New app"**
   - Select your repo, branch `main`, and set **Main file path** to `capstone_streamlit.py`

3. **Add your secret API key**
   - In the app settings → **Secrets**, add:
     ```toml
     GROQ_API_KEY = "your_groq_api_key_here"
     ```

4. **Click Deploy** — your app goes live with a public URL!

---

## Important: PDFs in the repo

Your PDF files are loaded from the `pdfs/` folder at startup.
Make sure all 12 PDFs are committed to the repo:
- Autonomous_Agents.pdf
- Deployment.pdf
- Embeddings.pdf
- Evaluation.pdf
- LangChain.pdf
- LangGraph.pdf
- LLM_API_Agents.pdf
- Memory_systems.pdf
- MultiAgent.pdf
- RAG.pdf
- RagMemory.pdf
- Tool_Calling.pdf

> **Note:** If your PDFs are large, Git LFS or storing them in Google Drive 
> and downloading at startup are alternatives. But for typical course PDFs, 
> committing them directly is the simplest approach.