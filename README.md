
# ⚽ FootballVerse – Team Info Manager

FootballVerse is a full-stack MVC web application that allows authenticated users to manage football teams and their players. Users can write and maintain descriptive information about teams, create and manage player rosters, and interact with a responsive and modern UI. The application supports full CRUD functionality, JWT authentication, RESTful API endpoints, and more.

## 🌐 Live Demo

🔗 [Deployed App]

---

## 📋 Features

- 🧾 **Full MVC Architecture**
- 🔐 **JWT Authentication**
- 🏆 **Paragraphs CRUD**
- ✍ **Team Description Paragraphs**
- 📦 **RESTful API**
- 🎨 **Responsive UI with Custom Design**
- 🧪 **Unit Testing (Jest)**
- 🚀 **Load Testing with Artillery**
- ☁ **Deployment**

---


## 🧱 Tech Stack

**Frontend**
- HTML
- CSS 

**Backend**
- Node.js
- Express.js
- MongoDB + Mongoose
- JWT for Authentication

**Testing**
- Jest
- Artillery (Load Testing)

---

## 🔧 Models Overview

### 🏟 Team Model

js
const mongoose = require('mongoose')
const teamSchema = new mongoose.Schema({
  name: String,
  league: String,
  description: String,
  logoUrl: String,
  createdBy: { type: mongoose.Schema.Types.ObjectId, ref: 'User' },
  players: [{ type: mongoose.Schema.Types.ObjectId, ref: 'Player' }]
})
module.exports = mongoose.model('Team', teamSchema)
`

### 👟 Player Model

js
const mongoose = require('mongoose')
const playerSchema = new mongoose.Schema({
  name: String,
  position: String,
  age: Number,
  nationality: String,
  team: { type: mongoose.Schema.Types.ObjectId, ref: 'Team' }
})
module.exports = mongoose.model('Player', playerSchema)


---

## 🔐 Authentication

* Register/Login using JWT
* Passwords hashed with bcrypt
* Protected CRUD routes for users

