# Predicción de Ingresos (Adult Income) & Optimizador de Perfil

Este proyecto implementa un sistema de **Machine Learning** capaz de predecir si una persona superará el umbral de ingresos de **50,000 USD anuales**, incorporando además un **motor de recomendación inteligente** que sugiere mejoras en el perfil del usuario para aumentar dicha probabilidad.

---

## 📘 Descripción del Proyecto

El sistema no solo realiza una predicción binaria, sino que incluye un **Optimizador de Perfil** que analiza variables en tiempo real (educación, ocupación, horas trabajadas, etc.) y propone cambios estratégicos para maximizar el éxito financiero.

---

## 🧩 Contexto

El nivel de ingresos de una persona depende de múltiples factores como:

- Nivel educativo  
- Tipo de ocupación  
- Horas trabajadas  
- Contexto socioeconómico  

Utilizando el dataset **Census Income**, este proyecto actúa como una herramienta de **simulación de carrera**, permitiendo visualizar cómo diferentes decisiones afectan la probabilidad de alcanzar mayores ingresos.

---

## 🎯 Objetivos

- **Análisis Exploratorio (EDA)**  
  Identificar patrones entre ingresos y variables clave.

- **Modelo Predictivo**  
  Clasificar perfiles según su probabilidad de superar los 50K.

- **Optimizador de Perfil**  
  Implementar un sistema de recomendaciones basado en simulaciones.

- **Interfaz Interactiva**  
  Desarrollar una aplicación en Streamlit para uso real.

---

## 📊 Características del Dataset

| Columna            | Tipo     | Descripción |
|--------------------|----------|------------|
| Age               | int64    | Edad del individuo |
| Education-num     | int64    | Nivel educativo (1–16) |
| Workclass         | object   | Sector laboral |
| Occupation        | object   | Ocupación |
| Hours-per-week    | int64    | Horas trabajadas |
| Capital Gain/Loss | int64    | Ganancias/pérdidas |
| Marital Status    | object   | Estado civil |
| Native Country    | object   | País de origen |

---

## 🚀 Metodología

### 1. Preprocesamiento y Limpieza

- **Mapeo Educativo**  
  Conversión de educación a valores numéricos mediante `education_mapping.csv`.

- **Ingeniería de Características**  
  Identificación de ocupaciones mejor remuneradas para alimentar el sistema de recomendación.

---

### 2. Entrenamiento y Persistencia

- **Modelo**  
  Modelo de clasificación binaria almacenado en `.sav` (Pickle).

- **Sistema de Recomendación**  
  Simulación de escenarios modificando variables del perfil y evaluando su impacto en la probabilidad.

---

### 🧠 Concepto

En lugar de solo predecir, el sistema responde:

> “¿Qué debería cambiar en este perfil para aumentar la probabilidad de superar los 50K?”

---

---

### 🔍 Ejemplo

- Aumentar educación → mejora la probabilidad  
- Cambiar ocupación → impacto directo medible  
- Aumentar horas → efecto cuantificable  

---

## ⚙️ Tecnologías Utilizadas

- **Python** → Core del proyecto  
- **Streamlit** → Interfaz web  
- **Pandas & NumPy** → Manipulación de datos  
- **Scikit-learn** → Modelo predictivo  
- **Pickle** → Persistencia del modelo  
- **Matplotlib** → Visualización  

---

## 📁 Estructura del Proyecto
project/
│
├── app.py
├── explore.ipynb
├── modelo_recomendacion.sav
├── education_mapping.csv
├── ocupaciones_top.csv
├── requirements.txt


---

## 💻 Instalación

```bash
pip install -r requirements.txt
```

El archivo `explore.ipynb` contiene el proceso de entrenamiento del modelo y generación de archivos auxiliares como:

- modelo_recomendacion.sav

- education_mapping.csv

- ocupaciones_top.json

Por lo que se recomienda abrir el notebook y ejecutar todas las celdas:

Abrir `explore.ipynb`

Ejecutar: Run All

## 💻 Ejecución

```bash
streamlit run src/app.py --server.port 10000 --server.address 0.0.0.0
```

## 👤 Autor

Bryan Jumbo Torres
📍 Mallorca, España
💻 Proyecto de Data Science & Machine Learning