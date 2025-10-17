<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Grantwell Blog</title>
  <link rel="stylesheet" href="/assets/css/style.css">
  <style>
    body {
      font-family: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      margin: 0;
      background-color: #ffffff;
      color: #111;
      line-height: 1.6;
    }
    header {
      background-color: #003366;
      color: white;
      padding: 2rem 1rem;
      text-align: center;
    }
    header p {
      margin-top: 0.5rem;
      font-weight: 300;
      font-size: 1rem;
    }
    main {
      max-width: 800px;
      margin: 2rem auto;
      padding: 0 1rem;
    }
    .post-list {
      list-style: none;
      padding: 0;
    }
    .post-list li {
      margin-bottom: 2rem;
      border-bottom: 1px solid #eee;
      padding-bottom: 1rem;
    }
    .post-list a {
      color: #003366;
      text-decoration: none;
      font-weight: 600;
      font-size: 1.1rem;
    }
    .post-list a:hover {
      text-decoration: underline;
    }
    .post-list small {
      color: #666;
      font-size: 0.85rem;
    }
    footer {
      background-color: #f5f5f5;
      color: #666;
      text-align: center;
      padding: 1rem;
      font-size: 0.9rem;
      margin-top: 3rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>Grantwell Blog</h1>
    <p>Insights on public safety grant management, funding automation, and compliance.</p>
  </header>

  <main>
    <h2 style="font-size:1.3rem; margin-bottom:1rem;">Latest Posts</h2>
    <ul class="post-list">
      {% for post in site.posts %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
          <small>{{ post.date | date: "%B %d, %Y" }}</small>
          {% if post.excerpt %}
            <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
          {% endif %}
        </li>
      {% endfor %}
    </ul>
  </main>

  <footer>
    © 2025 Grantwell — Purpose-built grant management for public safety agencies.
  </footer>
</body>
</html>
