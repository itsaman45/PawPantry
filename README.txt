# PawPantry

## Smart Pet Food Refills

PawPantry is a lightweight working prototype for helping dog owners avoid
running out of pet food. It tracks a dog's food profile, estimates when the
current bag will run out, suggests a reminder date, and provides a demo flow
for ordering a refill from a nearby partner shop.

This prototype is designed as an early MVP demonstration. It runs entirely in
the browser and does not connect to real shops, payment services, delivery
partners, or notification platforms.

## Product idea

Pet owners often notice that their dog's food is running low only when the bag
is nearly empty. PawPantry aims to make refills more predictable by combining:

- A simple dog and food profile.
- An estimated food consumption rate.
- A projected bag run-out date.
- An advance refill reminder.
- A sample refill order flow with local shop options.

## Prototype flow

1. Enter the dog's name and weight.
2. Select the current bag size and enter the food brand or type.
3. Enter the date the bag was opened.
4. Select **Calculate my refill forecast**.
5. Review the estimated daily food use, run-out date, and reminder date.
6. Choose a preferred delivery date and partner shop.
7. Enter a delivery area or address.
8. Select **Confirm demo refill** to add a sample order to the activity list.

## Features

### Dog food profile

The profile form collects:

- Dog's name.
- Dog's weight in kilograms.
- Food brand or type.
- Bag size from 1.5 kg to 15 kg.
- Bag opening date.

### Refill forecast

The prototype displays:

- Predicted bag duration.
- Estimated run-out date.
- Suggested refill reminder date.
- Estimated daily food usage.

The result is clearly presented as an estimate and includes a reminder that
actual feeding needs vary by food, age, activity level, and health.

### Demo refill ordering

The refill panel includes:

- The selected food and bag size.
- An illustrative sample price.
- Preferred delivery date.
- Sample partner shop options.
- Delivery area or address.
- A confirmation action that creates a local demo order.

### Refill activity

Confirmed demo orders appear in the refill activity section with:

- Dog and food details.
- Selected partner shop.
- Delivery date.
- Delivery area.
- Sample price.
- Demo order status.

## Forecast calculation

The forecast uses the following illustrative prototype assumption:

```text
Estimated daily food use = Dog weight × 2.5%
Estimated bag duration   = Bag size ÷ Estimated daily food use
```

The calculated duration is rounded up to a whole number of days. The suggested
reminder is set before the expected run-out date using a buffer of:

- 20% of the estimated bag duration, rounded up; or
- At least 4 days.

This calculation is included to demonstrate the product flow. It is not a
veterinary feeding recommendation.

## Running the prototype

### Requirements

- A modern web browser such as Chrome, Edge, Firefox, or Safari.
- No installation, build tools, server, or internet connection.

### Steps

1. Extract the project folder if it was provided as a ZIP file.
2. Open `index.html` in a modern browser.
3. Enter a dog profile and try the forecast and demo refill flow.

The prototype can also be served from any simple local web server if preferred,
but this is not required.

## Project files

```text
PawPantry_Prototype/
├── index.html    # Complete prototype: markup, styles, and browser logic
└── README.txt    # Project documentation
```

## Data storage

The prototype uses the browser's `localStorage` to save:

- The latest dog food profile under `pawpantryProfile`.
- Demo refill orders under `pawpantryOrders`.

This means data remains available when the page is reopened in the same
browser, but it is not synchronized across devices or browsers. Clearing site
data will remove the saved profile and demo orders.

## Important limitations

- Partner shops and prices are illustrative sample data.
- Confirming a refill does not contact a real shop or schedule delivery.
- No payment is taken.
- No account creation or authentication is available.
- No backend or database is connected.
- No inventory or product availability is checked.
- No SMS, email, WhatsApp, or push notifications are sent.
- Orders are stored only in the current browser.
- The forecast does not account for food-specific feeding guides, treats,
  activity level, age, breed, medical needs, or multiple pets.
- Feeding decisions should be based on the product packaging and guidance from
  a veterinarian.

## Suggested next steps

If the prototype were developed into a production product, the next steps
could include:

1. Add user accounts and secure cloud storage.
2. Support multiple pets and multiple food profiles.
3. Use food-specific feeding guidance instead of a single percentage
   assumption.
4. Add real product catalogs, shop inventory, and pricing.
5. Integrate payments and delivery tracking.
6. Add configurable email, SMS, WhatsApp, or push reminders.
7. Add order cancellation, repeat orders, and subscription refills.
8. Add accessibility testing, validation, and mobile usability testing.

## Prototype status

PawPantry is a basic working prototype created for product demonstration and
early user-flow validation. It is not a production ordering system or a
substitute for veterinary advice.
