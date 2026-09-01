# Pinax

**Pinax** es una aplicación desktop local-first para organizar el estudio universitario en un único espacio de trabajo. El proyecto busca reducir la fragmentación entre apuntes, documentos, referencias y herramientas de concentración sin depender de una conexión permanente.

> **Estado:** desarrollo activo. Este repositorio funciona como caso de estudio público; el código fuente se mantiene privado durante esta etapa.

## Problema que busca resolver

Estudiar suele implicar alternar entre apuntes, PDFs, gestores bibliográficos y aplicaciones separadas. Pinax reúne esas tareas en una experiencia de escritorio, priorizando la continuidad del trabajo, la privacidad y el control del usuario sobre sus archivos.

## Funcionalidades implementadas

- Lienzo de trabajo con desplazamiento, zoom y entrada manuscrita.
- Pegado y manipulación de texto e imágenes.
- Formas, líneas, flechas, divisores y plano cartesiano.
- Herramientas de borrado e historial para deshacer y rehacer operaciones compatibles.
- Modos Focus y Canvas-only para reducir distracciones.
- Espacio de trabajo local con base SQLite y archivos organizados en el equipo.
- Respaldos en JSON, importación y exportación.
- Integración con Zotero para buscar referencias y abrir adjuntos.
- Empaquetado e instalador para Windows.

## Arquitectura

| Capa | Tecnología | Responsabilidad |
|---|---|---|
| Interfaz | React + TypeScript | Experiencia de usuario, estado y herramientas del lienzo |
| Escritorio | Tauri + Rust | Integración nativa, operaciones de archivos y empaquetado |
| Persistencia | SQLite + sistema de archivos | Metadatos, imágenes, respaldos y exportaciones |
| Bibliografía | API local de Zotero | Búsqueda, paginación, adjuntos y enlaces profundos |

## Decisiones de diseño

- **Local-first:** el contenido principal permanece en el dispositivo del usuario.
- **Persistencia explícita:** la base de datos guarda metadatos y el sistema de archivos conserva los activos.
- **Integración gradual:** Zotero se incorpora sin reemplazar el flujo bibliográfico existente.
- **Separación de responsabilidades:** la interfaz web gestiona la experiencia y Rust concentra las operaciones nativas.

## Calidad y validación

El proyecto cuenta con pruebas automatizadas, verificación de tipos, controles del código Rust, compilación de producción y validación del proceso de empaquetado para Windows.

## Próximos pasos

- Mejorar la experiencia del lienzo y el rendimiento en espacios de trabajo grandes.
- Ampliar cobertura de pruebas e importación/exportación.
- Documentar decisiones técnicas y flujos principales.
- Explorar asistencia con IA sobre contenido seleccionado por el usuario. Esta función pertenece al roadmap y no se presenta como implementada.

## Privacidad

Este repositorio no contiene datos personales, documentos de estudio ni credenciales. Las capturas y demostraciones públicas utilizarán información de ejemplo.
