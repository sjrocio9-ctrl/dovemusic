# 🎵 MusicFlow - Aplicación de Streaming de Música Urbana

[![React](https://img.shields.io/badge/React-18.0-blue.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue.svg)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-4.0-38B2AC.svg)](https://tailwindcss.com/)
[![Deezer API](https://img.shields.io/badge/Deezer-API-FF6600.svg)](https://developers.deezer.com/)

## 📖 Descripción

MusicFlow es una moderna aplicación web de streaming de música enfocada en música urbana y reggaeton. Permite a los usuarios buscar, descubrir y reproducir canciones de los artistas más populares como Bad Bunny, Rauw Alejandro, Karol G, Feid, y muchos más.

## ✨ Características Principales

- 🔍 **Búsqueda Inteligente**: Búsqueda en tiempo real por artista, canción o álbum
- 🎨 **Diseño Moderno**: Interfaz dark theme con estética urbana
- 📱 **Responsive Design**: Optimizado para móviles, tablets y desktop
- 🔄 **Sistema de Fallback**: API de Deezer con fallback a base de datos local
- 🎵 **40+ Canciones**: Base de datos completa de música urbana
- 🚀 **Componentes Modulares**: Arquitectura clean con 4 componentes principales

## 🛠️ Tecnologías Utilizadas

- **Frontend**: React 18 + TypeScript
- **Styling**: Tailwind CSS v4.0
- **UI Components**: shadcn/ui
- **Icons**: Lucide React
- **API**: Deezer API + Sistema de proxies
- **Images**: Unsplash API para covers
- **State Management**: React Hooks

## 📁 Estructura del Proyecto

```
musicflow/
├── App.tsx                    # Componente principal
├── components/
│   ├── NavBar.tsx            # Barra de navegación
│   ├── HeroSection.tsx       # Página de inicio
│   ├── SearchResults.tsx     # Resultados de búsqueda  
│   ├── TrackCard.tsx         # Tarjeta de canción
│   ├── figma/
│   │   └── ImageWithFallback.tsx
│   └── ui/                   # Componentes shadcn/ui
├── docs/
│   ├── FUNCIONALIDAD.md      # Documentación de funcionalidades
│   ├── DISEÑO.md            # Documentación de diseño
│   └── API_ENDPOINTS.md     # Documentación de APIs
├── styles/
│   └── globals.css          # Estilos globales Tailwind
└── README.md
```

## 🚀 Instalación y Uso

### Prerrequisitos
- Node.js 18+
- npm o yarn

### Instalación
```bash
# Clonar el repositorio
git clone https://github.com/tuusuario/musicflow.git

# Navegar al directorio
cd musicflow

# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev
```

### Comandos Disponibles
```bash
npm run dev      # Servidor de desarrollo
npm run build    # Build de producción
npm run preview  # Preview del build
npm run lint     # Linting del código
```

## 🎯 Funcionalidades

### 🔍 Búsqueda de Música
- Búsqueda en tiempo real mientras escribes
- Filtros por artista, canción o álbum
- Sugerencias automáticas de artistas populares
- Resultados instantáneos con feedback visual

### 🎨 Exploración por Géneros
- **Reggaeton** 🔥: Los hits más candentes
- **Trap Latino** 💜: Lo último en trap urbano
- **Perreo** 🎵: Puro perreo para la pista
- **Urbano** 🌆: Música urbana contemporánea

### 👨‍🎤 Artistas Destacados
- **Bad Bunny**: Tití Me Preguntó, Me Porto Bonito, Ojitos Lindos, Moscow Mule
- **Rauw Alejandro**: Todo de Ti, Punto 40, Despertar, Vampiros
- **Karol G**: MAMIII, Provenza, Gatúbela, Bichota
- **Feid**: Normal, Porfa, Que Raro, FERXXO 151
- **Myke Towers**: LALA, Bandido, Diosa
- **Rels B**: La Última Canción, Buenos Días, Por Ti
- Y muchos más...

## 🏗️ Arquitectura

### Componentes Principales

#### 1. NavBar
- Barra de navegación con gradiente urbano
- Buscador integrado con botón
- Logo y branding consistente

#### 2. HeroSection  
- Página de inicio con hero banner
- Artistas destacados y géneros populares
- Grid de canciones más escuchadas

#### 3. SearchResults
- Manejo de estados (carga, error, vacío, resultados)
- Grid responsivo de resultados
- Información contextual

#### 4. TrackCard
- Tarjeta individual para cada canción
- Imagen del álbum con efectos hover
- Información completa (título, artista, duración)
- Enlace directo a Deezer

### 🔌 Integración con APIs

#### Deezer API
- **Endpoint**: `https://api.deezer.com/search`
- **Proxies**: AllOrigins, CORS Anywhere, CodeTabs
- **Timeout**: 8 segundos por request
- **Fallback**: Datos locales cuando falla

#### Sistema de Proxies
```typescript
const proxies = [
  'https://api.allorigins.win/raw?url=',
  'https://cors-anywhere.herokuapp.com/',
  'https://api.codetabs.com/v1/proxy?quest='
];
```

## 📱 Responsive Design

### Breakpoints
- **Mobile**: < 768px (1 columna)
- **Tablet**: 768px - 1024px (2 columnas)  
- **Desktop**: 1024px - 1280px (3 columnas)
- **Large**: > 1280px (4 columnas)

### Optimizaciones Mobile
- Touch-friendly buttons
- Optimized font sizes
- Swipe-friendly cards
- Fast loading images

## 🎨 Sistema de Diseño

### Colores
- **Primary**: Cyan (400-600)
- **Secondary**: Purple (500-600)
- **Background**: Gray-900 gradients
- **Text**: White / Cyan-300
- **Accent**: Genre-specific gradients

### Tipografía
- **Font Stack**: Sistema sans-serif
- **Weights**: 400 (normal), 500 (medium), 700 (bold)
- **Sizes**: Responsive con clamp()

## 🔧 Configuración

### Environment Variables
```env
# Opcional: URLs de proxy personalizadas
VITE_PROXY_1=https://api.allorigins.win/raw?url=
VITE_PROXY_2=https://cors-anywhere.herokuapp.com/
VITE_PROXY_3=https://api.codetabs.com/v1/proxy?quest=
```

### Tailwind Config
El proyecto usa Tailwind CSS v4.0 con configuración en `styles/globals.css`.

## 📊 Performance

### Métricas
- **First Contentful Paint**: < 1.5s
- **Largest Contentful Paint**: < 2.5s
- **Time to Interactive**: < 3.5s
- **Cumulative Layout Shift**: < 0.1

### Optimizaciones
- Lazy loading de imágenes
- Code splitting por componentes
- Optimized bundle size
- Efficient re-renders

## 🚦 Estados de la Aplicación

### Estados Implementados
- ✅ **Loading**: Spinner con mensaje contextual
- ✅ **Error**: Manejo elegante con retry
- ✅ **Empty**: Sin resultados con sugerencias
- ✅ **Success**: Grid de resultados
- ✅ **Initial**: Página de bienvenida

## 🧪 Testing

### Casos de Prueba
- [x] Búsqueda básica funciona
- [x] Fallback a datos mock funciona
- [x] Responsive design en móviles
- [x] Estados de error se muestran
- [x] Links a Deezer funcionan
- [x] Imágenes cargan correctamente

## 🔮 Roadmap

### v2.0 (Próximas Features)
- [ ] Playlists personalizadas
- [ ] Sistema de favoritos
- [ ] Historial de búsquedas
- [ ] Modo offline
- [ ] Compartir canciones
- [ ] Dark/Light mode toggle

### v3.0 (Futuro)
- [ ] Usuario registrado
- [ ] Recomendaciones IA
- [ ] Social features
- [ ] Mobile app
- [ ] API propia

## 🤝 Contribución

### Cómo Contribuir
1. Fork el proyecto
2. Crea una feature branch (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -m 'Agrega nueva funcionalidad'`)
4. Push a la branch (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

### Guidelines
- Seguir las convenciones de TypeScript
- Mantener consistencia en el diseño
- Agregar tests para nuevas funcionalidades
- Documentar cambios importantes

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver `LICENSE` para más detalles.

## 👥 Créditos

### APIs y Servicios
- **Deezer API**: Datos de música
- **Unsplash**: Imágenes de álbumes
- **AllOrigins/CORS Anywhere**: Servicios de proxy

### UI/UX
- **shadcn/ui**: Componentes base
- **Lucide React**: Iconografía
- **Tailwind CSS**: Sistema de diseño

## 📧 Contacto

- **Proyecto**: [GitHub Repository](https://github.com/tuusuario/musicflow)
- **Issues**: [GitHub Issues](https://github.com/tuusuario/musicflow/issues)
- **Documentación**: Ver carpeta `/docs/`

---

**¡Hecho con ❤️ para los amantes de la música urbana!** 🎵
