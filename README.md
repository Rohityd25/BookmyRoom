# 🏠 BookMyRoom

A full-stack **room booking web application** where users can discover, list, and review unique stays — from beachfront cottages to luxury villas — across the globe.

Built with **Node.js**, **Express**, **MongoDB**, and **EJS** templating.

---

## ✨ Features

- 🔐 **User Authentication** — Sign up, login, and logout with Passport.js (local strategy)
- 🏡 **Create Listings** — Hosts can add new room listings with title, description, price, image, and location
- ✏️ **Edit & Delete** — Listing owners can update or remove their properties
- ⭐ **Reviews & Ratings** — Guests can leave star ratings and text reviews on listings
- 🔍 **Browse & Search** — Explore all available rooms with a clean, card-based UI
- 🏔️ **Premium Homepage** — Beautiful landing page with hero section, featured destinations, testimonials, and CTA
- 📱 **Responsive Design** — Works seamlessly on desktop, tablet, and mobile
- ⚡ **Flash Messages** — User-friendly success and error notifications
- 🛡️ **Authorization** — Only listing owners can edit/delete their listings
- 🚀 **Server-side Validation** — Joi schema validation for listings and reviews

---

## 🖼️ Screenshots

### 🏠 Homepage
> A stunning landing page with a search bar, featured destinations, how-it-works guide, testimonials, and a call-to-action section.

### 📋 All Listings
> Browse all available rooms displayed as beautiful cards with images, titles, and pricing.

### 📝 Listing Details
> View full details of a listing including description, location, price, reviews, and ratings.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Backend** | Node.js, Express.js |
| **Frontend** | EJS, EJS-Mate (layouts), Bootstrap 5 |
| **Database** | MongoDB, Mongoose ODM |
| **Authentication** | Passport.js, Passport-Local, Passport-Local-Mongoose |
| **Validation** | Joi |
| **Session** | Express-Session, Connect-Flash |
| **Icons** | Font Awesome 6 |
| **Dev Tools** | Nodemon |

---

## 📁 Project Structure

```
BookMyRoom/
├── controllers/          # Route handler logic
│   ├── listings.js       # Listing CRUD operations
│   ├── reviews.js        # Review create & delete
│   └── users.js          # User signup, login, logout
│
├── models/               # Mongoose schemas
│   ├── listing.js        # Listing model
│   ├── review.js         # Review model
│   └── user.js           # User model
│
├── routes/               # Express route definitions
│   ├── listing.js        # /listing routes
│   ├── review.js         # /listing/:id/review routes
│   └── user.js           # /signup, /login, /logout routes
│
├── views/                # EJS templates
│   ├── layouts/
│   │   └── boilerplate.ejs   # Main layout template
│   ├── includes/
│   │   ├── navbar.ejs        # Navigation bar
│   │   ├── footer.ejs        # Footer
│   │   └── flash.ejs         # Flash messages
│   ├── listings/
│   │   ├── index.ejs         # All listings page
│   │   ├── show.ejs          # Single listing details
│   │   ├── newlist.ejs       # Create new listing form
│   │   └── edit.ejs          # Edit listing form
│   ├── users/
│   │   ├── signup.ejs        # Sign up page
│   │   └── login.ejs         # Login page
│   ├── home.ejs              # Homepage
│   └── error.ejs             # Error page
│
├── public/               # Static assets
│   ├── css/
│   │   ├── style.css         # Main stylesheet
│   │   └── rating.css        # Star rating styles
│   └── js/
│       └── script.js         # Client-side JavaScript
│
├── utils/                # Utility classes
│   ├── ExpressError.js   # Custom error class
│   └── wrapAsync.js      # Async error wrapper
│
├── init/                 # Database seeding
│   ├── data.js           # Sample listing data (30 listings)
│   └── index.js          # Seed script
│
├── app.js                # Main application entry point
├── middleware.js          # Custom middleware (auth checks)
├── schema.js             # Joi validation schemas
├── package.json          # Dependencies & scripts
└── .gitignore            # Git ignore rules
```

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/) (running locally or MongoDB Atlas)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Rohityd25/BookmyRoom.git
   cd BookmyRoom
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start MongoDB** (if running locally)
   ```bash
   mongod
   ```

4. **Seed the database** (optional — adds 30 sample listings)
   ```bash
   node init/index.js
   ```

5. **Run the application**
   ```bash
   npx nodemon app.js
   ```

6. **Open in browser**
   ```
   http://localhost:3000
   ```

---

## 🗂️ API Routes

### Listings
| Method | Route | Description |
|--------|-------|-------------|
| GET | `/listing` | View all listings |
| GET | `/listing/new` | New listing form |
| POST | `/listing` | Create a listing |
| GET | `/listing/:id` | View a listing |
| GET | `/listing/:id/edit` | Edit listing form |
| PUT | `/listing/:id` | Update a listing |
| DELETE | `/listing/:id` | Delete a listing |

### Reviews
| Method | Route | Description |
|--------|-------|-------------|
| POST | `/listing/:id/review` | Add a review |
| DELETE | `/listing/:id/review/:reviewId` | Delete a review |

### Users
| Method | Route | Description |
|--------|-------|-------------|
| GET | `/signup` | Sign up page |
| POST | `/signup` | Register user |
| GET | `/login` | Login page |
| POST | `/login` | Authenticate user |
| GET | `/logout` | Logout user |

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **ISC License**.

---

## 👨‍💻 Author

**Rohit Yadav**
- GitHub: [@Rohityd25](https://github.com/Rohityd25)

---

> ⭐ If you found this project helpful, please give it a star on GitHub!