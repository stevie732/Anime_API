# Build Modern Next 14 Server Side App with Server Actions, Infinite Scroll & Framer Motion Animations

# 🎌 Anime Card Component

A modern, animated React component for displaying anime information with a sleek user interface. Built with Next.js, TypeScript, and Framer Motion.

## 🌟 Features

- Smooth fade-in animations with staggered delays
- Responsive image display with Next.js Image optimization
- Clean typography and layout using Tailwind CSS
- Episode count and rating display
- Adaptive content handling for varying data types

## 🛠️ Technical Stack

- **Framework**: Next.js
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Animation**: Framer Motion
- **Image Optimization**: Next.js Image Component

## 📋 Component Structure

### Props Interface

```typescript
interface AnimeProp {
  id: string;
  name: string;
  image: {
    original: string;
  };
  kind: string;
  episodes: number;
  episodes_aired: number;
  score: string;
}

interface Prop {
  anime: AnimeProp;
  index: number;
}
Copy
Insert

Animation Configuration
const stagger = 0.25;
const variants = {
  hidden: { opacity: 0 },
  visible: { opacity: 1 },
};
Copy
Insert

🎨 Styling Details
The component features:

Maximum width of sm (small) breakpoint
Rounded corners for card and image
Flexible height with 37vh for the image container
Dark theme colors with white text
Custom background color (#161921) for anime type label
Orange-tinted score display (#FFAD49)
📱 Layout Components
Image Container
Full-width responsive container
Aspect ratio maintained using Next.js Image fill
Rounded corners (xl)
Content Section
Flexible column layout
Spacing between elements using gap utilities
Two main information rows:
Title and type
Episodes and score
Metadata Display
SVG icons for episodes and ratings
Responsive text sizing
Bold typography for emphasis
🚀 Usage
import AnimeCard from './components/AnimeCard';

// Example usage in a parent component
function AnimeList() {
  return (
    <div>
      {animeData.map((anime, index) => (
        <AnimeCard 
          key={anime.id}
          anime={anime}
          index={index}
        />
      ))}
    </div>
  );
}
Copy
Insert

⚙️ Installation Requirements
Install dependencies:
npm install framer-motion next-images tailwindcss
Copy
Insert

Required assets:
episodes.svg
star.svg
🎯 Best Practices
Uses TypeScript for type safety
Implements responsive design principles
Follows accessibility guidelines with proper alt texts
Optimizes images using Next.js Image component
Implements smooth animations with Framer Motion
Uses semantic HTML structure
📝 Notes
Images are served from shikimori.one domain
Requires configuration of Next.js Image domains
Animation delay is calculated based on index position
Fallback handling for episodes/episodes_aired
🔧 Configuration
Add the following to your next.config.js:

module.exports = {
  images: {
    domains: ['shikimori.one'],
  },
}
Copy
Insert

