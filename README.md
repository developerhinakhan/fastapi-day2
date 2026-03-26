# 🚀 FastAPI Beginner Project — Day 2

This is my Day 2 project while learning FastAPI.
In this project, I created a basic FastAPI application and rendered an HTML page using templates.

---

## 📌 What I Learned

* Creating a FastAPI app
* Understanding routes (`@app.get`)
* Working with request objects
* Using Jinja2 templates
* Connecting backend (FastAPI) with frontend (HTML)
* Understanding project structure
* Debugging errors (Internal Server Error)

---

## 📁 Project Structure

```
project/
│── main.py
│── templates/
│     └── home.html
```

---

## 🧠 How It Works

1. User opens:

   ```
   http://127.0.0.1:8000/
   ```
2. FastAPI catches the request using a route
3. The function runs
4. `TemplateResponse` loads the HTML file
5. HTML is sent back to the browser

---

## 🧾 Code

### main.py

```python
from fastapi import FastAPI, Request
from fastapi.templating import Jinja2Templates

app = FastAPI()
templates = Jinja2Templates(directory="templates")

@app.get("/")
def home(request: Request):
    return templates.TemplateResponse(
        request=request,
        name="home.html",
        context={}
    )
```

---

### templates/home.html

```html
<h1>Hello World</h1>
```

---

## ▶️ How to Run

### Using uv:

```bash
uv run uvicorn main:app --reload
```

---

## 🌐 Open in Browser

```
http://127.0.0.1:8000/
```

---

## 📚 Next Steps

* Passing data from Python to HTML
* Multiple routes
* Forms (GET/POST)
* Building APIs (JSON responses)

---

## 💡 Notes

This is part of my learning journey.
I am focusing on understanding concepts step-by-step.

---

## 📌 Author

Learning FastAPI step by step 🚀
