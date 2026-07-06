# Super Calculator

## Project overview
Calculadora básica construida con Angular 19 para fines didácticos.
Originalmente incluía 3 métodos vacíos (toggle sign, percent, theme
toggle) y una suite de tests con placeholders `pending()`, ambos ya
implementados como ejercicio.

## Tech stack
- Angular 19 (standalone components, sin NgModules)
- TypeScript 5.7
- Karma + Jasmine para unit tests

## How to run
- Instalar: `npm install`
- Servidor de desarrollo: `npm start` → http://localhost:4200
- Tests: `npm test`
- Build de producción: `npm run build` (salida en `dist/`)

## Project structure
- `src/app/app.component.ts` — toda la lógica: estado de la calculadora,
  manejo de dígitos/operadores, y los métodos de los ejercicios.
- `src/app/app.component.html` — template con el grid de botones y el
  binding de modo claro/oscuro.
- `src/app/app.component.css` — estilos del componente, incluida la
  variante `.light` para el tema claro.
- `src/app/app.component.spec.ts` — suite de tests (Karma + Jasmine).
- `requirements.md` — enunciado original del ejercicio (3 partes).

## Exercises
Los 3 métodos que originalmente estaban vacíos ya están implementados:
- `pressToggleSign()` — invierte el signo del número mostrado.
- `pressPercent()` — divide el número mostrado entre 100.
- `toggleTheme()` — alterna entre modo oscuro (default) y claro.

Los 12 tests marcados como `pending()` en `app.component.spec.ts`
también están completos.

## Coding conventions
- Componentes standalone (sin NgModule), como usa Angular 19+ por defecto.
- Comentarios JSDoc en métodos públicos explicando el propósito, no el detalle de implementación.
- Nombres de métodos con prefijo `press` para acciones disparadas por botones (`pressDigit`, `pressOperator`, etc.).
- Bloques CSS organizados por sección con comentarios `/* ── Sección ─ */`.
