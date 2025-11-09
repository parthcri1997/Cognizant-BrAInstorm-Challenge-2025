
# ReVogue - Hackathon Project

**Tagline:** *"Fashion Forward. Planet Friendly."*  

ReVogue is an AI-driven solution that helps users make sustainable fashion choices by analyzing clothing impact and promoting circular economy practices. Judges and mentors can follow this guide to quickly run and explore the solution.

---

## Quick Start

1. Clone the repository and check out your feature branch:

```bash
git clone <your-repo-url>
cd Cognizant_BrAInstorm_challenge_hackathon_2025/CarbonTool
git checkout <feature-branch>
```

2. Set up a Python virtual environment and install dependencies:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
.\venv\Scripts\activate.bat
pip install --upgrade pip
pip install --no-cache-dir -r requirements.txt
```

3. **Set your OpenAI API key**:  
Open `backend/main.py` and replace the placeholder `OPENAI_API_KEY` with your OpenAI API key:

```python
OPENAI_API_KEY = "your_openai_api_key_here"  # Replace this with your key
```

4. Run the backend server locally:

```bash
uvicorn backend.main:app --reload
```

5. Open the frontend HTML page directly in a browser:

```text
frontend/index.html
```

> No installation or frontend server is required. All frontend interactions will call the running backend API.

---

## Local Run Commands

| Step       | Command                                                                                     | Notes                                      |
|------------|---------------------------------------------------------------------------------------------|-------------------------------------------|
| Install    | `python -m venv venv && .\venv\Scripts\activate.bat && pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt` | Creates virtualenv and installs dependencies |
| Server      | `uvicorn backend.main:app --reload`                                                         | Starts backend API at `http://127.0.0.1:8000` |
| Frontend   | Open `frontend/index.html` in a browser                                                     | Static HTML page; no server required      |

---

## Environment Variables (Temporary)

> For the hackathon/demo, just replace `OPENAI_API_KEY` directly in `main.py`.

| Name              | Purpose                  | Example                  |
|------------------|--------------------------|-------------------------|
| `OPENAI_API_KEY`  | Access OpenAI API         | `"sk-xxxxxxxxxxxxxxxx"` |
| `DATA_PATH`       | Path to input dataset (if needed) | `"data/dataset.csv"`    |

---

## Hosted Demo / Video
  
- **Video walkthrough:** [Add URL here](https://example.com/video)

---

## Troubleshooting

- **Issue:** `venv not activating / script execution blocked`  
  **Resolution:** Run `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` in PowerShell.  

- **Issue:** Dependencies fail to install  
  **Resolution:** Upgrade pip `pip install --upgrade pip` and use `--no-cache-dir`.  

- **Issue:** Backend server not running  
  **Resolution:** Ensure `uvicorn` is installed and `OPENAI_API_KEY` is set correctly in `main.py`.  

---

## Notes for Judges

- Replace `OPENAI_API_KEY` in `backend/main.py` with your key.  
- Run the backend with `uvicorn backend.main:app --reload`.  
- Open the `frontend/index.html` file in a browser to interact with ReVogue.  
- All outputs (JSON or predictions) are served via API endpoints from the backend.  

---

ReVogue empowers users to make **fashion choices that are stylish, ethical, and sustainable**—combining AI insights with environmental consciousness.
