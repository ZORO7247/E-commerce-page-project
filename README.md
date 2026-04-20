# E-commerce-page-project
A fully-featured React e-commerce frontend that lets users browse products, filter by category and price, manage a wishlist, and complete a checkout flow.
State Management
CartContext
Managed with useReducer. Actions:

ADD_TO_CART — adds item or increments quantity if already present
REMOVE_FROM_CART — removes item by productId
UPDATE_QUANTITY — sets quantity for a specific item
CLEAR_CART — empties the cart (used after checkout)

WishlistContext
Managed with useState. Exposes:

addToWishlist(product) — adds if not already saved
removeFromWishlist(productId) — removes by id
isInWishlist(productId) — returns boolean

Folder Structure
src/
├── App.js
├── index.js
├── index.css
│
├── services/
│   └── api.js              # Axios calls to Fake Store API
│
├── context/
│   ├── CartContext.js       # Global cart state (useReducer)
│   └── WishlistContext.js  # Global wishlist state (useState)
│
├── hooks/
│   ├── useProducts.js      # Fetches all products + categories
│   └── useDebounce.js      # Debounce hook for search
│
├── utils/
│   └── helpers.js          # formatPrice, filterProducts, TAX_RATE
│
├── components/
│   ├── Navbar/
│   ├── Footer/
│   ├── ProductCard/
│   ├── ProductGrid/
│   ├── CartItem/
│   ├── Filters/
│   └── SearchBar/
│
└── pages/
    ├── Home/               # Hero + tabbed featured products
    ├── Products/           # Full listing with filters
    ├── ProductDetails/     # Single product page
    ├── Cart/               # Cart items + summary
    ├── Wishlist/           # Saved products
    └── Checkout/           # Form + order summary
