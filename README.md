# 🐾 PawPantry

### Smart pet-food refills that arrive right on time

<p align="center">
  <strong>Track food · Predict run-out dates · Plan the next refill</strong>
</p>

<p align="center">
  <a href="#-getting-started">Getting Started</a> ·
  <a href="#-how-it-works">How It Works</a> ·
  <a href="#-features">Features</a> ·
  <a href="#-limitations">Limitations</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-early%20MVP%20demo-286b4e?style=for-the-badge" alt="Early MVP demo" />
  <img src="https://img.shields.io/badge/platform-browser-f3a65a?style=for-the-badge" alt="Browser prototype" />
  <img src="https://img.shields.io/badge/backend-none-6d7b72?style=for-the-badge" alt="No backend" />
</p>

> PawPantry is a browser-based prototype that helps dog owners estimate when
> their current food bag will run out and plan a sample refill before it does.

---

## ✨ Why PawPantry?

Running out of pet food is easy to do when daily consumption is not tracked.
PawPantry turns a few simple details into a practical refill timeline:

```text
Dog + food details → Run-out forecast → Reminder date → Demo refill order
```

The experience is designed as an early MVP for exploring a predictable,
convenient pet-food refill journey.

## 🖥️ What the prototype looks like

The single-page experience includes:

- A friendly PawPantry landing section.
- A dog food profile form.
- Forecast summary cards.
- A nearby-shop refill panel.
- Local refill activity history.
- Responsive layouts for desktop and mobile screens.

## 🚀 Features

| Feature | What it does |
| --- | --- |
| 🐶 **Dog profile** | Stores the dog's name, weight, food type, bag size, and opening date. |
| 📅 **Food forecast** | Estimates bag duration and the expected run-out date. |
| 🔔 **Refill reminder** | Suggests a date to arrange the next refill. |
| 🛍️ **Demo ordering** | Lets users select a delivery date, shop, and delivery area. |
| 📦 **Order activity** | Shows confirmed demo orders with status and sample price. |
| 💾 **Browser storage** | Keeps the profile and demo orders in local `localStorage`. |
| 📱 **Responsive UI** | Works across common desktop and mobile viewport sizes. |

## 🧭 How it works

1. Add the dog's name and weight.
2. Select the food bag size and enter the food brand or type.
3. Enter the date the bag was opened.
4. Select **Calculate my refill forecast**.
5. Review the estimated daily usage, run-out date, and reminder date.
6. Choose a preferred delivery date and partner shop.
7. Add a delivery area or address.
8. Select **Confirm demo refill** to save a sample order.

## 🧮 Forecast logic

The prototype uses an illustrative assumption that a dog consumes about
`2.5%` of its body weight in food per day:

```text
Estimated daily food use = Dog weight × 2.5%
Estimated bag duration   = Bag size ÷ Estimated daily food use
```

The duration is rounded up to a whole number of days. The suggested reminder
uses the larger of:

- `20%` of the estimated bag duration, rounded up.
- A minimum buffer of `4 days`.

> ⚠️ This is a product-demo calculation, not veterinary feeding advice.
> Always follow the food packaging guidance or consult a veterinarian.

## 🛠️ Getting started

### Requirements

- A modern browser: Chrome, Edge, Firefox, or Safari.
- No Node.js, package installation, database, or internet connection required.

### Run locally

1. Clone or download this repository.
2. Open `index.html` in a modern browser.
3. Fill in the dog profile.
4. Try the forecast and demo refill flow.

You can also use any simple local web server, but opening the HTML file
directly is enough for this prototype.

## 📁 Project structure

```text
PawPantry_Prototype/
├── index.html    # Complete browser prototype
└── README.md     # Project documentation
```

The prototype is intentionally self-contained: the markup, styling, and
JavaScript behavior are all contained in `index.html`.

## 💾 Data storage

PawPantry uses browser `localStorage`:

| Storage key | Contents |
| --- | --- |
| `pawpantryProfile` | The latest saved dog food profile and forecast. |
| `pawpantryOrders` | Demo refill orders created in the current browser. |

Data is not synchronized across browsers or devices. Clearing the browser's
site data removes the saved profile and demo orders.

## ⚠️ Limitations

This is an early MVP demonstration, not a production ordering platform:

- Partner shops, prices, and order statuses are sample data.
- No real shop, payment gateway, or delivery service is contacted.
- No account system, backend, database, or authentication is included.
- No inventory or product availability is checked.
- No email, SMS, WhatsApp, or push notifications are sent.
- Orders are saved only in the current browser.
- The estimate does not account for food-specific guidance, treats, age,
  breed, activity, health conditions, or multiple pets.

## 🗺️ Possible next steps

- [ ] Add accounts and secure cloud storage.
- [ ] Support multiple pets and multiple food profiles.
- [ ] Add food-specific feeding guidance.
- [ ] Connect real product catalogs, pricing, and shop inventory.
- [ ] Add payments, delivery tracking, and order management.
- [ ] Add email, SMS, WhatsApp, or push reminders.
- [ ] Support repeat orders and subscription refills.
- [ ] Complete accessibility and mobile usability testing.

## 📌 Project status

**PawPantry is an early MVP prototype for product demonstration and user-flow
validation.** It is not a production ordering system and should not replace
professional veterinary guidance.

---

<p align="center">
  Made with 🐾 for happier, better-planned pet care.
</p>
