# 🎬 TikTok Claims EDA — Análisis Exploratorio para Clasificación de Contenido

> Análisis exploratorio de datos sobre **19,382 videos de TikTok** como base para un modelo de clasificación *claim vs. opinion*. Trabajo realizado bajo el framework **PACE** (Plan, Analyze, Construct, Execute).

---

## 📌 Contexto del proyecto

Como parte del **Google Advanced Data Analytics Certificate** (Course 2 - Get Started with Python), trabajé como analista de datos en un escenario simulado para TikTok. El equipo de liderazgo aprobó la propuesta para construir un modelo de clasificación de claims, y este notebook entrega el primer EDA estructurado que sirve como base para el modelado posterior.

## 🎯 Objetivos

- Entender la estructura del dataset (12 columnas, 19,382 registros)
- Identificar valores nulos, outliers y problemas de calidad
- Comparar engagement entre videos `claim` vs `opinion`
- Investigar la relación entre `author_ban_status` y métricas de engagement
- Calcular tasas de engagement (likes/view, shares/view, comments/view)

## 🔑 Insights clave

| Hallazgo | Dato |
|---|---|
| Distribución claim vs opinion | ~49.6% claims · ~48.9% opinions · ~1.5% sin clasificar |
| Promedio de vistas — claim vs opinion | **501,029** vs 4,956 (≈100x más) |
| Mediana de shares — banned vs active | **14,468** vs 437 (33x más) |
| Likes/view promedio — claim vs opinion | 0.33 vs 0.22 |

**Conclusión:** Los videos tipo *claim* son significativamente más virales y generan mayor engagement por vista que las opiniones. Los autores con cuentas baneadas o en revisión presentan métricas desproporcionadamente altas — un patrón crítico para estrategia de moderación de contenido.

## 🧠 Metodología (PACE)

- **Plan:** Revisión del data dictionary y categorización de variables (atributos de contenido, autor, métricas de engagement)
- **Analyze:** `head()`, `info()`, `describe()`, detección de nulos y outliers
- **Construct:** Creación de columnas derivadas (`likes_per_view`, `shares_per_view`, `comments_per_view`)
- **Execute:** Síntesis ejecutiva con respuestas a las preguntas planteadas por el equipo de TikTok

## 🛠️ Stack

- Python 3 · pandas · numpy
- Jupyter Notebook
- Framework PACE para estructura del análisis

## 📂 Archivos

- `tiktok_eda.ipynb` — Notebook completo con código y comentarios
- `Tiktok_Project.pdf` — Versión PDF del notebook para visualización rápida sin ejecutar

## 🚀 Cómo ejecutar

\`\`\`bash
pip install pandas numpy jupyter
jupyter notebook tiktok_eda.ipynb
\`\`\`

---

*Proyecto del Google Advanced Data Analytics Certificate · César Rábago Pérez · 2025*
