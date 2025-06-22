# TypeScript Boilerplate with Mapbox React

https://github.com/attila5287/ts-boilerplate-mapbox-react

This project demonstrates a React + TypeScript + Vite setup with Mapbox GL JS integration.

## Project Development Journey

Started by cloning the [Vercel Vite React TypeScript starter kit](https://github.com/vercel/examples/tree/main/framework-boilerplates/vite-react) as our foundation. 

For the initial implementation, used the Map component from the [Mapbox React-JS tutorial](https://docs.mapbox.com/help/tutorials/dynamic-markers-react/?step=2) as a "Hello World" example. However, encountered several TypeScript errors that needed to be resolved:

- Fixed ref type annotations for proper TypeScript support
- Added null checks for React refs
- Removed unused imports
- Properly typed the Mapbox GL JS integration
- **Fixed CSS styling issues** that prevented the map from displaying correctly

After resolving the local TypeScript issues, encountered additional errors during the Vercel deployment process. These were also successfully fixed, and the project is now live at:

**🌐 Live Demo: [https://ts-boilerplate-mapbox-react.vercel.app/](https://ts-boilerplate-mapbox-react.vercel.app/)**

## Quick Start

### Clone and Setup

```bash
# Clone this repository link 

git clone https://github.com/attila5287/ts-boilerplate-mapbox-react.git

# Navigate to the project directory
cd ts-boilerplate-mapbox-react

# Install dependencies
npm install

# Start the development server
npm run dev
```

The application will be available at `http://localhost:5173`

### Deploy to Vercel

#### Option 1: Deploy from GitHub (Recommended)

1. Fork or clone this repository to your GitHub account
2. Go to [Vercel](https://vercel.com) and sign in
3. Click "New Project"
4. Import your GitHub repository
5. Vercel will automatically detect it's a Vite project
6. Click "Deploy" - your app will be live in minutes!

#### Option 2: Deploy from Local Directory

```bash
# Install Vercel CLI globally
npm i -g vercel

# Navigate to your project directory
cd ts-boilerplate-mapbox-react

# Deploy to Vercel
vercel

# Follow the prompts to link to your Vercel account
```

## Tech Stack

- **React 18** with TypeScript
- **Vite** for fast development and building
- **Mapbox GL JS** for interactive maps
- **Vercel** for deployment

## Getting Started

1. Clone this repository
2. Install dependencies: `npm install`
3. Start development server: `npm run dev`
4. Build for production: `npm run build`

## Features

- Interactive Mapbox map integration
- TypeScript support with proper type safety
- Vite-based development with HMR
- Ready for Vercel deployment

## CSS Styling

The CSS styling was absolutely critical - **without these specific styles, the Mapbox map would be completely invisible**. The map container needs explicit dimensions to render properly. Additionally, removed all default styles from `index.css` that came with the Vite React starter kit to prevent conflicts:

```css
#map-container {
  width: 100vw;
  height: 100vh;
  position: relative;
}

/* Ensure the map takes up the full viewport */
body,
html {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}

/* Make sure the root element also takes full height */
#root {
  height: 100%;
  width: 100%;
}
```

**Why this CSS is essential:**
- Without `width: 100vw` and `height: 100vh`, the map container has zero dimensions and the map won't render
- The `position: relative` is required for proper Mapbox GL JS positioning
- Removed all default Vite starter kit styles from `index.css` to ensure clean slate
- Body/html/root sizing ensures the map can expand to full viewport without scrollbars
