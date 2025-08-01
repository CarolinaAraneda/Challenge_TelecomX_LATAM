# Challenge_TelecomX_LATAM

# Análisis de Fuga de Clientes – TelecomX

Este proyecto tiene como objetivo identificar patrones de abandono de clientes en TelecomX, analizar las causas potenciales y ofrecer recomendaciones estratégicas que ayuden a mejorar la retención. A través de limpieza, visualización y análisis de datos, se exploran variables relevantes como servicios contratados, métodos de pago y costos mensuales.

---

## Estructura del Proyecto

- `TelecomX_Data_estandarizado.csv` – Datos limpios y transformados.
- `TelecomX_LATAM.ipynb` – Código en Python desarrollado en Google Colab.
- `README.md` – Descripción del proyecto (este archivo).

---

## Tecnologías Utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Google Colab
- Paleta de colores: Viridis

---

## Limpieza y Preparación de Datos

1. **Importación:**
   - Dataset cargado desde un archivo `.json` público en GitHub.
   - Columnas anidadas (`customer`, `phone`, `internet`, `account`) fueron normalizadas y unidas en un único DataFrame.

2. **Limpieza:**
   - Eliminación de registros con `Churn` vacío (224 registros, 3%).
   - Reemplazo de valores nulos por `0`.

3. **Estandarización:**
   - Conversión de valores textuales "Yes/No" a binarios `1/0`.
   - Traducción y renombre de columnas.
   - Normalización de valores para gráficos y análisis.

4. **Transformaciones:**
   - Creación de columna `cuentas_diarias` = `Charges.Monthly / 30`.
   - Creación de columna `cantidad_servicios`.
   - Clasificación de internet real (`DSL` o `Fiber optic`) en `tiene_internet_real`.

---

## Análisis Realizado

### Métricas Descriptivas

- Media, mediana, desviación estándar de cargos mensuales y totales.
- Distribución del tiempo de permanencia.

### Visualizaciones Generadas

Cada gráfico fue generado como una función reutilizable:

1. `grafico_abandono_pie_chart` – Porcentaje de abandono.
2. `grafico_hist_abandono_tiempo` – Histograma de abandono por tiempo.
3. `grafico_linea_abandono_tiempo` – Línea de abandono por tiempo.
4. `grafico_abandono_por_genero`
5. `grafico_abandono_genero_edad`
6. `grafico_abandono_genero_pareja`
7. `grafico_comparativo_abandono_metodo_pago`
8. `grafico_comparativo_servicios`
9. `grafico_box_costo_vs_abandono`
10. `grafico_distribucion_costo_vs_abandono.`
11. `grafico_kde_costo_mensual_abandono`
12. `grafico_kde_cuentas_diarias_vs_abandono`

---

## Conclusiones Principales

- **Mayor abandono en el primer mes:** 20% de los clientes abandonan al mes 1.
- **Costo elevado:** Clientes que abandonan tienden a pagar más mensualmente.
- **Sin pareja → mayor abandono:** Clientes sin pareja muestran tasas más altas de fuga.
- **Método de pago importa:** Cheques electrónicos concentran la mayoría de los abandonos.
- **Adultos mayores abandonan menos:** Mayor fidelidad en personas ≥ 65 años.
- **Clientes con más servicios abandonan más:** Posible relación con costos percibidos.

---

## Recomendaciones Estratégicas

- **Refuerzo del onboarding:** Programas de bienvenida y soporte el primer mes.
- **Campañas de fidelización:** Enfocadas en personas sin pareja.
- **Revisión de precios o beneficios para multi-servicios.**
- **Fomento de métodos de pago automáticos.**
- **Análisis de satisfacción en servicios de internet y telefonía.**

---

## Contacto

Desarrollado por: **Carolina Araneda**
Proyecto: **TelecomX**
Fecha: `2025`

---

