---
trigger: always_on
---

---
name: generar-landing
description: Crea una landing page B2B/B2C de alta conversión en un solo archivo index.html. Úsalo cuando se te pida diseñar, programar o maquetar una nueva página web, landing page o embudo de ventas.
---

# Generación de Landing Page de Alta Conversión

Sigue estos pasos secuencialmente cuando el usuario te pida crear una landing page.

## Paso 1: Fase de Consulta (Auditoría de Negocio)
Antes de escribir cualquier código, preséntate como Arquitecto de Alta Conversión y haz estas 3 preguntas (espera la respuesta del usuario para continuar):
1. **Nicho y Oferta:** ¿Cuál es el negocio y cómo se estructura la oferta? (¿Hay un producto único, una "Escalera de Valor" o distintos planes de precios?).
2. **Estilo de Navegación y UX:** ¿Prefieres un scroll vertical clásico (estilo SaaS), un formato de presentación por secciones (tipo App), o una página de captura corta y directa?
3. **Identidad Visual:** ¿Tienes una paleta de colores o referencias en mente? (Para aplicar la regla 60-30-10 para fondos, contrastes y llamadas a la acción).

## Paso 2: Construcción de la Arquitectura `GLOBAL_CONFIG`
Una vez obtenidas las respuestas, estructura un objeto `GLOBAL_CONFIG` en JS que controle absolutamente todo el sistema de diseño. Debe incluir:
- **Tipografía Modular:** Configuración de Google Fonts y un sub-objeto de `tamanos` con clases de Tailwind.
- **Colores Granulares:** Variables súper específicas (fondos, textos, botones, tarjetas).
- **Contenido Estructurado:** Textos simples, enlaces y Arrays de Objetos para componentes repetitivos (ej. Planes de pago).
- **Media y Enlaces:** Rutas de imágenes, videos y generadores de enlaces (ej. WhatsApp con mensaje predefinido).

## Paso 3: Desarrollo del Esqueleto HTML y JS Blindado
Construye el HTML utilizando Tailwind CSS (CDN). 
- Aplica las reglas de Layout y Diseño B2B/SaaS (asimetría, flexbox, mobile-first). ADVERTENCIA ESTRUCTURAL: Al diseñar en mobile-first (flex-col), usa espaciados tipo gap y alineación justify-center o justify-start. Evita absolutamente usar justify-between si tu contenedor es de alto completo (h-full / h-screen) para que los elementos no queden separados al extremo superior e inferior de la pantalla.
- Implementa la lógica JS utilizando las funciones *Fail-safe* requeridas en las reglas globales.
- Asegúrate de incluir la lógica para inicializar las Pestañas (Tabs) y los Modales para elementos multimedia.

## Paso 4: Entrega y Recomendaciones Finales
- Entrega el código completo en un solo bloque de código HTML listo para producción.
- Finaliza ofreciendo breves consejos de arquitectura de hosting (ej. GitHub Pages, Vercel) y cómo gestionar sus dominios corporativos según el contexto del cliente.