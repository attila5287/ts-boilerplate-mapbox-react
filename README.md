# TypeScript Boilerplate with Mapbox React

This project demonstrates a React + TypeScript + Vite setup with Mapbox GL JS integration.

## Project Development Journey

Started by cloning the [Vercel Vite React TypeScript starter kit](https://github.com/vercel/examples/tree/main/framework-boilerplates/vite-react) as our foundation. 

For the initial implementation, used the Map component from the [Mapbox React-JS tutorial](https://docs.mapbox.com/mapbox-gl-js/example/simple-map/) as a "Hello World" example. However, encountered several TypeScript errors that needed to be resolved:

- Fixed ref type annotations for proper TypeScript support
- Added null checks for React refs
- Removed unused imports
- Properly typed the Mapbox GL JS integration

After resolving the local TypeScript issues, encountered additional errors during the Vercel deployment process. These were also successfully fixed, and the project is now live at:

**🌐 Live Demo: [https://ts-boilerplate-mapbox-react.vercel.app/](https://ts-boilerplate-mapbox-react.vercel.app/)**

## Quick Start

### Clone and Setup

```bash
# Clone this repository
git clone https://github.com/your-username/ts-boilerplate-mapbox-react.git

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
