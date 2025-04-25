---
const post = {
  title: 'My First Blog Post',
  pubDate: '2024-12-01',
  description: 'This is the first post of my new Astro blog.',
  author: 'Astro Learner',
  image: {
    url: 'https://docs.astro.build/assets/rose.webp',
    alt: 'The Astro logo on a dark background with a pink glow.',
  },
  tags: ['astro', 'blogging', 'learning in public'],
};
---

<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>{post.title}</title>
    <meta name="description" content={post.description} />
    <style>
      body {
        font-family: system-ui, sans-serif;
        max-width: 700px;
        margin: 2rem auto;
        line-height: 1.6;
        padding: 0 1rem;
      }
      h1 {
        color: #333;
      }
      h2 {
        color: #555;
        margin-top: 2rem;
      }
      img {
        max-width: 100%;
        border-radius: 8px;
        margin: 1rem 0;
      }
      code {
        background: #f4f4f4;
        padding: 2px 5px;
        border-radius: 4px;
        font-family: monospace;
      }
    </style>
  </head>
  <body>
    <article>
      <h1>{post.title}</h1>
      <p><strong>Published on:</strong> {post.pubDate}</p>
      <p><strong>Author:</strong> {post.author}</p>
      <img src={post.image.url} alt={post.image.alt} />

      <p>Welcome to my <em>new blog</em> about <em>learning</em> Astro! Here, I will share my learning journey as I build a new website.</p>

      <h2>What I've accomplished</h2>

      <ol>
        <li>
          <strong>Installing Astro</strong>: First, I created a new Astro project and set up my online accounts.
        </li>
        <li>
          <strong>Making Pages</strong>: I then learned how to make pages by creating new <code>.astro</code> files and placing them in the <code>src/pages/</code> folder.
        </li>
        <li>
          <strong>Making Blog Posts</strong>: This is my first blog post! I now have Astro pages and Markdown posts!
        </li>
      </ol>

      <h2>What's next</h2>

      <p>🪐 I will finish the Astro tutorial, and then keep adding more posts.<br />
      Watch this space for more to come.</p>
    </article>
  </body>
</html>
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>Astro</title>
  </head>
  <body>
    <a href="/">Home</a>
    <a href="/about/">About</a>
    <a href="/blog/">Blog</a>

    <h1>My Astro Learning Blog</h1>
    <p>This is where I will post about my journey learning Astro.</p>

    <ul>
      <li><a href="/blog/post-1/">Post 1</a></li>
    </ul>
  </body>
</html>
 ---
import Navigation from '../components/Navigation.astro';
import Footer from '../components/Footer.astro';
import "../styles/global.css";

const pageTitle = 'My Astro Site';
---

<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" type="image/svg+xml" href="/favicon.svg" />
    <meta name="viewport" content="width=device-width" />
    <meta name="generator" content={Astro.generator} />
    <title>{pageTitle}</title>
  </head>
  <body>
    <Navigation />

    <h1>{pageTitle}</h1>
