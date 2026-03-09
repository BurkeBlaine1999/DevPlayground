# DevPlayground

A free, zero-backend developer toolkit for practising SQL and testing APIs — hosted entirely on GitHub Pages with no server, no build step, and no running costs.

Built as a single `index.html` file, everything runs directly in your browser.

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

### ⚡ API Tester
A lightweight API testing tool similar to Postman.

- Send GET, POST, PUT, PATCH, and DELETE requests
- Custom request headers and JSON body editor
- Syntax-highlighted JSON response viewer
- Response headers inspector
- Test assertions (e.g. `status == 200`, `body.id == 1`)
- Save and reload requests from a local collection

Here are some sample API calls to try out!

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

## Tech Stack

- [sql.js](https://github.com/sql-js/sql.js) — SQLite compiled to WebAssembly, runs entirely in the browser
- [Fira Code](https://fonts.google.com/specimen/Fira+Code) & [Syne](https://fonts.google.com/specimen/Syne) — Google Fonts
- Vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies

---

## About

This project was created with the assistance of [Claude](https://claude.ai)
