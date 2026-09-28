# TOY HAVEN — EASY VS CODE / VIVA VERSION

## START HERE

If you are opening this project for the first time:

1. Open the `toy-haven` folder in Visual Studio Code.
2. Open `index.html`.
3. Right-click → **Open with Live Server**.
4. The website should open in your browser.

---

# MOST IMPORTANT FILES

```text
toy-haven/
│
├── index.html                 ← HOME PAGE
├── products.html              ← PRODUCT LISTING
├── cart.html                  ← SHOPPING CART
├── checkout.html              ← CHECKOUT
├── wishlist.html              ← MY COLLECTION
├── support.html               ← FEEDBACK + FAQ
│
├── css/
│   └── style.css              ← ALL WEBSITE STYLING
│
├── js/
│   ├── products-data.js       ← ⭐ EDIT PRODUCTS HERE
│   └── app.js                 ← WEBSITE FUNCTIONALITY
│
├── assets/                    ← IMAGES / ICONS
│
├── manifest.json              ← PWA SETTINGS
└── sw.js                      ← SERVICE WORKER
```

---

# ⭐ IF YOU NEED TO EDIT A PRODUCT

DO NOT search through the whole project.

Open:

```text
js/products-data.js
```

You will see:

```javascript
{
  id: 1,
  name: "Spider-Man Figurine",
  category: "Figurines",
  price: 29.99,
  description: "A display-ready superhero figurine for collectors and fans.",
  image: "assets/spiderman.svg"
}
```

## Change the name

```javascript
name: "New Product Name"
```

## Change the price

```javascript
price: 39.99
```

## Change the category

```javascript
category: "Toys"
```

## Change the description

```javascript
description: "My new product description."
```

## Change the picture

Put your image inside:

```text
assets/
```

Then change:

```javascript
image: "assets/my-new-image.jpg"
```

---

# ⭐ IF YOU NEED TO ADD A PRODUCT

Copy an existing product object:

```javascript
{
  id: 9,
  name: "My New Toy",
  category: "Toys",
  price: 25.99,
  description: "A new toy for the Toy Haven collection.",
  image: "assets/my-new-toy.jpg"
}
```

Put it inside the `PRODUCTS` array.

IMPORTANT:

Every product needs a different `id`.

Example:

```text
1 Spider-Man
2 Batman
3 LEGO City
...
8 Construction Truck
9 My New Toy
```

Once you save the file, the product automatically appears wherever the JavaScript uses `PRODUCTS`.

---

# ⭐ IF YOU NEED TO CHANGE THE WEBSITE COLOURS

Open:

```text
css/style.css
```

Go to the very top.

You will find:

```css
:root {
  --primary: #FF6B6B;
  --secondary: #FFD93D;
  --accent: #6BCB77;
  --background: #FFF8E7;
  --text: #333333;
}
```

These are your assignment colours.

---

# ⭐ IF YOU NEED TO CHANGE THE HOME PAGE

Open:

```text
index.html
```

The file is divided into clearly labelled sections:

```text
HEADER
HERO
CATEGORY SHORTCUTS
PRODUCT OF THE DAY
FULL PRODUCT COLLECTION
PROMOTIONAL STRIP
FOOTER
```

The Home page gets its products from:

```text
js/products-data.js
```

and displays them using:

```text
js/app.js
```

---

# ⭐ IF YOU NEED TO CHANGE THE PRODUCT PAGE

Open:

```text
products.html
```

Main functionality is inside:

```text
js/app.js
```

Look for:

```javascript
renderProducts()
```

This handles:

- Search
- Category filtering
- Displaying product cards

Look for:

```javascript
openProductModal()
```

This handles:

- Opening the product modal
- Showing product information
- Add to cart
- Wishlist status

---

# ⭐ IF YOU NEED TO CHANGE THE CART

Open:

```text
cart.html
```

Then open:

```text
js/app.js
```

Look for:

```javascript
addToCart()
```

Adds products.

```javascript
renderCart()
```

Displays the cart.

```javascript
cartTotal()
```

Calculates the total.

The cart is stored using:

```text
localStorage
```

---

# ⭐ IF YOU NEED TO CHANGE CHECKOUT

Open:

```text
checkout.html
```

Then:

```text
js/app.js
```

Look for:

```javascript
renderCheckout()
```

and:

```javascript
validateForm()
```

Checkout stores completed orders in localStorage.

---

# ⭐ IF YOU NEED TO CHANGE WISHLIST

Open:

```text
wishlist.html
```

Then search in `app.js` for:

```javascript
saveWishlist()
```

and:

```javascript
renderWishlist()
```

Statuses:

```text
Interested
Owned
Not Interested
```

are stored using localStorage.

---

# ⭐ IF YOU NEED TO CHANGE SUPPORT / FAQ

Open:

```text
support.html
```

Then search `app.js` for:

```javascript
initSupport()
```

This handles:

- Feedback form
- Feedback validation
- Saving feedback
- FAQ accordion

---

# VIVA: HOW THE WEBSITE WORKS

A simple explanation:

```text
HTML
 ↓
Creates the page structure

CSS
 ↓
Controls colours, layout, responsive design and animations

JavaScript
 ↓
Adds interaction and dynamic content

localStorage
 ↓
Remembers cart, wishlist, newsletter,
feedback and orders in the browser
```

---

# VIVA: PRODUCT DATA

Say:

> "I separated the product data into a dedicated JavaScript file called products-data.js. This makes the project easier to maintain because I can add or edit products without changing the main application logic."

Then show:

```text
js/products-data.js
```

---

# VIVA: REUSABLE FUNCTION

Say:

> "I created reusable functions so I don't have to repeat the same code on different pages."

Examples:

```javascript
productCard()
addToCart()
cartTotal()
validateForm()
showToast()
```

---

# VIVA: RESPONSIVE DESIGN

The CSS has three main layouts:

```text
Desktop
↓
more columns + full navigation

Tablet
↓
hamburger + 2-column products

Mobile
↓
compact layout + 2-column cards + stacked forms
```

The responsive breakpoints are near the bottom of:

```text
css/style.css
```

---

# VIVA: LOCALSTORAGE

The website uses localStorage because there is no backend/database in this HTML/CSS/JavaScript-only assignment.

It stores:

```text
toyHavenCart
toyHavenWishlist
toyHavenFeedback
toyHavenNewsletter
toyHavenOrders
```

---

# VIVA: PWA

These files provide the PWA foundation:

```text
manifest.json
sw.js
```

The service worker caches the website files so the browser can reuse cached resources.

---

# ASSIGNMENT CHECKLIST

Required pages:

- [x] Home
- [x] Products
- [x] Shopping Cart
- [x] Checkout
- [x] Wishlist / Collection
- [x] Feedback & Support

Required functionality:

- [x] Auto-rotating hero
- [x] Product of the Day
- [x] Product search
- [x] Category filtering
- [x] Product modal
- [x] Add to Cart
- [x] Quantity controls
- [x] Cart total
- [x] localStorage
- [x] Checkout validation
- [x] Order history
- [x] Wishlist statuses
- [x] Feedback form
- [x] FAQ accordion
- [x] Newsletter
- [x] Responsive design
- [x] Favicon
- [x] PWA files

Before submission, still test:

- [ ] W3C HTML
- [ ] W3C CSS
- [ ] WAVE
- [ ] Lighthouse Desktop
- [ ] Lighthouse Mobile
- [ ] Mobile / tablet / laptop / desktop
- [ ] GitHub Pages
