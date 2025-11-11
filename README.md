# Tech Innovator Portfolio

A futuristic, animated portfolio website showcasing IoT, AI, and Web Technologies. Built with Next.js, TypeScript, Tailwind CSS, Framer Motion, and Three.js.

## Features

- 🎨 **Futuristic Design**: Neon blue + black + cyber purple gradients with glassmorphism effects
- ✨ **Animated Sections**: Hero, About, Experience, Projects, Skills, Achievements, and Contact
- 🎭 **3D Animations**: Interactive 3D brain mesh using Three.js
- 💫 **Particle Background**: Interactive particle system that reacts to mouse movement
- 🤖 **AI Chatbot**: Nisha AI assistant for interactive guidance
- 📱 **Fully Responsive**: Optimized for all device sizes
- 🎯 **Smooth Animations**: Scroll-triggered animations using Framer Motion
- 🌙 **Dark Theme**: Futuristic dark theme with neon accents
- 💾 **SQLite Database**: Local database for storing contact submissions and projects

## Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **3D Graphics**: Three.js, React Three Fiber
- **Particles**: TSParticles
- **Database**: SQLite (better-sqlite3)
- **Icons**: Lucide React
- **Fonts**: Orbitron (headings) + Poppins (body)

## Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn/pnpm

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd gk
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables (optional):
Create a `.env.local` file in the root directory if needed:
```env
# Optional: Add any additional environment variables here
```

**Note**: The contact form now uses SQLite database instead of Formspree. All submissions are stored locally in `data/portfolio.db`.

4. Update your personal information:
Edit `lib/constants.ts` to add your:
- Personal info (name, email, social links)
- Education details
- Work experience
- Projects
- Skills
- Achievements

5. Run the development server:
```bash
npm run dev
```

6. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Project Structure

```
├── app/
│   ├── layout.tsx          # Root layout with fonts and metadata
│   ├── page.tsx            # Main page with all sections
│   └── globals.css         # Global styles and animations
├── components/
│   ├── Hero.tsx            # Hero section with typing animation
│   ├── About.tsx           # About section with timeline
│   ├── Experience.tsx      # Experience cards with flip effects
│   ├── Projects.tsx        # Projects showcase with modals
│   ├── Skills.tsx          # Skills with 3D brain visualization
│   ├── Achievements.tsx    # Achievements section
│   ├── Contact.tsx         # Contact form with Formspree
│   ├── Chatbot.tsx         # Nisha AI chatbot
│   ├── Navigation.tsx      # Navigation bar
│   ├── ParticleBackground.tsx  # Particle animation
│   ├── CursorEffect.tsx    # Cursor reactive effects
│   ├── ThemeToggle.tsx     # Theme toggle (future use)
│   ├── Timeline.tsx        # Education timeline component
│   ├── 3DBrain.tsx         # 3D brain mesh component
│   └── ProjectModal.tsx    # Project detail modal
├── lib/
│   ├── constants.ts        # Personal data and constants
│   ├── animations.ts       # Framer Motion animation variants
│   ├── utils.ts            # Utility functions
│   ├── db.ts               # SQLite database setup
│   └── db-utils.ts         # Database utility functions
├── app/
│   └── api/
│       ├── contact/        # Contact form API route
│       └── projects/       # Projects API route
├── data/
│   └── portfolio.db        # SQLite database (created automatically)
└── public/
    ├── images/             # Project images and logos
    ├── lottie/             # Lottie animation files
    └── sounds/             # Sound effects (optional)
```

## Customization

### Colors

Edit `app/globals.css` to customize the color palette:
- `--neon-blue`: Primary neon blue color
- `--cyber-purple`: Cyber purple color
- `--dark-bg`: Dark background color

### Content

Update `lib/constants.ts` with your personal information:
- Personal info
- Education history
- Work experience
- Projects
- Skills
- Achievements
- Social links

### Animations

Modify `lib/animations.ts` to adjust animation timings and effects.

## Database

The project uses SQLite for local data storage. The database is automatically created in the `data/` directory when you first run the application.

### Database Tables

- **contact_submissions**: Stores contact form submissions
- **projects**: Stores project information
- **blog_posts**: Stores blog posts (for future use)

### API Endpoints

- `POST /api/contact` - Submit a contact form message
- `GET /api/contact` - Get all contact submissions (for admin use)
- `GET /api/projects` - Get all projects
- `POST /api/projects` - Create a new project

### Viewing Database

You can use any SQLite browser tool to view the database:
- [DB Browser for SQLite](https://sqlitebrowser.org/)
- [SQLite Viewer (Online)](https://sqliteviewer.app/)

The database file is located at: `data/portfolio.db`

## Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import your repository to [Vercel](https://vercel.com)
3. **Note**: SQLite works locally but for production, consider using a cloud database like:
   - Vercel Postgres
   - Supabase
   - PlanetScale
   - Or keep SQLite for simple deployments
4. Deploy!

### Other Platforms

The project can be deployed to any platform that supports Next.js:
- Netlify
- AWS Amplify
- Railway
- Heroku

**Important**: For production deployments, you may want to migrate from SQLite to a cloud database service for better scalability and reliability.

## Features to Add (Optional)

- [ ] Light mode theme
- [ ] Sound effects on interactions
- [ ] More Lottie animations
- [ ] Blog section
- [ ] Resume download button
- [ ] Analytics integration
- [ ] Performance monitoring

## License

This project is open source and available under the MIT License.

## Credits

- Design inspired by futuristic tech portfolios
- Icons by [Lucide](https://lucide.dev)
- Fonts by [Google Fonts](https://fonts.google.com)

## Contact

For questions or suggestions, feel free to reach out through the contact form on the website!
