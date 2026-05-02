# Satguru Transport — Company Website

Official website for **Satguru Transport**, a logistics and transport company based in Delhi with 18+ years of experience. The site is a fully static, single-file HTML application with no build step or backend required.

---

## Live Site

Hosted on GitHub Pages.

---

## Features

- **Quote Request Form** — Customers can submit shipment details (name, phone, route, vehicle type, cargo) and the enquiry is delivered instantly to `jolly@satgurulogistics.com` via EmailJS
- **Truck Gallery** — Showcases the full fleet: TATA ACE, TATA 407, 14 FT, 17 FT, 20 FT, 22 FT, and Refrigerated 22 FT trucks
- **Services Section** — Full Truckload (FTL), Part Load (LTL), Refrigerated Transport, Intercity & Interstate logistics
- **Industries Served** — Pharmaceuticals, FMCG, Automotive, E-commerce, and more
- **Responsive Design** — Works on mobile, tablet, and desktop
- **No backend** — Entirely client-side; no server, no database

---

## Tech Stack

| Technology             | Purpose                                     |
| ---------------------- | ------------------------------------------- |
| React 18 (CDN)         | UI components and state management          |
| Babel Standalone (CDN) | JSX transpilation in the browser            |
| EmailJS Browser SDK v4 | Sending quote form emails without a backend |
| Google Fonts (Barlow)  | Typography                                  |
| Vanilla CSS            | All styling via CSS variables               |

---

## Project Structure

```
satguru-logistics/
├── index.html        # Entire website — HTML, CSS, and React all in one file
├── embed_images.py   # Optional script to download and base64-embed all truck images
└── README.md
```

---

## EmailJS Setup

The quote form uses [EmailJS](https://www.emailjs.com) to send enquiries. The free tier allows **200 emails/month**.

The credentials are stored as constants inside the `<script type="text/babel">` block in `index.html`:

```js
const EMAILJS_PUBLIC_KEY = "your_public_key";
const EMAILJS_SERVICE_ID = "your_service_id";
const EMAILJS_TEMPLATE_ID = "your_template_id";
```

### To update credentials:

1. Log in at [emailjs.com](https://www.emailjs.com)
2. **Public Key** → Account → General
3. **Service ID** → Email Services → your connected service
4. **Template ID** → Email Templates → your template

### EmailJS template variables:

When editing the template on EmailJS, these variables are available:

| Variable        | Value                   |
| --------------- | ----------------------- |
| `{{from_name}}` | Customer's full name    |
| `{{phone}}`     | Customer's phone number |
| `{{email}}`     | Customer's email        |
| `{{company}}`   | Company name            |
| `{{from_city}}` | Origin city             |
| `{{to_city}}`   | Destination city        |
| `{{vehicle}}`   | Vehicle type selected   |
| `{{cargo}}`     | Cargo type              |
| `{{message}}`   | Additional details      |

---

## Making Updates

Since the whole site is one file, all edits happen in `satguru-logistics.html`.

| What to change                 | Where to look in the file                                  |
| ------------------------------ | ---------------------------------------------------------- |
| Phone number / email           | Search for `+919971130303` or `jolly@satgurulogistics.com` |
| Truck images                   | Search for `TruckGallery` — update the `src:` URLs         |
| Services offered               | Search for `const SERVICES`                                |
| Industries section             | Search for `const INDUSTRIES`                              |
| Testimonials                   | Search for `const TESTIMONIALS`                            |
| Company stats (18+ years etc.) | Search for `const STATS`                                   |

---

## Deployment (GitHub Pages)

1. Push `satguru-logistics.html` to the `main` branch of your GitHub repository

## Contact

**Satguru Transport**
📍 Delhi, India
📞 +91 99711 30303
📧 jolly@satgurulogistics.com
