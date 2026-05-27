# Predicting-Fund-Prices-Prophet-LSTM-GARCH
Predicción de series temporales del valor de cuotas de fondos de inversión mediante un análisis comparativo con Prophet, LSTM y GARCH.

markdown# Predicting-Fund-Prices-Prophet-LSTM-GARCH

**Autora / Author:** Joanice Moreira Bastos  
**Proyecto / Project:** Proyecto Integrador Final (Módulo 5): Valor de la Cuota del Fondo de Inversión

---

## 🌐 Idioma / Language
*   [Leer en Español (Original)](#-español)
*   [Read in English](#-english)

---

## 🇪🇸 Español

### 📈 Explicación del Negocio
Un fondo de inversión es un fondo común administrado por profesionales que invierten el dinero de los inversionistas en diferentes opciones como acciones, bonos o plazos fijos dependiendo del perfil. Cada inversionista es dueño de una parte del fondo y esa parte se mide en cuotas calculadas al cierre de cada día hábil.

Este proyecto tiene como objetivo analizar y predecir el comportamiento de las series temporales del valor de las cuotas utilizando tres enfoques avanzados: **Prophet**, redes neuronales **LSTM** y modelos de volatilidad **GARCH**.

### 📋 Estructura de la Base de Datos
El script procesa un archivo llamado `Valor_Cuota.csv` (separado por punto y coma `;` y con codificación `latin1`). Contiene las siguientes columnas:
*   **Fecha**: Fecha del registro (formato `DD/MM/AAAA`).
*   **Valor_Cuota_ATU**: Cartera Actuarial (concentra el 56% de los activos).
*   **Valor_Cuota_CON**: Cartera Conservadora.
*   **Valor_Cuota_MOD**: Cartera Moderada.
*   **Valor_Cuota_AGR**: Cartera Agresiva.

> ⚠️ **Nota de seguridad:** Por motivos de privacidad, la base de datos real no se encuentra en este repositorio público. Se ha proporcionado un archivo ficticio con la misma estructura (`Valor_Cuota.csv` con datos de prueba) para verificar la ejecución del código.

### 🛠️ Tecnologías y Librerías Utilizadas
El proyecto está desarrollado en **Python 3.12** e incluye el uso de:
*   **Procesamiento de datos**: `pandas`, `numpy`
*   **Visualización**: `matplotlib`, `seaborn`
*   **Análisis de Series Temporales**: `statsmodels` (análisis de estacionalidad, test Dickey-Fuller, ACF)
*   **Modelos de Predicción**: `prophet`, `tensorflow` (LSTM), `arch` (GARCH)
*   **Métricas de evaluación**: `scikit-learn` (MAE, MSE)

### 🚀 Cómo Ejecutar el Proyecto
Asegúrate de instalar las librerías necesarias ejecutando en tu terminal:
```bash
pip install numpy pandas matplotlib seaborn statsmodels scikit-learn prophet tensorflow arch
```
El script detectará automáticamente si estás en Google Colab o en un entorno local para cargar el archivo `Valor_Cuota.csv`.

---

## 🇬🇧 English

### 📈 Business Background
An investment fund is a mutual fund managed by professionals who invest investors' money in different financial instruments (stocks, bonds, or fixed-term deposits) depending on the risk profile. Each investor owns a share of the fund, which is measured in quotas calculated at the close of each business day.

This project aims to analyze and predict the behavior of investment fund quota price time series using three advanced approaches: **Prophet**, **LSTM** neural networks, and **GARCH** volatility models.

### 📋 Dataset Structure
The script processes a file named `Valor_Cuota.csv` (semicolon-separated `;` with `latin1` encoding). It contains the following columns:
*   **Fecha**: Documented date (format `DD/MM/YYYY`).
*   **Valor_Cuota_ATU**: Actuarial Portfolio (holds 56% of total assets).
*   **Valor_Cuota_CON**: Conservative Portfolio.
*   **Valor_Cuota_MOD**: Moderate Portfolio.
*   **Valor_Cuota_AGR**: Aggressive Portfolio.

> ⚠️ **Security Note:** For privacy reasons, the actual database is not included in this public repository. A dummy file with the exact same structure (`Valor_Cuota.csv` containing test data) has been provided to verify code execution.

### 🛠️ Technologies and Libraries Used
The project is built with **Python 3.12** and utilizes:
*   **Data Processing**: `pandas`, `numpy`
*   **Visualization**: `matplotlib`, `seaborn`
*   **Time Series Analysis**: `statsmodels` (seasonality analysis, Dickey-Fuller test, ACF plots)
*   **Predictive Models**: `prophet`, `tensorflow` (LSTM), `arch` (GARCH)
*   **Evaluation Metrics**: `scikit-learn` (MAE, MSE)

### 🚀 How to Run the Project
Make sure to install the required libraries by running the following command in your terminal:
```bash
pip install numpy pandas matplotlib seaborn statsmodels scikit-learn prophet tensorflow arch
```
The script will automatically detect whether you are running it on Google Colab or in a local environment to fetch the `Valor_Cuota.csv` file properly.
