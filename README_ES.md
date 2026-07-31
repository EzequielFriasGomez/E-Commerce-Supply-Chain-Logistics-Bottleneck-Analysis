<p align="center">
  <img src="https://github.com/EzequielFriasGomez/E-Commerce-Supply-Chain-Logistics-Bottleneck-Analysis/blob/main/An%C3%A1lisis_Log%C3%ADstica_Transporte.jpg" width="800"/>
</p>

# Arquitectura y Proceso (ETL & BI)

### PostgreSQL (SQL)

Construcción de un script de ingeniería de datos para extraer, limpiar y normalizar las fechas de la base de datos, aislando métricas exactas del primer semestre (H1) de 2017 y 2018 para garantizar una comparación simétrica. Se calcularon los porcentajes de demora y los tiempos de entrega directamente en el motor SQL para optimizar el rendimiento del modelo.

### Microsoft Power BI

Ingesta del modelo de datos limpio para calcular dinámicamente métricas financieras (inversión en fletes) mediante expresiones DAX. Se diseñaron matrices de calor interactivas y se aplicaron filtros de volumen (mínimo de 300 órdenes) para aislar anomalías logísticas y eliminar el ruido estadístico de las rutas de baja demanda.

# Diagnóstico Comercial (Lo que muestran los datos)

El análisis del dashboard expuso vulnerabilidades críticas en la cadena de suministro durante la expansión.

### El Colapso de la Escala vs. Infraestructura

El volumen de órdenes creció masivamente de **20 mil** a **53 mil** transacciones. Sin embargo, la infraestructura logística no estaba preparada para soportar esta expansión en un período tan corto. Como consecuencia, la tasa de demora a nivel nacional se duplicó, pasando del **4,32%** al **8,75%**.

### La Fuga de Capital en Transporte

El gasto en fletes experimentó un crecimiento exponencial, pasando de **$388 mil** a **$1.073 mil**. A pesar de que la inversión casi se triplicó, el porcentaje de entregas tardías también se duplicó. Esto evidencia que el dinero destinado al transporte fue absorbido por un servicio deficiente, arrastrando además el *Review Promedio* de los clientes hasta **3,99**.

### El Cuello de Botella del Hub Principal

Aplicando un filtro estadístico de **300 órdenes mínimas** para descartar rutas fantasma, los datos revelan que las **seis rutas de alto volumen con mayor deterioro** nacen exclusivamente en **San Pablo (SP)**. La ruta **SP → MA**, por ejemplo, colapsó pasando de un **2,6%** a un **21,2%** de demora.

### El Agujero Negro del Norte (Bahía)

El análisis demuestra que el problema trasciende el volumen de ventas y radica en fallas puramente operativas. Destinos como **Bahía (BA)** presentan un colapso sistémico: sin importar de dónde provenga el paquete (**PR, MG, RJ o SP**), los tiempos de entrega sufrieron demoras superiores al **15%** durante 2018.

# La Jugada Estratégica

### Auditoría de Proveedores y Última Milla

Ejecutar una investigación inmediata sobre las flotas de transportistas que operan las salidas del centro de distribución de **San Pablo (SP)** y la logística de entrega local en **Bahía (BA), Río de Janeiro (RJ) y Paraná (PR)**. Al comprobar que el problema es operativo y no de volumen, se deben revisar las causas de los retrasos operativos.

### Renegociación y Diversificación de Contratos

Congelar la asignación exclusiva de rutas a los transportistas actuales en los ejes **SP, RJ y RS**. Iniciar un proceso de licitación para buscar y contratar nuevos socios logísticos en estas regiones, exigiendo **Acuerdos de Nivel de Servicio (SLA)** más estrictos para frenar el desperdicio de capital en fletes ineficientes.

---

**Tech Stack:** PostgreSQL (SQL) | Microsoft Power BI (DAX)
