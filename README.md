# 🌍 Eco-Route AI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?logo=node.js&logoColor=white)](https://nodejs.org/)

> **Empowering sustainable travel decisions with AI-driven route optimization**

Eco-Route AI is a cutting-edge web application that helps users make environmentally conscious travel choices by comparing routes based on carbon emissions, travel time, and ecological impact. Built with modern web technologies, it provides real-time route comparisons to promote greener transportation options.

## ✨ Features

### 🚀 Core Functionality
- **Real-time Route Comparison**: Compare fastest vs. greenest routes instantly
- **Multi-Modal Support**: Supports electric, hybrid, gas vehicles, bikes, and public transport
- **Carbon Footprint Calculation**: Accurate CO₂ emission estimates for different routes
- **Environmental Impact Metrics**: See equivalent tree savings and percentage improvements
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices

### 🎨 User Experience
- **Intuitive Interface**: Clean, modern UI with gradient designs
- **Form Validation**: Real-time input validation with helpful error messages
- **Loading States**: Smooth user feedback during API calls
- **Accessibility**: Semantic HTML and keyboard navigation support

### 🛠 Technical Excellence
- **Type-Safe**: Full TypeScript implementation for reliability
- **Modern Stack**: React 18, Vite, tRPC for optimal performance
- **Database Integration**: Drizzle ORM with PostgreSQL support
- **Authentication**: OAuth integration for secure user management
- **Cloud Storage**: AWS S3 integration for file uploads
- **Testing**: Comprehensive test suite with Vitest

## 📸 Screenshots

### Home Page
A beautiful landing page with route comparison form and results display.

### Route Comparison Results
Side-by-side comparison of fastest and greenest routes with environmental metrics.

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- pnpm (recommended) or npm/yarn
- PostgreSQL database (for full functionality)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/KrishnTundia/hgfdsa.git
   cd hgfdsa
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   ```

3. **Configure environment**
   ```bash
   # Copy and edit environment variables
   cp .env.example .env.local
   ```

   Update the following in `.env.local`:
   ```env
   VITE_OAUTH_PORTAL_URL=https://your-oauth-provider.com
   VITE_APP_ID=your-app-id
   DATABASE_URL=postgresql://user:password@localhost:5432/ecoroute
   AWS_ACCESS_KEY_ID=your-aws-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret
   ```

4. **Set up the database**
   ```bash
   pnpm db:push
   ```

5. **Start development server**
   ```bash
   pnpm dev
   ```

6. **Open your browser**
   ```
   http://localhost:3000
   ```

## 📖 Usage

### Basic Route Comparison

1. Enter your starting point and destination
2. Select your vehicle type
3. Click "Compare Routes"
4. View the comparison results showing:
   - Distance and duration for each route
   - CO₂ emissions
   - Environmental savings

### API Usage

The application uses tRPC for type-safe API communication. Key endpoints:

#### Compare Routes
```typescript
const result = await trpc.routes.compare.query({
  startingPoint: "Times Square, NYC",
  destination: "Central Park, NYC",
  vehicleType: "hybrid"
});

// Response
{
  success: true,
  data: {
    fastest: {
      distance: "2.8 km",
      duration: "8 min",
      emissions: "224 g CO2e",
      route: "Via highways"
    },
    greenest: {
      distance: "2.5 km",
      duration: "12 min",
      emissions: "125 g CO2e",
      route: "Via scenic roads"
    },
    savings: {
      emissionsSaved: "99 g CO2e",
      treesEquivalent: 1,
      percentBetter: "44.2%"
    }
  }
}
```

## 🏗 Project Structure

```
hgfdsa/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Page components
│   │   ├── hooks/         # Custom React hooks
│   │   └── lib/           # Utility libraries
│   ├── public/            # Static assets
│   └── index.html         # Main HTML template
├── server/                 # Backend Node.js server
│   ├── _core/             # Core business logic
│   ├── routers.ts         # tRPC route definitions
│   └── storage.ts         # File storage handlers
├── shared/                 # Shared types and constants
├── drizzle/                # Database schema and migrations
├── dist/                   # Built application (after build)
└── package.json           # Project dependencies and scripts
```

## 🧪 Testing

Run the test suite:
```bash
pnpm test
```

Run tests in watch mode:
```bash
pnpm test:watch
```

## 🚢 Deployment

### Build for Production
```bash
pnpm build
```

### Start Production Server
```bash
pnpm start
```

The application will be available at `http://localhost:3002`

### Deployment Options
- **Vercel/Netlify**: For frontend hosting
- **Railway/Render**: For full-stack deployment
- **AWS/DigitalOcean**: For custom infrastructure

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Development Guidelines
- Use TypeScript for all new code
- Follow existing code style and conventions
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with ❤️ for a greener future
- Inspired by the need for sustainable transportation
- Thanks to the open-source community for amazing tools

## 📞 Support

If you have questions or need help:
- Open an issue on GitHub
- Check the documentation in `QUICK_START.md` and `ECO_ROUTE_IMPLEMENTATION.md`
- Join our community discussions

---

**Made with 🌱 for the planet**