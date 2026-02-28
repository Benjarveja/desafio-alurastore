# 📊 Alura Store LATAM — Análisis de desempeño comercial

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-5A9)](https://seaborn.pydata.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success)](#)

Proyecto de análisis exploratorio de datos (EDA) sobre el rendimiento de 4 tiendas de **Alura Store LATAM**, desarrollado en el notebook [`AluraStoreLatam.ipynb`](./AluraStoreLatam.ipynb).

---

## Tabla de contenidos

- [1. Contexto del negocio](#-1-contexto-del-negocio)
- [2. Objetivo](#-2-objetivo)
- [3. Dataset](#-3-dataset)
- [4. Metodología](#-4-metodología)
- [5. KPIs analizados](#-5-kpis-analizados)
- [6. Resultados principales](#-6-resultados-principales)
- [7. Conclusiones y recomendaciones](#-7-conclusiones-y-recomendaciones)
- [8. Stack tecnológico](#-8-stack-tecnológico)
- [9. Reproducibilidad](#-9-reproducibilidad)
- [10. Autor](#-10-autor)

---

## 1. Contexto del negocio

El Sr. Juan debe decidir qué tienda de su cadena Alura Store debe vender para iniciar un nuevo emprendimiento. Para ello, se analizarán datos de ventas, rendimiento y reseñas de las 4 tiendas de Alura Store. El objetivo es identificar la tienda menos eficiente y presentar una recomendación final basada en los datos.

---

## 2. Objetivo

Evaluar el desempeño de las 4 tiendas usando métricas clave para responder:

- ¿Qué tienda factura menos?
- ¿Cómo se distribuyen las ventas por categoría?
- ¿Cuál tiene mejor/peor percepción del cliente?
- ¿Qué productos lideran y cuáles no rotan?
- ¿Cómo se comporta el costo de envío por tienda?

---

## 3. Dataset

Se utilizaron 4 archivos CSV (uno por tienda), con variables de venta y operación:

- `tienda_1.csv`
- `tienda_2.csv`
- `tienda_3.csv`
- `tienda_4.csv`

**Campos relevantes**:
`producto`, `categoría`, `precio`, `costo_envío`, `fecha_compra`, `vendedor`, `calificación`, `método_pago`, `cuotas`, `latitud`, `longitud`.

---

## 4. Metodología

1. **Carga y consolidación** de fuentes por tienda.
2. **Limpieza y validación básica** de tipos y consistencia.
3. **Cálculo de KPIs** comerciales, satisfacción y logística.
4. **Visualización** para comparación entre tiendas.
5. **Interpretación de hallazgos** con enfoque en decisión de negocio.

---

## 5. KPIs analizados

- **Facturación total por tienda**
- **Ingresos por categoría**
- **Calificación promedio de clientes**
- **Producto más vendido y menos vendido por tienda**
- **Costo promedio de envío por tienda**

---

## 6. Resultados principales

### 6.1 Facturación total por tienda

| Tienda | Facturación |
|---|---:|
| Tienda 1 | 1,150,880,400 |
| Tienda 2 | 1,116,343,500 |
| Tienda 3 | 1,098,019,600 |
| Tienda 4 | 1,038,375,700 |

**Insight:** La **Tienda 4** presenta la menor facturación del conjunto.

---

### 6.2 Calificación promedio por tienda

| Tienda | Calificación promedio |
|---|---:|
| Tienda 1 | 3.98 |
| Tienda 2 | 4.04 |
| Tienda 3 | 4.05 |
| Tienda 4 | 4.00 |

**Insight:** La **Tienda 3** lidera en satisfacción. La **Tienda 1** es la más baja.

---

### 6.3 Producto más y menos vendido por tienda

| Tienda | Más vendido | Menos vendido |
|---|---|---|
| Tienda 1 | Microondas | Auriculares con micrófono |
| Tienda 2 | Iniciando en programación | Juego de mesa |
| Tienda 3 | Kit de bancas | Bloques de construcción |
| Tienda 4 | Cama box | Guitarra eléctrica |

**Insight:** Existen patrones de rotación distintos por tienda; conviene ajustar surtido por demanda local.

---

### 6.4 Costo de envío promedio por tienda

| Tienda | Costo promedio de envío |
|---|---:|
| Tienda 1 | 26,018.61 |
| Tienda 2 | 25,216.24 |
| Tienda 3 | 24,805.68 |
| Tienda 4 | 23,459.46 |

**Insight:** La **Tienda 4** es la más eficiente en costo logístico promedio.

---

### 6.5 Ventas por categoría

El análisis comparativo por categorías muestra mayor contribución en líneas como:

- Electrónicos
- Electrodomésticos
- Muebles

**Insight:** Estas categorías concentran gran parte de los ingresos y son prioritarias para estrategias comerciales.

---

## 7. Conclusiones y recomendaciones

### Conclusiones
- Bajo un enfoque de portafolio (desinvertir en 1 de 4 tiendas), la **Tienda 4** es la principal candidata a venta, ya que presenta la **menor facturación total** del grupo.
- Aunque la **Tienda 4** tiene el **menor costo de envío promedio** (buena eficiencia logística), esta ventaja no compensa su menor generación de ingresos frente a las demás tiendas.
- La **Tienda 3** muestra el mejor equilibrio competitivo (mayor calificación promedio y facturación superior a Tienda 4), por lo que no sería prioritaria para desinversión.
- La **Tienda 1** requiere mejoras en experiencia de cliente (calificación más baja), pero su nivel de facturación reduce la prioridad de venderla en el corto plazo.

### Recomendación de decisión (venta de tienda)
1. **Vender la Tienda 4** por menor aporte relativo a ingresos dentro de la red.
2. Antes de ejecutar la venta, validar el impacto contractual y operativo de la logística actual para no transferir sobrecostos al resto de tiendas.
3. Reasignar parte del capital liberado a iniciativas de crecimiento en **Tienda 2 y Tienda 3** (categorías de mayor contribución), ademas de su utilizacion para la idea de emprendimiento mencionada por el Sr. Juan.
4. Implementar en **Tienda 1** un plan de mejora de satisfacción para proteger ingresos y reputación.

---

## 8. Stack tecnológico

- **Python 3**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook / Google Colab**

---

## 9. Reproducibilidad

### Clonar repositorio
```bash
git clone https://github.com/Benjarveja/desafio-alurastore.git
cd desafio-alurastore

Benjarveja
Proyecto desarrollado para el desafío de Data Science - Alura LATAM.
