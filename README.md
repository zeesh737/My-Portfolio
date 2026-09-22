# Zeesh Portfolio — Node/Express Edition

This is your original static portfolio template, restructured as a Node/Express
app. The `contact.php` + PHPMailer handler has been replaced with a Node route
powered by **Nodemailer** — same behavior, no PHP required.

## Project structure

```
zeesh-portfolio-node/
├── public/              # everything served as static files
│   ├── index.html       # default landing page (copy of index-light.html)
│   ├── index-*.html     # the other 7 theme variants
│   ├── css/
│   ├── js/               (app.js, typewriter.js)
│   ├── webfonts/
│   └── img/
│       ├── clients/     # empty — add your client logos here
│       └── projects/    # empty — add your project screenshots here
├── src/
│   ├── server.js        # starts the server
│   ├── app.js            # express app: middleware, static files, routes
│   ├── routes/
│   │   └── contact.routes.js
│   ├── controllers/
│   │   └── contact.controller.js   # validates input, calls the mailer
│   ├── services/
│   │   └── mailer.service.js       # Nodemailer SMTP logic
│   ├── middlewares/
│   │   └── errorHandler.js
│   └── config/
│       └── env.js        # reads/centralizes .env values
├── .env.example
├── .gitignore
└── package.json
```

## Setup

```bash
npm install
cp .env.example .env   # then fill in real values
npm run dev             # http://localhost:3000
```
