# Running-llama3.2-using-Ollama
### ✅ Step 1: **Running LLaMA 3 with Ollama**

#### 1. **Install Ollama**
Install the Ollama from the below website. Make sure you have installed a appropriate version, I mean if you are using a windows laptop download the windows installer and if you are using macbook then install the macbook installer.

> 🔗 Visit: https://ollama.com/download for manual downloads (macOS, Linux, Windows).

---

#### 2. **Start Ollama **
Make sure the Ollama is functional and  is running (we need to take terminal in macbook and windows powershell in windows laptop, then execute the below prompt):

```bash
ollama run llama3
```

> It will automatically download the latest `llama3` model (e.g., `llama3:8b`).

---

#### 3. **Use the Model in Terminal**
Once pulled, you can chat with the model:

```bash
ollama run llama3
```

Or specify a model like:

```bash
ollama run llama3:8b
```

---

#### 4. **Use Programmatically (Optional)**
Install the Python package (if building an app):

```bash
pip install ollama
```

Then use in Python:

```python
import ollama

response = ollama.chat(model='llama3', messages=[
  {'role': 'user', 'content': 'Tell me about quantum computing.'}
])

print(response['message']['content'])
```

---

### ✅ Step 2: **Create Your GitHub Project**

#### 1. **Create a Local Project Folder**

```bash
mkdir llama3-ollama-project
cd llama3-ollama-project
```

#### 2. **Add Python Script**

Example file structure:

```
llama3-ollama-project/
│
├── app.py         # Your main Python script
├── README.md      # Documentation
└── requirements.txt
```

Example `requirements.txt`:
```
ollama
```

---

#### 3. **Initialize Git and Push to GitHub**

```bash
git init
git add .
git commit -m "Initial commit: llama3 with ollama"
gh repo create llama3-ollama-project --public --source=. --remote=origin
git push -u origin main
```

> Note: Make sure you have GitHub CLI (`gh`) installed and authenticated.

---

### ✅ Step 3: **README.md Sample**

```md
# 🦙 LLaMA 3 with Ollama

This project demonstrates how to run Meta's LLaMA 3 locally using [Ollama](https://ollama.com/).

## 🚀 Setup

1. Install Ollama:
   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ```

2. Run LLaMA 3:
   ```bash
   ollama run llama3
   ```

3. Python Integration:
   ```bash
   pip install -r requirements.txt
   python app.py
   ```

## 🧠 Example

Ask the model:

```python
response = ollama.chat(model='llama3', messages=[
  {'role': 'user', 'content': 'Explain LLaMA 3 architecture.'}
])
```

## 🛠 Requirements

- Python 3.8+
- Ollama
```

---

Would you like me to generate the code (`app.py`, `README.md`, and `requirements.txt`) and help you push to GitHub right now?
