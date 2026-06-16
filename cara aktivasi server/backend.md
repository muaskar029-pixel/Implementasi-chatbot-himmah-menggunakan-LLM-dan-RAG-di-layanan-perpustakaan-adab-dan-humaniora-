backend
```
cd ~/Projects/llm-perpus-web/backend/
```
```
source .venv/bin/activate.fish
  python -m pip install -r requirements.txt
  python -m uvicorn app.main:app --host 127.0.0.1 --port 8000 --reload
```
frontend
```
cd ~/Projects/llm-perpus-web/frontend
```
```
 npm run dev
```
