# Pirineos 2026 · Tredòs

Landing estática para consultar el viaje del **12 al 16 de agosto de 2026** desde móvil u ordenador.

## Qué incluye

- Cuenta atrás automática hasta la salida del 12 de agosto a las 07:00.
- Durante el viaje, cambia a **“Día X de 5”** y muestra el plan de esa jornada.
- Itinerario completo, participantes, coches y enlaces compartidos.
- Mapa interactivo con todas las paradas.
- Botón de ubicación en tiempo real, visible únicamente en el dispositivo del usuario.
- Simulador de presupuesto y checklist personal guardados en el navegador.
- Archivo de calendario `.ics`.
- Diseño responsive con temática de montaña.

## Publicarlo en GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `pirineos-2026`.
2. Sube **todos los archivos de esta carpeta** a la raíz de la rama `main`.
3. En el repositorio, abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/(root)`, y guarda.
6. Tras el despliegue, GitHub mostrará la URL pública del sitio.

El archivo `.nojekyll` permite publicar los archivos estáticos directamente.

## Editar datos

La web está concentrada en `index.html` para que sea fácil de mantener.

- Fechas y textos de cada día: busca `data-date="2026-08-12"` y los bloques siguientes.
- Cuenta atrás y texto diario: busca `const tripDays`.
- Participantes y coches: busca la sección `id="grupo"`.
- Puntos del mapa: busca `const places`.
- Valores iniciales del presupuesto: busca `budgetDefaults`.

## Notas de privacidad

- GitHub Pages publica el sitio en Internet. No se ha incluido la dirección exacta de la casa; el marcador usa el centro de Tredòs.
- La geolocalización no se envía a un servidor ni se comparte con el grupo.
- El presupuesto y la checklist se almacenan únicamente en el navegador de cada persona.

## Dependencias

El mapa utiliza Leaflet 1.9.4 y teselas de OpenStreetMap cargadas desde Internet. El resto de la página funciona sin compilación ni backend.
