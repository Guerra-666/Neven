# Neven Landing Page

[![Astro](https://img.shields.io/badge/Astro-FF5D01?style=flat&logo=astro&logoColor=white)](https://astro.build/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-38B2AC?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)


### Características principales

- **Rendimiento optimizado**: Tiempo de carga inferior a 2 segundos
- **Diseño responsivo**: Compatible con todos los dispositivos
- **SEO integrado**: Configuración completa para motores de búsqueda
- **Gestión de contenido**: Edición sencilla mediante archivos JSON
- **Componentes modulares**: Arquitectura escalable y mantenible

## Stack Tecnológico

| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| **[Astro](https://astro.build/)** | v4.x | Framework de sitios estáticos |
| **[TailwindCSS](https://tailwindcss.com/)** | v3.x | Framework de CSS utilitario |
| **[SwiperJS](https://swiperjs.com/)** | v11.x | Carruseles y componentes interactivos |
| **[Sharp](https://sharp.pixelplumbing.com/)** | v0.32.x | Optimización de imágenes |

## Estructura del Proyecto

```
neven-landing-page/
│
├── public/                       # Archivos estáticos públicos
│   ├── favicon.svg               # Icono del sitio
│   ├── manifest.json             # Configuración PWA
│   └── content-images/           # Imágenes de contenido
│
├── src/                          # Código fuente
│   ├── assets/                   # Recursos del proyecto
│   │   ├── css/                  # Estilos personalizados
│   │   ├── fonts/                # Tipografías
│   │   └── theme-images/         # Imágenes del tema
│   │
│   ├── components/               # Componentes Astro
│   │   ├── CardCaseStudy.astro   # Tarjeta de caso de estudio
│   │   ├── CaseStudiesSection.astro # Sección de casos de éxito
│   │   ├── ClientsSection.astro  # Sección de clientes
│   │   ├── DetailsAccordion.astro # Componente acordeón
│   │   ├── DialogModal.astro     # Modal de diálogo
│   │   ├── FaqSection.astro      # Preguntas frecuentes
│   │   ├── FooterMain.astro      # Pie de página
│   │   ├── HeaderMain.astro      # Cabecera de navegación
│   │   ├── HeroSection.astro     # Sección principal
│   │   ├── NewsletterSection.astro # Newsletter
│   │   ├── PricingSection.astro  # Precios
│   │   ├── QuoteSection.astro    # Cotización
│   │   ├── ServicesCarousel.astro # Carrusel de servicios
│   │   └── TestimonialsSection.astro # Testimonios
│   │
│   ├── data/                     # Datos en formato JSON
│   │   ├── case_studies.json     # Casos de estudio
│   │   ├── clients.json          # Lista de clientes
│   │   ├── credits.json          # Créditos
│   │   ├── faq.json              # Preguntas frecuentes
│   │   ├── global_settings.json  # Configuración global
│   │   ├── home.json             # Contenido página principal
│   │   ├── newsletter.json       # Configuración newsletter
│   │   ├── pricing.json          # Planes y precios
│   │   ├── services.json         # Servicios
│   │   └── testimonials.json     # Testimonios
│   │
│   ├── layouts/                  # Plantillas base
│   │   └── Layout.astro          # Layout principal
│   │
│   └── pages/                    # Páginas del sitio
│       ├── index.astro           # Página principal
│       └── credits.astro         # Página de créditos
│
├── astro.config.mjs              # Configuración Astro
├── package.json                  # Dependencias
├── pnpm-lock.yaml                # Lock de dependencias
└── tsconfig.json                 # Configuración TypeScript
```

## Instalación

### Prerrequisitos

- Node.js 18 o superior
- pnpm (recomendado)

### Pasos de instalación

```bash
# Clonar el repositorio
git clone git@github.com:Guerra-666/Neven.git

# Navegar al directorio
cd neven

# Instalar dependencias
pnpm install

# Iniciar servidor de desarrollo
pnpm dev
```

El sitio estará disponible en `http://localhost:4321`

## Comandos Disponibles

| Comando | Descripción |
|---------|-------------|
| `pnpm install` | Instala las dependencias del proyecto |
| `pnpm dev` | Inicia el servidor de desarrollo |
| `pnpm build` | Genera la build de producción |
| `pnpm preview` | Previsualiza la build de producción |
| `pnpm astro check` | Ejecuta verificación de tipos TypeScript |
| `pnpm astro add [integración]` | Añade una nueva integración |

## Configuración

### Contenido

El contenido se gestiona a través de archivos JSON ubicados en `src/data/`. Cada archivo corresponde a una sección específica del sitio.

Ejemplo de configuración de servicios:

```json
// src/data/services.json
{
  "services": [
    {
      "title": "Desarrollo Web",
      "description": "Sitios web modernos y responsivos",
      "icon": "web",
      "price": "$25,000 MXN"
    }
  ]
}
```

Ejemplo de configuración global:

```json
// src/data/global_settings.json
{
  "company": {
    "name": "Neven",
    "email": "contacto@neven.tech",
    "phone": "+52 442 XXX XXXX",
    "address": "Querétaro, México"
  }
}
```

### Personalización de estilos

El proyecto utiliza TailwindCSS. Los estilos se pueden personalizar en `astro.config.mjs`:

```javascript
// astro.config.mjs
export default defineConfig({
  integrations: [
    tailwind({
      config: {
        theme: {
          extend: {
            colors: {
              primary: '#3B82F6',
              secondary: '#10B981',
              accent: '#F59E0B'
            }
          }
        }
      }
    })
  ]
})
```

## Despliegue

### Proceso de despliegue

```bash
# Generar build de producción
pnpm build

# El directorio dist/ contiene los archivos para el servidor
```

## Optimizaciones incluidas

### Rendimiento
- Lazy loading automático de imágenes
- Minificación de CSS y JavaScript
- Compresión automática de imágenes con Sharp
- Código splitting automático

### SEO
- Meta tags configurables por página
- Open Graph tags para redes sociales
- Schema markup estructurado
- Sitemap XML generado automáticamente

### Accesibilidad
- Contraste de colores WCAG AA
- Navegación por teclado
- Atributos ARIA apropiados
- Semántica HTML correcta

## Solución de problemas

### Errores comunes

**Error: "Cannot find module"**
```bash
rm -rf node_modules pnpm-lock.yaml
pnpm install
```

**Error: "Port already in use"**
```bash
pnpm dev --port 3000
```

**Imágenes no se cargan**
- Verificar que las imágenes estén en `public/` para acceso directo
- O en `src/assets/` para procesamiento automático
- Comprobar las rutas en los componentes

**Estilos no se aplican**
```bash
# Reiniciar servidor de desarrollo
pnpm dev
```

## Recursos

### Documentación
- [Astro Documentation](https://docs.astro.build/)
- [TailwindCSS Documentation](https://tailwindcss.com/docs)
- [SwiperJS Documentation](https://swiperjs.com/get-started)

### Herramientas útiles
- [Tailwind UI](https://tailwindui.com/) - Componentes premium
- [Heroicons](https://heroicons.com/) - Iconos SVG
- [Unsplash](https://unsplash.com/) - Imágenes gratuitas

## Contribución

Para contribuir al proyecto:

1. Fork el repositorio
2. Crear una rama feature: `git checkout -b feature/nueva-funcionalidad`
3. Commit los cambios: `git commit -m 'Añadir nueva funcionalidad'`
4. Push a la rama: `git push origin feature/nueva-funcionalidad`
5. Crear un Pull Request

### Estándares de código

- Utilizar TypeScript para nuevo código
- Seguir las convenciones de TailwindCSS
- Documentar funciones y componentes complejos
- Probar en dispositivos móviles y desktop

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---