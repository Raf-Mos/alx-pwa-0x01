# Cine Seek - Progressive Web App (PWA)

A modern movie browsing Progressive Web App built with Next.js, featuring offline capabilities, installability, and native app-like experience.

## 🎬 About

Cine Seek is a movie discovery application transformed into a PWA that allows users to:
- Browse movie collections with an intuitive interface
- Access previously viewed content offline
- Install the app on mobile devices and desktops
- Enjoy fast loading times with intelligent caching
- Experience smooth navigation with service worker functionality

## 🚀 Features

### Progressive Web App Capabilities
- **Offline Access**: Browse cached movie data without internet connection
- **Installable**: Add to home screen on mobile devices and desktops
- **Fast Loading**: Optimized caching strategies for improved performance
- **Responsive Design**: Works seamlessly across all device sizes
- **Service Workers**: Background sync and push notifications ready

### Movie App Features
- Movie search and discovery
- Detailed movie information
- Responsive grid layout
- Optimized image loading
- Clean, modern UI design

## 🛠 Technologies Used

- **Framework**: Next.js 15.4.6
- **PWA**: @ducanh2912/next-pwa
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Icons**: FontAwesome
- **Deployment**: Vercel (production-ready)

## 🏗 Project Structure

```
alx-movie-app/
├── components/           # React components
│   ├── commons/         # Reusable UI components
│   └── layout/          # Layout components
├── interfaces/          # TypeScript interfaces
├── pages/              # Next.js pages
│   ├── api/            # API routes
│   └── movies/         # Movie-related pages
├── public/             # Static assets
│   ├── icons/          # PWA icons
│   └── manifest.json   # Web App Manifest
├── src/                # Source files
└── next.config.ts      # Next.js + PWA configuration
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ installed
- npm, yarn, pnpm, or bun package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/alx-pwa-0x01.git
cd alx-movie-app
```

2. Install dependencies:
```bash
npm install
# or
yarn install
# or
pnpm install
```

3. Generate PWA icons:
   - Use a PWA Manifest Generator tool
   - Upload your app logo
   - Generate icons in sizes: 192x192, 152x152, 310x310
   - Place them in `/public/icons/` directory

4. Run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser to see the app.

## 🔧 PWA Testing

### Local Testing
1. Start the development server
2. Open Chrome DevTools (F12)
3. Navigate to **Application** tab
4. Check:
   - **Service Workers**: Verify registration
   - **Manifest**: Confirm proper loading
   - **Storage**: Review caching behavior

### Mobile Testing
1. Deploy to production (see deployment section)
2. Visit the URL on a mobile device
3. Look for "Add to Home Screen" prompt
4. Test offline functionality

## 📱 PWA Features Testing

- **Install Prompt**: Available on supporting browsers
- **Offline Mode**: Works without internet connection
- **Caching**: Assets cached for faster loading
- **Responsive**: Optimized for all screen sizes
- **Theme**: Follows system theme preferences

## 🚀 Deployment

### Vercel Deployment (Recommended)

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Deploy the application:
```bash
vercel
```

3. Follow the prompts to complete deployment

### Alternative Deployment Platforms
- **Netlify**: Deploy via Git integration
- **Railway**: Connect GitHub repository
- **Heroku**: Use Heroku CLI
- **AWS Amplify**: Deploy with AWS services

## 🔍 Development

### Key Configuration Files

- `next.config.ts`: PWA and Next.js configuration
- `public/manifest.json`: Web App Manifest for PWA
- `pages/_document.tsx`: HTML document with manifest link
- `package.json`: Dependencies and scripts

### Environment Setup
```bash
# Development
npm run dev

# Production build
npm run build
npm run start

# Linting
npm run lint
```

## 📚 Learn More

### PWA Resources
- [Progressive Web Apps (MDN)](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)
- [Next PWA Documentation](https://ducanh-next-pwa.vercel.app/)
- [Web App Manifests](https://developer.mozilla.org/en-US/docs/Web/Manifest)
- [Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API)

### Next.js Resources
- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API
- [Learn Next.js](https://nextjs.org/learn-pages-router) - an interactive Next.js tutorial
- [Next.js GitHub repository](https://github.com/vercel/next.js) - feedback and contributions welcome

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is part of the ALX Software Engineering Program.

## 🔗 Links

- **Live Demo**: [Add your deployed URL here]
- **Repository**: [GitHub Repository](https://github.com/YOUR_USERNAME/alx-pwa-0x01)
- **Documentation**: [Project Documentation](https://github.com/YOUR_USERNAME/alx-pwa-0x01/wiki)

## 📞 Support

If you have any questions or need help with the project:
- Open an issue on GitHub
- Check the documentation
- Review the PWA testing guide above

---

**Made with ❤️ for the ALX Software Engineering Program**
