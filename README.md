# [DevPlayground](https://burkeblaine1999.github.io/DevPlayground/)

A free, zero-backend developer toolkit for practising SQL, testing APIs, visualising JSON, and experimenting with regex.

---

## Features

### ⬡ SQL Playground

An interactive SQL editor powered by SQLite (via sql.js), similar to LeetCode's SQL environment.

- Three built-in sample databases: E-Commerce, HR/Employees, and Library
- Write and run any SQL query in the browser — no backend needed
- Collapsible schema browser with click-to-insert column names
- Import your own custom schema by pasting `CREATE TABLE` and `INSERT INTO` statements
- Resizable editor pane
- `Ctrl + Enter` keyboard shortcut to run queries

**Sample query to try:**
```sql
SELECT
  c.name,
  c.country,
  COUNT(o.id) AS num_orders,
  ROUND(SUM(o.total), 2) AS total_spent
FROM customers c
JOIN orders o ON c.id = o.customer_id
GROUP BY c.id, c.name, c.country
ORDER BY total_spent DESC;
```

**Custom schema sample** — paste into the Custom Schema modal:
```sql
CREATE TABLE users (id INTEGER, name TEXT, email TEXT, age INTEGER);
INSERT INTO users VALUES
  (1, 'Alice', 'alice@example.com', 30),
  (2, 'Bob', 'bob@example.com', 25);
```

---

### ⚡ API Tester

A lightweight API testing tool similar to Postman.

- Send GET, POST, PUT, PATCH, and DELETE requests
- Custom request headers and JSON body editor
- Syntax-highlighted JSON response viewer
- Response headers inspector
- Test assertions (e.g. `status == 200`, `body.id == 1`)
- Save and reload requests from a local collection

**Sample API calls to try:**

Country data
```
https://restcountries.com/v3.1/name/ireland
```

Pokémon data
```
https://pokeapi.co/api/v2/pokemon/pikachu
```

Live Dublin weather
```
https://api.open-meteo.com/v1/forecast?latitude=53.33&longitude=-6.25&current_weather=true
```

---

### ❴❵ JSON Visualiser

A tool for exploring and debugging JSON — paste any JSON and it renders as an interactive collapsible tree.

- Collapsible/expandable tree view with key and depth metadata
- Highlights and explains invalid JSON with clear error messages
- Search bar highlights matching keys and auto-expands their parents
- Collapse All / Expand All controls

**Sample JSON to paste and parse:**
```json
{
  "company": "Software ltd",
  "founded": 2000,
  "active": true,
  "headquarters": {
    "city": "Dublin",
    "country": "Ireland",
    "coordinates": {
      "lat": 53.3498,
      "lng": -6.2603
    }
  },
  "departments": [
    { "name": "Engineering", "headcount": 120, "lead": "Sarah Johnson" },
    { "name": "QA", "headcount": 45, "lead": "Mike Davis" }
  ],
  "techStack": ["Java", "Spring Boot", "React", "AWS", "Docker"],
  "remote": true,
  "notes": null
}
```

**Things to try:**
- Search `name` to highlight and expand all matching keys
- Click the `▶` arrows to collapse individual nodes
- Paste `{ "broken": json` to see the error highlighting

---

### ✦ Regex Playground

A live regex tester with match highlighting, token explanation, and a built-in cheat sheet.

- Live match highlighting as you type — alternating colours for each match
- **Explain tab** — breaks down every token in your pattern
- **Matches tab** — lists every match with its exact index and length
- **Cheat Sheet tab** — click any token to insert it directly into your pattern
- Supports all standard JS regex flags (`g`, `i`, `m`, `s`)

**Sample test string:**
```
Contact us at hello@devtools.io or support@example.com
Phone: +353 89 765 4321 or +1 (555) 123-4567
Visit https://www.devtools.io or http://example.github.io
Order #A1042 and #B2891 were shipped on 2024-03-15 and 2024-04-02
The price was $19.99, reduced from $34.99
IP address: 192.168.0.1 — last login: 2024-06-01 at 08:45
```

**Sample patterns to try:**

| Pattern | Flags | Matches |
|--------|-------|---------|
| `[\w.-]+@[\w.-]+\.\w+` | `g` | Email addresses |
| `https?:\/\/[\w./-]+` | `g` | URLs |
| `#[A-Z]\d+` | `g` | Order numbers |
| `\d{4}-\d{2}-\d{2}` | `g` | Dates |
| `\b[A-Z][a-z]+\b` | `g` | Capitalised words |

---

## Tech Stack

- [sql.js](https://github.com/sql-js/sql.js) — SQLite compiled to WebAssembly, runs entirely in the browser
- [Fira Code](https://fonts.google.com/specimen/Fira+Code) & [Syne](https://fonts.google.com/specimen/Syne) — Google Fonts
- Vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies

---

## About

This project was created with the assistance of [Claude](https://claude.ai)
