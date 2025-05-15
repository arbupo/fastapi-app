uv venv 
source .venv/bin/activate
uv pip install fastapi "uvicorn[standard]"
uv freeze > requierements.txt
uvicorn app.main:app --reload