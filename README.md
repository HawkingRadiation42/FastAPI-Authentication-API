# FastAPI-Auth
Example app using FastAPI and JWT

```
pip3 install -r requirements.txt
gunicorn -w 1 -k uvicorn.workers.UvicornWorker api:app --bind=0.0.0.0:5002
```

Requires external user management, or generate a password using
```
python3 -c "import bcrypt; print(bcrypt.hashpw('testtest'.encode('utf-8'), bcrypt.gensalt(10)).decode())"
$2b$10$YbleoHiOWO.gTG/ToE1TAO9wGbQou5.u3bfbIEBbbqsx/8Q4GC.FC
```
Where `testtest` is the password.
