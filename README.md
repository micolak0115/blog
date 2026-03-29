# My CV + Blog on GitHub Pages

A single-file CV with an embedded blog — no build tools, no frameworks, just HTML.

## 🚀 How to Deploy

1. Create a repo named `yourusername.github.io` on GitHub
2. Drop `index.html` into the root of the repo
3. Push to GitHub — your site is live in ~60 seconds

## ✍️ How to Add a Blog Post

### Option A: Write in the browser
1. Go to your site → click **+ New Post**
2. Write your idea (or drag & drop a `.md` / `.txt` file)
3. Click **Export as HTML** → file downloads
4. Put the file in `blog/posts/` in your repo
5. Open `index.html`, find the `posts` array in the `<script>` block
6. Add a new entry:
```js
{
  id: 4,
  title: "Your New Post Title",
  date: "2026-03-29",
  summary: "One sentence overview.",
  tags: ["tag1", "tag2"],
  content: `Your content here.\n\nNew paragraph.\n\n### A Heading\n\nMore text.`
},
```
7. `git add . && git commit -m "New post" && git push`

### Option B: Write directly in the array
Edit `index.html`, scroll to the `posts` array in the JavaScript section, and add your post. Same format as above.

## 📁 File Structure

```
yourusername.github.io/
└── index.html        ← Everything lives here
```

That's it. One file. No dependencies.

## 🎨 Customising Your CV

Edit `index.html` — find these sections:
- `<h1>Your Name</h1>` → change your name
- `.avatar` → change the initials
- Contact items → update email, location, GitHub
- Skill tags → add/remove your skills
- Experience items → replace with your real experience

## Content Formatting in Posts

Inside the `content` field, use these conventions:
- Blank line (`\n\n`) = new paragraph
- `### Heading` = section heading
- `> Quote text` = blockquote
- `1. Item` = numbered list
