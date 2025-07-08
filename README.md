# BlogCraft Elite - Luxury Blog CMS

A premium drag-and-drop blog content management system with luxury design aesthetics and advanced features.

![BlogCraft Elite](https://images.unsplash.com/photo-1499750310107-5fef28a66643?w=800&h=400&fit=crop)

## ✨ Features

- **Premium Authentication System** - Secure login and registration
- **Drag-and-Drop Editor** - Intuitive content block management
- **Luxury Design** - Apple-level design aesthetics with premium animations
- **Real-time Preview** - See your blog as you build it
- **Responsive Design** - Perfect on all devices
- **Premium Content Blocks** - Headings, paragraphs, images, quotes, lists, and dividers
- **Auto-save & Publishing** - Never lose your work
- **User Management** - Complete profile and settings system

## 🚀 Live Demo

Visit the live application: [BlogCraft Elite](https://wonderful-cheesecake-37e3e6.netlify.app)

## 🛠️ Tech Stack

- **Frontend**: React 18 + TypeScript
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Build Tool**: Vite
- **Deployment**: Netlify

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/blogcraft-elite.git
cd blogcraft-elite
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open [http://localhost:5173](http://localhost:5173) in your browser

## 🏗️ Build for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

## 🚀 Deployment

### Deploy to Netlify

1. Build the project:
```bash
npm run build
```

2. Deploy the `dist` folder to Netlify

### Deploy to GitHub Pages

1. Install gh-pages:
```bash
npm install --save-dev gh-pages
```

2. Add to package.json:
```json
{
  "homepage": "https://yourusername.github.io/blogcraft-elite",
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist"
  }
}
```

3. Deploy:
```bash
npm run deploy
```

## 🎨 Features Overview

### Authentication System
- Secure email/password authentication
- User profiles with avatars
- Premium and Enterprise plans
- Persistent sessions

### Content Editor
- Drag-and-drop content blocks
- Real-time editing
- Auto-save functionality
- Preview mode
- Responsive design

### Premium Content Blocks
- **Headings**: Elegant typography
- **Paragraphs**: Rich text content
- **Images**: High-resolution with smart optimization
- **Quotes**: Stunning blockquotes
- **Lists**: Beautiful bulleted lists
- **Dividers**: Elegant section separators

### User Experience
- Smooth animations and transitions
- Intuitive drag-and-drop interface
- Responsive design for all devices
- Premium loading states
- Contextual notifications

## 🔧 Development

### Project Structure
```
src/
├── components/          # React components
│   ├── AuthModal.tsx   # Authentication modal
│   ├── ContentBlocks.tsx # Content editor and blocks
│   ├── Header.tsx      # Application header
│   ├── SettingsModal.tsx # User settings
│   └── Sidebar.tsx     # Content blocks sidebar
├── hooks/              # Custom React hooks
│   ├── useAuth.ts      # Authentication logic
│   └── useBlogState.ts # Blog state management
├── types/              # TypeScript type definitions
└── App.tsx            # Main application component
```

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## 🎯 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

For support, email support@blogcraft-elite.com or join our Discord community.

## 🙏 Acknowledgments

- Design inspiration from Apple's design principles
- Icons by [Lucide](https://lucide.dev/)
- Images from [Unsplash](https://unsplash.com/)
- Built with [Vite](https://vitejs.dev/) and [React](https://reactjs.org/)

---

Made with ❤️ by the BlogCraft Elite team