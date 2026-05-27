# Predicting-Fund-Prices-Prophet-LSTM-GARCH
Predicción de series temporales del valor de cuotas de fondos de inversión mediante un análisis comparativo con Prophet, LSTM y GARCH.

markdown# Predicting-Fund-Prices-Prophet-LSTM-GARCH

**Autora:** Joanice Moreira Bastos  
**Proyecto:** Proyecto Integrador Final (Módulo 5): Valor de la Cuota del Fondo de Inversión

---

## 📈 Explicación del Negocio
Un fondo de inversión es un fondo común administrado por profesionales que invierten el dinero de los inversionistas en diferentes opciones como acciones, bonos o plazos fijos dependiendo del perfil. Cada inversionista es dueño de una parte del fondo y esa parte se mide en cuotas calculadas al cierre de cada día hábil.

Este proyecto tiene como objetivo analizar y predecir el comportamiento de las series temporales del valor de las cuotas utilizando tres enfoques avanzados: **Prophet**, redes neuronales **LSTM** y modelos de volatilidad **GARCH**.

---

## 📋 Estructura de la Base de Datos
El script procesa un archivo llamado `Valor_Cuota.csv` (separado por punto y coma `;` y con codificación `latin1`). Contiene las siguientes columnas:

*   **Fecha**: Fecha del registro (formato `DD/MM/AAAA`).
*   **Valor_Cuota_ATU**: Cartera Actuarial (concentra el 56% de los activos).
*   **Valor_Cuota_CON**: Cartera Conservadora.
*   **Valor_Cuota_MOD**: Cartera Moderada.
*   **Valor_Cuota_AGR**: Cartera Agresiva.

> ⚠️ **Nota de seguridad:** Por motivos de privacidad, la base de datos real no se encuentra en este repositorio público. Se ha proporcionado un archivo ficticio con la misma estructura (`dados_exemplo.csv` o `Valor_Cuota.csv` con datos de prueba) para verificar la ejecución del código.

---

## 🛠️ Tecnologias y Librerías Utilizadas
El proyecto está desarrollado en **Python 3.12** e incluye el uso de:

*   **Procesamiento de datos**: `pandas`, `numpy`
*   **Visualización**: `matplotlib`, `seaborn`
*   **Análisis de Series Temporales**: `statsmodels` (análisis de estacionalidad, test Dickey-Fuller, ACF)
*   **Modelos de Predicción**:
    *   `prophet` (Predicción de series temporales de Meta)
    *   `tensorflow` / `keras` (Redes neuronales de memoria a largo y corto plazo - LSTM)
    *   `arch` (Modelado de efectos GARCH para volatilidad financiera)
*   **Métricas de evaluación**: `scikit-learn` (MAE, MSE)

---

## 🚀 Cómo Ejecutar el Proyecto

### 1. Clonar el repositorio e instalar dependencias
Asegúrate de instalar las librerías necesarias ejecutando en tu terminal:
```bash
pip install numpy pandas matplotlib seaborn statsmodels scikit-learn prophet tensorflow arch
```

### 2. Ajuste del código (Si no usas Google Colab)
El script original está diseñado para ejecutarse en Google Colab conectando Google Drive. Si deseas ejecutarlo de forma local en tu computadora con el archivo ficticio, reemplaza las líneas de la sección **1.2** por una ruta local directa:

```python
# En lugar de usar google.colab, lee el archivo directamente:
url_csv = 'Valor_Cuota.csv'  # Asegúrate de que el CSV esté en la misma carpeta que el script
data_original = pd.read_csv(url_csv, encoding='latin1', sep=';')
