[繁體中文](./README.md) · **English** · [日本語](./README.ja.md)

# Blog System - Exercise 6

This is a simple blog built with Deno and SQLite. It lets you create and display posts.

## Features

- Display all posts in chronological order.
- Create posts with a title and body.
- Automatically record the publication time.
- Includes a script that automatically creates three posts.

## Running the blog

### Step 1: Create three posts

Run this command to add the three sample posts:

```
deno run --allow-net --allow-read --allow-write addPosts.js
```

### Step 2: Start the blog app

Run this command to start the app:

```
deno run --allow-net --allow-read --allow-write blogApp.js
```

### Step 3: Open the blog

Open the following URLs in your browser:

- Home: http://localhost:8000
- Create a post: http://localhost:8000/new

## Technology

- **Deno**: A secure runtime for JavaScript and TypeScript.
- **Oak**: Middleware for Deno, similar to Express for Node.js.
- **SQLite**: A lightweight relational database.
- **HTML/CSS**: Used for the frontend.

## Database schema

The blog uses a table called `posts`:

```sql
CREATE TABLE IF NOT EXISTS posts (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT NOT NULL,
  content TEXT NOT NULL,
  created_at TEXT DEFAULT (datetime('now','localtime'))
)
```

## About the exercise

This system meets the Exercise 6 requirement to write a program that adds three posts. Running `addPosts.js` creates three posts, each with a title and body. The web interface also lets you add more posts by hand.
