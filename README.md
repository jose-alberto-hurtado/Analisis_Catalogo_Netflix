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
