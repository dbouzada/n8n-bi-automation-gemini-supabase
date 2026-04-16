# 📈 Automated BI Ecosystem: n8n + Gemini + Supabase

Este repositorio contiene la arquitectura completa de un sistema de Business Intelligence automatizado. El flujo integra la extracción de datos desde una base de datos relacional, la consolidación mediante lógica custom en JavaScript y la generación de reportes visuales utilizando IA Generativa.

---

## 🏗️ Arquitectura del Sistema

El proyecto se divide en tres capas principales:

1.  **Capa de Datos (Storage):** Gestión de registros de ventas, vendedores y productos en **Supabase (PostgreSQL)**.
2.  **Capa de Orquestación (n8n):** * **Consolidación:** Un motor en Node.js procesa +4000 registros para agrupar métricas por mes, vendedor y producto.
    * **Transformación:** Limpieza de datos y preparación de estructuras JSON para la IA.
3.  **Capa de Presentación (IA & Viz):** * **Google Gemini:** Analiza las métricas y redacta un reporte ejecutivo en HTML.
    * **QuickChart API:** Renderizado dinámico de 4 tipos de gráficos (Gauge, Pie, Bar, Line).

---

## 🛠️ Cómo Replicar este Proyecto

### Requisitos
- Instancia de **n8n** (Docker o Cloud).
- API Key de **Google Gemini**.
- Cuenta en **Supabase** con las tablas de ventas configuradas.

### Instalación
1. Importa los archivos situados en la carpeta `/workflows` en tu instancia de n8n.
2. Configura las credenciales de Gmail, Supabase y Google Gemini.
3. El workflow está configurado para ejecutarse mediante un **Cron Job** cada lunes a las 08:00 AM.

---

## 📊 Dashboard de Resultados (Email)

A continuación se muestra el reporte final generado automáticamente y enviado por correo electrónico:

![Reporte de Ventas](assets/Reporte%20Mail.png)

---

## 👨‍💻 Autor
**Diego Bouzada** - Data Engineer 
