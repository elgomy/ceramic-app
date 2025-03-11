# Ceramic Workshop App

Aplicación para la gestión de talleres de cerámica, incluyendo control de costos, procesos, productos y análisis con IA.

## Características

- Gestión de colecciones y productos
- Cálculo detallado de costos de producción
- Seguimiento de procesos de fabricación
- Análisis de costos con inteligencia artificial
- Dashboard con métricas clave
- Autenticación de usuarios

## Tecnologías

- Next.js 14
- Supabase (Autenticación y Base de datos)
- NextAuth.js
- OpenAI API
- TailwindCSS
- React Hook Form + Zod
- Chart.js
- Jest (Testing)

## Configuración

1. Clona este repositorio
2. Instala las dependencias:
   ```bash
   npm install
   ```
3. Crea un proyecto en Supabase y configura las variables de entorno
4. Obtén una API key de OpenAI
5. Configura el archivo `.env.local` con tus claves
6. Ejecuta el servidor de desarrollo:
   ```bash
   npm run dev
   ```

## Pruebas

La aplicación incluye pruebas de integración con Supabase. Para ejecutarlas:

1. Configura el archivo `.env.test` con tus credenciales de Supabase:
   ```
   NEXT_PUBLIC_SUPABASE_URL=tu_url_de_supabase
   NEXT_PUBLIC_SUPABASE_ANON_KEY=tu_clave_anon
   SUPABASE_SERVICE_ROLE_KEY=tu_clave_service_role
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=tu_secreto_nextauth
   ```

2. Ejecuta el script de pruebas:
   - En macOS/Linux:
     ```bash
     ./scripts/run-tests.sh
     ```
   - En Windows:
     ```bash
     scripts\run-tests.bat
     ```

3. También puedes ejecutar los comandos individualmente:
   ```bash
   # Verificar tablas en la base de datos
   npm run db:check
   
   # Configurar base de datos
   npm run db:setup
   
   # Ejecutar pruebas
   npm test
   
   # Ejecutar pruebas con cobertura
   npm run test:coverage
   ```

Las pruebas realizan las siguientes operaciones:
- Creación de usuario de prueba
- Configuración de horas de trabajo
- Creación de costes fijos
- Creación de procesos de producción
- Creación de colecciones y productos
- Asociación de procesos a productos
- Limpieza de datos de prueba

## Estructura del Proyecto

```
/ceramic-workshop-app
  /app
    /api - Endpoints de la API
    /components - Componentes reutilizables
    /lib - Utilidades y configuraciones
    /pages - Páginas de la aplicación
  /public - Archivos estáticos
  /__tests__ - Pruebas de la aplicación
  /scripts - Scripts de utilidad
```

## Licencia

MIT