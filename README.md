# Shadcn Map 🗺️

A premium, declarative mapping component library for Next.js, built on top of **Leaflet** and inspired by the **Shadcn UI** philosophy. This project provides a set of highly customizable, accessible, and beautiful map components that feel right at home in any modern React application.

## ✨ Features

- **🚀 Next.js 15 & React 19 Ready**: Optimized for the latest web standards, including full support for React Server Components and experimental features.
- **🧩 Declarative API**: Manage your maps using familiar React patterns. No more imperative Leaflet code.
- **🎨 Shadcn-Inspired UI**: Beautifully crafted controls (zoom, layers, fullscreen) built with Radix UI and Tailwind CSS.
- **📍 Advanced Mapping Tools**:
  - **Drawing & Editing**: Integrated drawing tools for markers, polylines, polygons, circles, and rectangles.
  - **Marker Clustering**: Effortlessly handle thousands of markers with built-in clustering support.
  - **Custom Popups & Tooltips**: Fully stylable popups and tooltips that follow your application's design system.
  - **Layer Management**: Sophisticated layer control with support for multiple tile providers and feature groups.
- **🌓 Theme Support**: Seamless integration with `next-themes` for flawless light and dark mode support.
- **📱 Responsive & Accessible**: Built with mobile users and accessibility in mind.

## 🛠️ Tech Stack

- **Framework**: [Next.js 15.1](https://nextjs.org/)
- **Core Library**: [React 19](https://react.dev/)
- **Mapping**: [Leaflet](https://leafletjs.com/) & [React-Leaflet](https://react-leaflet.js.org/)
- **UI Components**: [Radix UI](https://www.radix-ui.com/) & [Lucide Icons](https://lucide.dev/)
- **Styling**: [Tailwind CSS 4](https://tailwindcss.com/)
- **Type Safety**: [TypeScript](https://www.typescriptlang.org/) & [Zod](https://zod.dev/)
- **Linting**: [Biome](https://biomejs.dev/)

## 🚀 Getting Started

### Prerequisites

- Node.js 20+
- pnpm (recommended)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/map-experimental.git
   cd map-experimental
   ```

2. **Install dependencies:**
   ```bash
   pnpm install
   ```

3. **Run the development server:**
   ```bash
   pnpm dev
   ```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the interactive map.

## 📖 Usage Example

```tsx
import { Map, MapLayers, MapTileLayer, MapMarker, MapPopup, MapZoomControl } from "@/components/ui/map";

export default function Home() {
  return (
    <Map center={[40.7128, -74.006]} zoom={12} className="h-screen w-full">
      <MapLayers defaultTileLayer="Street">
        <MapTileLayer name="Street" />
        <MapTileLayer 
            name="Satellite" 
            url="https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}" 
        />
        
        <MapMarker position={[40.7128, -74.006]}>
          <MapPopup>
            <div className="p-2">
              <h3 className="font-bold">New York City</h3>
              <p>The city that never sleeps.</p>
            </div>
          </MapPopup>
        </MapMarker>
        
        <MapZoomControl />
      </MapLayers>
    </Map>
  );
}
```

## 📂 Project Structure

- `src/app`: Next.js App Router structure.
- `src/components/ui/map.tsx`: The powerhouse component containing all map-related logic and sub-components.
- `src/components/map`: Higher-level map implementations and examples.
- `src/components/ui`: Core UI components (buttons, dropdowns, etc.) following the Shadcn pattern.
- `public`: Static assets including map markers and icons.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details (if applicable).
