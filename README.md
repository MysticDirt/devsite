# My Developer Portfolio

Welcome to my personal developer website! This site showcases my projects, technical skills, and blog posts, and serves as a central hub for everything I'm working on.


---

## Tech Stack

- **Frontend**: [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML), [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS), [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- **Backend**: 
- **Deployment**: [Nginx](https://www.nginx.com/), [Linux](https://ubuntu.com/), [Git](https://git-scm.com/), [CI/CD](#-cicd)
- **Domain**: [chandrarkmuddana.com](https://chandrarkmuddana.com)

---

## Project Structure
my-website/<br>
├── public/ # Static assets<br>
├── src/ # Source code<br>
│ ├── components/ # Reusable UI components<br>
│ └── pages/ # Pages (if using Next.js)<br>
├── deploy.sh # Deployment script<br>
├── nginx.conf # Nginx config (if applicable)<br>
└── README.md # This file


---

## 🚀 Deployment

This site is deployed on a self-hosted VPS using `nginx` and `git`. Deployment is handled via a simple CI/CD workflow.

### CI/CD Flow

1. **Push** to `main` on GitHub
2. **Webhook** notifies the server
3. Server runs `deploy.sh`:

```bash
#!/bin/bash
cd /var/www/devsite
git pull origin main
npm install --production # or build command
npm run build            # if using a bundler or static site generator
sudo systemctl reload nginx
```
### Local Development
```bash
git clone https://github.com/MysticDirt/devsite.git
cd devsite
npm install           # or pip install -r requirements.txt if using Python
npm run dev           # or python manage.py runserver
```
## Features
- None at the moment

## To-Do
- Portfolio showcasing projects
- Blog posts
- Contact form and social media
- Add analytics