uv venv 
source .venv/bin/activate
uv pip install fastapi "uvicorn[standard]"
uv freeze > requierements.txt
uvicorn app.main:app --reload


docker build -t arbupo/fastapi-app:latest .
docker run -p 8000:8000 arbupo/fastapi-app:latest
docker push arbupo/fastapi-app:latest 