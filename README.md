# Campus Canteen & Stationery Ordering Portal

A responsive full-featured React web application designed for campus cafeterias and stationery stores. The platform allows students and faculty to browse food items and stationery supplies, customize orders with real-time cart state management, manage user profiles, and generate printable PDF receipts/invoices on checkout.

---

## Key Features

- **Dual Storefront Mode**: Toggle seamlessly between cafeteria snacks/beverages and campus stationery supplies.
- **Dynamic Category Filtering**: Filter products dynamically across subcategories (Beverages, Snacks, Books, Supplies, or All).
- **Global Cart State Management**: Centralized React Context (`CanteenContext`) providing instant add-to-cart, quantity adjustments, item removal, and live subtotal calculations.
- **Client-Side Routing**: Multi-page navigation built on `react-router-dom` v6 supporting Home, Menu, Cart, Authentication (Login & Signup), and Student Profile views.
- **Automated PDF Invoice Generation**: Direct in-browser export of structured order receipts using `jspdf` and `jspdf-autotable`.
- **Responsive Layout**: Clean desktop and mobile responsive design styled with CSS modular sheets.

---

## Tech Stack

- **Frontend**: React 18
- **Routing**: React Router DOM v6
- **State Management**: React Context API
- **Document Generation**: jsPDF, jsPDF-AutoTable
- **Styling**: Vanilla CSS3 with flexbox/grid layout systems
- **Tooling**: Create React App, Web Vitals

---

## Project Structure

```text
canteen/
├── public/                 # Static assets, HTML shell, and manifest
│   ├── index.html
│   └── manifest.json
├── src/
│   ├── components/         # Modular React components
│   │   ├── CanteenCart/    # Cart line-item controls and checkout
│   │   ├── CanteenMenu.js/ # Product catalog and menu toggles
│   │   ├── CartTile.js     # Single cart item view
│   │   ├── EmptyCart/      # Fallback UI for empty shopping bag
│   │   ├── Footer/         # Application footer
│   │   ├── HomeImage/      # Hero banner
│   │   ├── LoginPage/      # Student login authentication view
│   │   ├── Navbar/         # Header navigation bar
│   │   ├── pages/          # Primary route pages (Home, Cart, Profile)
│   │   ├── ProductCard/    # Individual item presentation card
│   │   ├── SignupPage/     # Student registration view
│   │   ├── StuProfile/     # Student details and order history
│   │   └── SubCategoryButtons/ # Category pill filter buttons
│   ├── context/
│   │   └── CanteenContext.js # Global cart and order state provider
│   ├── App.css
│   ├── App.js              # Application root and route declarations
│   ├── index.css
│   └── index.js            # React DOM hydration entry point
├── package.json            # Dependencies and build scripts
└── README.md               # Project documentation
```

---

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/azimrehan/canteen.git
   cd canteen
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Launch the development server:
   ```bash
   npm start
   ```

   The app will open automatically at `http://localhost:3000`.

### Building for Production

To create an optimized production bundle:
```bash
npm run build
```

The compiled assets will be output to the `build/` folder ready for deployment to Vercel, Netlify, or any static hosting service.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
