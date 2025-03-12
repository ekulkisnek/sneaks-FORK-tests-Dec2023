
# The Sneaks App

## Overview
The Sneaks App is a comprehensive web application that allows users to search for sneakers across multiple reseller platforms and compare prices in real-time. This application serves as a one-stop solution for sneaker enthusiasts and buyers looking to find the best deals on their favorite footwear.

## Features
- **Unified Search Interface**: Search for sneakers across multiple platforms from a single interface
- **Price Comparison**: Compare prices from StockX, GOAT, Stadium Goods, and Flight Club
- **Trending Sneakers**: View currently trending sneakers in the marketplace
- **Brand Filtering**: Quick access to filter by popular sneaker brands
- **Detailed Product View**: Access comprehensive information about each sneaker
- **Responsive Design**: Fully responsive interface that works on desktop and mobile devices

## Technology Stack
This application is built using modern web technologies:

- **Frontend Framework**: React.js
- **Routing**: React Router (v6)
- **UI Components**: React Bootstrap
- **Styling**: CSS with Bootstrap 5
- **Build Tool**: Vite (for fast development and optimized production builds)
- **Deployment**: Static site deployment via Replit

## Architecture
The application follows a component-based architecture with the following key components:

- **App.jsx**: Main component that handles routing and layout
- **NavBar**: Navigation bar component
- **SearchBar**: Component for user search input
- **BrandIcons**: Component displaying filterable brand icons
- **Trending**: Component that displays trending sneakers
- **Products**: Component that displays search results
- **MiniCard**: Component for displaying individual sneaker information
- **PriceTable**: Component for displaying detailed price comparison

## API Integration
The application integrates with the Sneaks API (hosted on Azure) to fetch sneaker data:
- Base URL: `https://sneaks-api.azurewebsites.net/`
- Endpoints:
  - `/home`: Fetches trending sneakers
  - `/search/{query}`: Searches for sneakers matching the query
  - `/id/{styleID}/prices`: Fetches detailed pricing information for a specific sneaker

## Development Setup
To set up the development environment:

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Start the development server:
   ```
   npm run dev
   ```
4. The application will be available at http://localhost:5173

## Build Process
To build the application for production:

1. Run the build command:
   ```
   npm run build
   ```
2. The build artifacts will be stored in the `dist/` directory

## Deployment
The application is configured for deployment on Replit:
- The deployment target is set to "static"
- Build command: `npm run build`
- Public directory: `dist`

## Project Structure
```
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── NavBar.jsx
│   │   ├── SearchBar.jsx
│   │   ├── BrandIcons.jsx
│   │   ├── Trending.jsx
│   │   ├── Products.jsx
│   │   ├── MiniCard.jsx
│   │   └── PriceTable.jsx
│   ├── images/
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── index.jsx
├── index.html
├── package.json
├── vite.config.js
└── tsconfig.json
```

## How It Works
1. The application fetches trending sneakers when a user lands on the homepage
2. Users can search for specific sneakers using the search bar
3. When a search is performed, the application queries the Sneaks API
4. Results are displayed as cards showing the sneaker image, name, and lowest price
5. Users can click on a specific sneaker to view detailed pricing information
6. The detailed view shows prices from different resellers, allowing users to compare and find the best deal

## Performance Optimizations
- Vite is used as the build tool for faster development and optimized production builds
- React's state management is used efficiently to minimize re-renders
- API calls are optimized to fetch data only when needed
- Images are optimized for faster loading

## Future Enhancements
- User authentication for saving favorite sneakers
- Price alerts when sneakers drop below a specified price
- Historical price tracking
- More detailed filtering options
- Mobile app version

## Contributing
Contributions to The Sneaks App are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the ISC License - see the LICENSE file for details.
