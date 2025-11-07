# 🎬 Análisis del Catálogo de Netflix  

📊 **Proyecto de Ciencia de Datos – José Alberto Hurtado Echeverría**  
Análisis exploratorio del catálogo global de Netflix utilizando **Python (pandas, matplotlib y seaborn)** para identificar tendencias, patrones y oportunidades de mejora en la plataforma.  

---

## 🧠 Objetivo  
Explorar las películas y series disponibles en Netflix para responder preguntas como:
- ¿Qué tipo de contenido domina: películas o series?  
- ¿Cuáles son los países con más producciones?  
- ¿Qué clasificaciones por edad son más comunes?  
- ¿Qué géneros son los más populares?  
- ¿Cómo ha evolucionado la cantidad de estrenos por año?  

---

## 📂 Dataset  
- **Archivo:** `netflix_titles.csv`  
- **Fuente:** [Kaggle – Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
- **Dimensiones:** 8,807 filas × 12 columnas  
- **Columnas principales:**  
  `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`.  

---

## 🧹 1. Limpieza de Datos  
- Estandarización de nombres de columnas.  
- Conversión de fechas a formato datetime.  
- Revisión de valores nulos y duplicados.  

**Conclusión:**  
El dataset se encuentra limpio y listo para análisis. Los valores nulos se concentran en `director`, `cast` y `country`, lo cual no afecta los análisis principales.

---

## 🎬 2. Tipo de Contenido  
**Código clave:**
```python
df['type'].value_counts()
Resultados:

Películas: 6,131

Series: 2,676

Conclusión:
El catálogo de Netflix está compuesto en un 70% por películas, confirmando una mayor inversión en contenido cinematográfico.

📈 3. Años de Lanzamiento
Código clave:

python
Copiar código
df['release_year'].value_counts().sort_index().plot(kind='bar')
Conclusión:
El número de estrenos creció rápidamente a partir de 2015, con un pico en 2019, antes de una ligera caída en 2020.

🔢 4. Clasificaciones por Edad
Código clave:

python
Copiar código
df['rating'].value_counts().head(10)
Resultados destacados:

TV-MA (adultos): 3,200 títulos

TV-14 (adolescentes): 2,160 títulos

Conclusión:
El contenido está principalmente orientado a públicos adultos y jóvenes, reflejando una estrategia de audiencia madura.

🌍 5. Países con Más Producciones
Top 5:

Estados Unidos 🇺🇸

India 🇮🇳

Reino Unido 🇬🇧

Canadá 🇨🇦

Francia 🇫🇷

Conclusión:
EE.UU. domina el catálogo, pero la participación de India y Reino Unido muestra la expansión global de Netflix.

🎭 6. Géneros Populares
Top 5 géneros:

International Movies

Dramas

Comedies

International TV Shows

Documentaries

Conclusión:
Netflix apuesta fuertemente por dramas, comedias y contenido internacional, lo que refuerza su estrategia global.

💡 Conclusiones Generales
Netflix mantiene una estructura de catálogo dominada por películas.

Estados Unidos concentra la mayor producción, seguido de India.

Los estrenos aumentaron entre 2016 y 2019, con tendencia a estabilizarse.

El público objetivo principal son jóvenes adultos y adultos.

Los géneros más frecuentes confirman el enfoque internacional y diverso de la plataforma.

🚀 Recomendaciones
Incrementar la representación de producciones latinoamericanas.

Aumentar contenido infantil y familiar para diversificar audiencia.

Analizar el descenso de estrenos tras 2019 para optimizar la estrategia de producción.

Aplicar análisis de segmentación para personalizar marketing según país y tipo de contenido.

🧰 Tecnologías Utilizadas
Lenguaje: Python

Librerías: pandas, numpy, matplotlib, seaborn

Entorno: Google Colab

Visualizaciones: Gráficos de barras y distribuciones

📅 Proyecto completado: Noviembre 2025
👤 Autor: José Alberto Hurtado Echeverría
🔗 LinkedIn: linkedin.com/in/josealbertohurtadoecheverria
