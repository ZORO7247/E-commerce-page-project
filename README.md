# ShopEasy — E-Commerce Product Explorer

A React-based e-commerce app built as part of PRD 4 project.

---

## Setup Instructions

### 1. Create the React app
```bash
npx create-react-app ecommerce-app
cd ecommerce-app
```

### 2. Install all required packages
```bash
npm install react-router-dom axios react-icons react-toastify react-hook-form @hookform/resolvers yup swiper framer-motion uuid
```

### 3. Replace files with the project code
Copy each file from this project into the correct location (see folder structure below).

### 4. Run the app
```bash
npm start
```

---

## Folder Structure

```
src/
│
├── App.js                          ← Main app + routes
├── index.js                        ← Entry point
├── index.css                       ← Global styles
│
├── context/
│   └── CartContext.js              ← Global cart + wishlist state (Context API)
│
├── services/
│   └── api.js                      ← Axios API calls to FakeStore API
│
├── utils/
│   └── helpers.js                  ← formatPrice, truncateText, getRatingStars
│
├── hooks/
│   ├── useProducts.js              ← Custom hook: fetch all products
│   ├── useDebounce.js              ← Custom hook: debounce search input
│   └── useWishlist.js              ← Custom hook: wishlist helpers
│
├── components/
│   ├── Navbar/
│   │   ├── Navbar.js
│   │   └── Navbar.css
│   ├── ProductCard/
│   │   ├── ProductCard.js
│   │   └── ProductCard.css
│   ├── ProductGrid/
│   │   ├── ProductGrid.js
│   │   └── ProductGrid.css
│   ├── SearchBar/
│   │   ├── SearchBar.js
│   │   └── SearchBar.css
│   ├── Filters/
│   │   ├── Filters.js
│   │   └── Filters.css
│   └── CartItem/
│       ├── CartItem.js
│       └── CartItem.css
│
└── pages/
    ├── Home/
    │   ├── Home.js
    │   └── Home.css
    ├── Products/
    │   ├── Products.js
    │   └── Products.css
    ├── ProductDetails/
    │   ├── ProductDetails.js
    │   └── ProductDetails.css
    ├── Cart/
    │   ├── Cart.js
    │   └── Cart.css
    ├── Wishlist/
    │   ├── Wishlist.js
    │   └── Wishlist.css
    └── Checkout/
        ├── Checkout.js
        └── Checkout.css
```

---

## Features Implemented

- Product listing with responsive grid (3 col → 2 → 1)
- Product Details page with rating stars
- Search with debounce (400ms delay)
- Category filters (sidebar + tabs)
- Price range filters
- Sort: price asc/desc, rating
- Shopping cart with quantity controls
- Wishlist toggle (heart icon)
- Checkout form with validation (react-hook-form + yup)
- Toast notifications for cart/wishlist actions
- Framer Motion animations on cards and page load
- Mobile responsive navbar with hamburger menu
- Empty states for cart and wishlist

---

## React Concepts Used

| Concept | Where Used |
|---|---|
| useState | Filters, search, cart, wishlist |
| useEffect | Fetch products, categories |
| Context API | CartContext (cart + wishlist) |
| Custom Hooks | useProducts, useDebounce, useWishlist |
| React Router DOM | All 6 page routes |
| react-hook-form + yup | Checkout form validation |
| framer-motion | Card hover + page animations |
| react-toastify | Cart/wishlist notifications |
| react-icons | All icons |
