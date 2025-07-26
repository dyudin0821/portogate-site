# PortoGate Landing Page

Современный лендинг для проекта PortoGate, построенный на Astro с поддержкой мультиязычности и автоматическим деплоем на GitHub Pages.

## ✨ Особенности

- 🚀 **Astro** - быстрая генерация статических сайтов
- 🎨 **TailwindCSS** - современные стили и адаптивность
- 🌍 **Мультиязычность** - поддержка русского и английского языков
- 📱 **Responsive** - корректное отображение на всех устройствах
- ⚡ **Высокая производительность** - оптимизация для скорости
- 🔄 **Автоматический деплой** - GitHub Actions для CI/CD
- 📝 **MDX поддержка** - для создания документации
- 🎯 **SEO оптимизация** - мета-теги и структурированные данные

## � Технологический стек

- **Frontend:** Astro, TailwindCSS, TypeScript
- **Иконки:** Tabler Icons, Lucide
- **Документация:** MDX
- **Деплой:** GitHub Pages
- **CI/CD:** GitHub Actions

## 🚀 Быстрый старт

### Требования

- Node.js 18+ 
- npm или yarn

### Установка

```bash
# Клонирование репозитория
git clone https://github.com/your-username/portogate.git
cd portogate/site

# Установка зависимостей
npm install

# Запуск dev сервера
npm run dev
```

Сайт будет доступен по адресу `http://localhost:4321`

### Основные команды

```bash
# Разработка
npm run dev

# Сборка для продакшена
npm run build

# Предварительный просмотр сборки
npm run preview

# Проверка кода
npm run astro check
```

## 📁 Структура проекта

```
site/
├── public/                 # Статические файлы
│   ├── images/            # Изображения
│   └── favicon.svg        # Favicon
├── src/
│   ├── components/        # Компоненты Astro
│   │   ├── Navigation.astro
│   │   ├── Hero.astro
│   │   ├── Features.astro
│   │   ├── HowItWorks.astro
│   │   ├── Pricing.astro
│   │   ├── FAQ.astro
│   │   └── Footer.astro
│   ├── layouts/           # Макеты страниц
│   │   └── Layout.astro
│   ├── pages/             # Страницы сайта
│   │   ├── ru/           # Русская версия
│   │   ├── en/           # Английская версия
│   │   └── index.astro   # Редирект на /ru/
│   ├── styles/           # Глобальные стили
│   │   └── global.css
│   └── utils/            # Утилиты
│       └── i18n.ts       # Система переводов
├── astro.config.mjs      # Конфигурация Astro
└── tailwind.config.js    # Конфигурация Tailwind
```

## 🌍 Мультиязычность

Сайт поддерживает два языка:
- **Русский** (`/ru/`) - основной язык
- **Английский** (`/en/`) - дополнительный язык

Переводы хранятся в файле `src/utils/i18n.ts`.

### Добавление нового перевода

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

## 🎨 Дизайн-система

### Цветовая палитра

- **Основной:** `#0E1E2F`
- **Фон:** `#0A0A0A` 
- **Акцент:** `#4F81C7`
- **Границы:** `#DDE3EC`

### Компоненты

Все компоненты следуют принципам:
- Responsive дизайн (mobile-first)
- Темная тема по умолчанию
- Плавные анимации и переходы
- Доступность (a11y)

## 🚀 Деплой

### GitHub Pages (автоматически)

1. Пуш в ветку `main`
2. GitHub Actions автоматически собирает и деплоит сайт
3. Сайт доступен по адресу `https://your-username.github.io/portogate`

### Ручной деплой

```bash
# Сборка
npm run build

# Деплой папки dist/ на ваш хостинг
```

## 📝 Контент

### Добавление новой страницы

1. Создайте файл в `src/pages/ru/` и `src/pages/en/`
2. Используйте макет `Layout.astro`
3. Добавьте навигацию при необходимости

### Документация

Документация создается в формате MDX в папках:
- `src/pages/ru/docs/`
- `src/pages/en/docs/`

## 🔧 Конфигурация

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

### Обновление ссылок

Обновите ссылки на Telegram-бота в компонентах:
- `src/components/Hero.astro`
- `src/components/Pricing.astro`
- `src/components/Footer.astro`

## 📊 Производительность

Целевые показатели Lighthouse:
- **Performance:** 90+
- **Accessibility:** 90+
- **Best Practices:** 90+
- **SEO:** 90+

## 🤝 Контрибьюция

1. Форкните репозиторий
2. Создайте ветку для фичи (`git checkout -b feature/amazing-feature`)
3. Коммитьте изменения (`git commit -m 'Add amazing feature'`)
4. Пушьте в ветку (`git push origin feature/amazing-feature`)
5. Откройте Pull Request

