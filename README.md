
Go Web Server (GOPATH style)
# Go Web Server Project

A simple Go web server that serves a static HTML page and handles form submissions.

This project is designed for learning Go and practicing basic web server concepts without using Go modules. The project is located inside the `GOPATH/src` folder.

---

## 🏗️ Project Structure

GOPATH/src/go-server/
├── main.go        # Go server code
└── static/
└── index.html # Static HTML page with a form


- `main.go` contains the Go server logic  
- `static/` contains the HTML file for the website  

> Note: This project does **not use Go modules**, so it must stay in the `GOPATH/src` folder to build.

---

## 🚀 Features

1. Serves a static HTML page at `/`  
2. Handles form submissions at `/form` (POST request)  
3. Displays the submitted `name` and `address` in the browser  
4. Provides a simple `/hello` endpoint that returns `hello!`  

---

## ⚡ How It Works

1. **Start the server**  
   Open terminal in `GOPATH/src/go-server` and run:
   ```bash
   go run main.go

Server listens on port `8080`.

2. **Visit the page**
   Open your browser:

   ```
   http://localhost:8080/
   ```

   You will see the HTML form.

3. **Submit the form**

   * Enter `name` and `address`
   * Click **Submit**
   * The server responds with the entered data

4. **Visit `/hello`**

   ```
   http://localhost:8080/hello
   ```

   Returns `hello!` (GET request only)

---

## 📝 HTML Form Rules

* All input elements **must be inside the `<form>` tag**
* Form must have `method="POST"` and `action="/form"`
* Example:

```html
<form method="POST" action="/form">
  <input name="name" placeholder="Name">
  <input name="address" placeholder="Address">
  <button type="submit">Submit</button>
</form>
```

---

## ⚙️ Commands

**Run the project locally:**

```bash
cd $GOPATH/src/go-server
go run main.go
```

**Build the project (optional):**

```bash
go build
./go-server
```

**Push to GitHub (from VS Code terminal):**

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/go-server.git
git push -f origin main
```

---

## 📚 Learning Goals

This project helps you understand:

* Go project structure in `GOPATH/src`
* HTTP server in Go (`net/http`)
* Handlers and routes (`http.HandleFunc`)
* Form handling (`r.ParseForm()` and `r.FormValue()`)
* Serving static files (`http.FileServer`)
* Using Git and GitHub for project management

---

## 🧠 Notes / Tips

* Inputs **outside `<form>` are ignored**
* Use `<br>` or `<p>` tags to make output readable
* You can expand this project by:

  * Adding CSS/JS for styling
  * Using Go templates (`html/template`)
  * Storing form data in memory or a file


---

