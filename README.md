# Megaline-Cual-es-la-mejor-tarifa-

# 📱 ¿Cuál es la mejor tarifa?
## Análisis de ingresos en planes móviles de Megaline

Este proyecto analiza el comportamiento de los clientes de Megaline, un operador de telecomunicaciones, con el fin de determinar qué tarifa de prepago —**Surf** o **Ultimate**— genera más ingresos. A través de datos reales de llamadas, mensajes e internet de 500 clientes, se aplicaron técnicas de análisis exploratorio y estadístico para responder esta pregunta.

---

## 📁 Dataset utilizado

El conjunto de datos se compone de varias tablas con información sobre:

1. **Usuarios (`users.csv`)**  
   - `user_id`: ID único del cliente  
   - `age`, `city`, `churn_date`, `reg_date`, `tariff`

2. **Llamadas (`calls.csv`)**  
   - `user_id`, `call_date`, `duration` (en minutos)

3. **Mensajes (`messages.csv`)**  
   - `user_id`, `message_date`

4. **Internet (`internet.csv`)**  
   - `user_id`, `session_date`, `mb_used`

5. **Planes tarifarios (`tariffs.csv`)**  
   - `tariff_name`, `rub_monthly_fee`, `minutes_included`, `messages_included`, `mb_per_month_included`, `rub_per_minute`, `rub_per_message`, `rub_per_gb`

---

## 🛠 Tecnologías utilizadas

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Pandas](https://img.shields.io/badge/Pandas-Used-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Used-blueviolet)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Used-orange)
![NumPy](https://img.shields.io/badge/NumPy-Used-lightgrey)
![SciPy](https://img.shields.io/badge/SciPy-TTest-lightblue)

---

## 🔍 Metodología

### 1. Preparación de datos
- Conversión de fechas a `datetime`.
- Creación de nuevas columnas: mes de uso, total mensual por usuario, GB usados.
- Cálculo del total de ingresos mensuales por usuario y por tipo de tarifa.

### 2. Análisis exploratorio
- Visualización de llamadas, mensajes e internet por cliente y tarifa.
- Distribución de edad y ciudades de los usuarios.

### 3. Análisis estadístico
- Cálculo de promedios, desviación estándar y dispersión para ingresos.
- Prueba de hipótesis con `scipy.stats.ttest_ind` para comparar ingresos entre planes.

---

## 📊 Resultados clave

- El plan **Ultimate**, aunque más caro, tiene menos sobrecostos por uso.
- El plan **Surf** muestra más variabilidad en ingresos por los cargos extra (minutos, GB, SMS).
- Se rechazó la hipótesis nula: los ingresos **no** son iguales entre ambos planes. Ultimate es estadísticamente más rentable.
- La diferencia en ingresos **no** depende significativamente de la ciudad o edad del usuario.

---

## 🎯 Aprendizajes

- Aplicación de limpieza multitabla y uso de joins condicionales.
- Creación de funciones personalizadas para calcular ingresos por cliente.
- Implementación de pruebas estadísticas (t-test) para comparación de grupos.
- Análisis interpretativo con visualizaciones (boxplots, histogramas, medias móviles).

---

## 🚀 Cómo ejecutar este proyecto

1. Clona este repositorio:
git clone https://github.com/tu-usuario/analisis-tarifas-megaline.git
cd analisis-tarifas-megaline

2. Instala las dependencias:
pip install pandas matplotlib seaborn scipy numpy

3. Abre el notebook:
jupyter notebook tarifa_megaline.ipynb

---

## 📬 Conecta conmigo
¿Te interesa el análisis de productos o tarifas en empresas tech o telecomunicaciones? Con gusto puedes escribirme por [LinkedIn](https://www.linkedin.com/in/bruno-ramos-huerta/) o explorar mis otros proyectos en GitHub.
