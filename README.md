# ¿Es el bitcoin el "oro digital"?

**Análisis exploratorio de datos (EDA)** sobre si el bitcoin se comporta como un activo refugio en las crisis financieras, comparado con el oro y con la bolsa (S&P 500), entre 2014 y 2026.

Proyecto del módulo de Data Analysis del Bootcamp de Data Science (Vitoria-Gasteiz).

## Pregunta

¿Se comporta el bitcoin como un verdadero activo refugio, es decir, protege el capital cuando la bolsa cae?

## Hipótesis

- **General:** el bitcoin no es un activo refugio.
- **H1:** en las crisis financieras desde 2014, el bitcoin cayó junto con la bolsa.
- **H2:** el bitcoin se comporta más como la renta variable (S&P 500) que como el oro.
- **H3:** el bitcoin cae cuando la Reserva Federal sube los tipos de interés y sube cuando los baja, igual que la bolsa.

## Datos

| Dato | Fuente | Frecuencia |
|---|---|---|
| Bitcoin (BTC/USD) | [Investing.com](https://es.investing.com/crypto/bitcoin) | Diaria |
| S&P 500 | [Investing.com](https://es.investing.com/indices/us-spx-500) | Diaria |
| Oro (XAU/USD) | [Investing.com](https://es.investing.com/currencies/xau-usd) | Diaria |
| Tipos de interés de la FED (FEDFUNDS) | [FRED](https://fred.stlouisfed.org/series/fedfunds) | Mensual |

Periodo analizado: 02/01/2014 – 10/11/2026, con 9 crisis financieras identificadas (del crash bursátil chino de 2015 al conflicto con Irán de 2026).

## Resultados

| Hipótesis | Dato clave | ¿Se cumple? |
|---|---|---|
| H1 – Crisis | El bitcoin cayó en 7 de 9 crisis; variación media -20,2 % (S&P 500 -14,7 %, oro +0,8 %) | Sí |
| H2 – Comparativa | Correlación diaria con el S&P 500: 0,12 / con el oro: 0,04 | Sí, de forma débil |
| H3 – Tipos de la FED | Cayó en los ciclos de subidas fuertes (2018: -74 %; 2022: -64 %), pero no de forma sistemática | Parcialmente |

**Conclusión:** el bitcoin no es un activo refugio. Se comporta como un activo de riesgo de alta volatilidad, no como el "oro digital".

## Tecnologías

- Python
- Pandas y NumPy (limpieza y análisis)
- Matplotlib y Seaborn (visualización)
- Jupyter Notebook

## Estructura del repositorio

```
├── README.md
├── Es bitcoin oro digital.pptx   # Presentación
└── src/
    ├── data/                     # Ficheros CSV utilizados
    ├── img/                      # Gráficos exportados
    ├── notebooks/                # Notebooks de pruebas (limpieza y análisis)
    ├── utils/                    # Funciones auxiliares
    └── memoria.ipynb             # Memoria del proyecto
```

## Cómo ejecutarlo

1. Instalar las librerías: `pip install pandas numpy matplotlib seaborn`
2. Abrir `src/memoria.ipynb` y ejecutar todas las celdas.

## Autor

**Joaquín Flores Serradilla**
