# PortoGate Landing Page

Modern landing page for the PortoGate project, built with Astro featuring multilingual support and automated deployment to GitHub Pages.

## ✨ Features

- 🚀 **Astro** - fast static site generation
- 🎨 **TailwindCSS** - modern styling and responsiveness
- 🌍 **Multilingual** - Russian and English language support
- 📱 **Responsive** - proper display on all devices
- ⚡ **High Performance** - optimized for speed
- 🔄 **Automated Deployment** - GitHub Actions for CI/CD
- 📝 **MDX Support** - for creating documentation
- 🎯 **SEO Optimization** - meta tags and structured data

## 🛠 Tech Stack

- **Frontend:** Astro, TailwindCSS, TypeScript
- **Icons:** Tabler Icons, Lucide
- **Documentation:** MDX
- **Deployment:** GitHub Pages
- **CI/CD:** GitHub Actions

## 🚀 Quick Start

### Requirements

- Node.js 18+ 
- npm or yarn

### Installation

```bash
# Clone repository
git clone https://github.com/your-username/portogate.git
cd portogate/site

# Install dependencies
npm install

# Start dev server
npm run dev
```

The site will be available at `http://localhost:4321`

### Main Commands

```bash
# Development
npm run dev

# Production build
npm run build

# Preview build
npm run preview

# Code check
npm run astro check
```

## 📁 Project Structure

```
site/
├── public/                 # Static files
│   ├── images/            # Images
│   └── favicon.svg        # Favicon
├── src/
│   ├── components/        # Astro components
│   │   ├── Navigation.astro
│   │   ├── Hero.astro
│   │   ├── Features.astro
│   │   ├── HowItWorks.astro
│   │   ├── Pricing.astro
│   │   ├── FAQ.astro
│   │   └── Footer.astro
│   ├── layouts/           # Page layouts
│   │   └── Layout.astro
│   ├── pages/             # Site pages
│   │   ├── ru/           # Russian version
│   │   ├── en/           # English version
│   │   └── index.astro   # Redirect to /ru/
│   ├── styles/           # Global styles
│   │   └── global.css
│   └── utils/            # Utilities
│       └── i18n.ts       # Translation system
├── astro.config.mjs      # Astro configuration
└── tailwind.config.js    # Tailwind configuration
```

## 🌍 Internationalization

The site supports two languages:
- **Russian** (`/ru/`) - primary language
- **English** (`/en/`) - secondary language

Translations are stored in the `src/utils/i18n.ts` file.

### Adding New Translation

```typescript
export const ui = {
  ru: {
    'new.key': 'Новый текст',
  },
  en: {
    'new.key': 'New text',
  },
} as const;
```

## 🎨 Design System

### Color Palette

- **Primary:** `#0E1E2F`
- **Background:** `#0A0A0A` 
- **Accent:** `#4F81C7`
- **Borders:** `#DDE3EC`

### Components

All components follow these principles:
- Responsive design (mobile-first)
- Dark theme by default
- Smooth animations and transitions
- Accessibility (a11y)

## 🚀 Deployment

### GitHub Pages (Automatic)

1. Push to `main` branch
2. GitHub Actions automatically builds and deploys the site
3. Site is available at `https://your-username.github.io/portogate`

### Manual Deployment

```bash
# Build
npm run build

# Deploy dist/ folder to your hosting
```

## 📝 Content

### Adding a New Page

1. Create a file in `src/pages/ru/` and `src/pages/en/`
2. Use the `Layout.astro` layout
3. Add navigation if needed

### Documentation

Documentation is created in MDX format in folders:
- `src/pages/ru/docs/`
- `src/pages/en/docs/`

## 🔧 Configuration

### Astro (astro.config.mjs)

```javascript
export default defineConfig({
  site: 'https://your-username.github.io',
  base: '/portogate',
  integrations: [tailwind(), mdx()],
  i18n: {
    defaultLocale: 'ru',
    locales: ['ru', 'en'],
  }
});
```

### Updating Links

Update Telegram bot links in components:
- `src/components/Hero.astro`
- `src/components/Pricing.astro`
- `src/components/Footer.astro`

## 📊 Performance

Target Lighthouse scores:
- **Performance:** 90+
- **Accessibility:** 90+
- **Best Practices:** 90+
- **SEO:** 90+

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

