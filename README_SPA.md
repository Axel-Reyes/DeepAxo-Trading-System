# DeepAxo - Algorithmic Trading Terminal

**DeepAxo** es una plataforma de escritorio de grado de producción diseñada para el análisis financiero automatizado y la ejecución de operaciones algorítmicas. 

*(Nota: Este repositorio funciona como un showcase técnico de arquitectura y control de calidad. El código fuente de los agentes, modelos predictivos y la lógica de gestión de riesgo se mantiene en un repositorio privado por razones de propiedad intelectual).*

## Arquitectura del Sistema

El software fue desarrollado bajo una arquitectura modular, separando estrictamente la capa visual del motor de procesamiento de datos:
* **Frontend:** Construido con PySide6 (Qt for Python). Interfaz premium con diseño responsivo, animaciones mecánicas y renderizado de gráficos financieros interactivos con Matplotlib.
* **Motor de Análisis:** Sistema multi-agente en Python que automatiza rastreos del mercado y predice tendencias utilizando modelos de Machine Learning (`RandomForestClassifier`).
* **Persistencia y Conectividad:** Base de datos PostgreSQL normalizada para registro transaccional en tiempo real y ejecución de órdenes vía la API de Alpaca.

## Estrategia de Calidad (QA) y Testing

Como profesional orientado a **Quality Assurance** y prácticas **ISTQB**, la plataforma fue construida priorizando la estabilidad, la auditabilidad y la prevención de defectos:

* **Pruebas Funcionales Automatizadas:** Implementación de una suite estructural con `PyTest` y `unittest.mock` para aislar y validar determinísticamente:
  * El cálculo exacto de indicadores técnicos (RSI, SMA) filtrando falsos positivos.
  * La lógica estricta del agente de riesgo (bloqueo de operaciones que superen los límites de apalancamiento).
  * El manejo seguro de estructuras de datos vacías ante caídas simuladas.
* **Tolerancia a Fallos (Resiliencia):** El dashboard cuenta con escudos visuales y lógicos que detectan latencia en las APIs o caídas de red, realizando una degradación elegante sin romper la ejecución del programa.
* **Trazabilidad:** Consola de logs integrada para intercepción de eventos del sistema en vivo y exportación de reportes de backtesting a formato `.csv` para auditoría externa.

## Funcionalidades Destacadas
- [x] Motor de simulación y Backtesting con algoritmos de clasificación.
- [x] Interfaz de gestión de suscripciones y paywall interno.
- [x] Alertas instantáneas integradas con la API de Telegram.
- [x] Despliegue en entorno aislado mediante PyInstaller (`.exe`).

![DeepAxo Dashboaard] (deepaxo_dashboard.png)
![DeepAxo Logs](deepaxo_logs.png)
![DeepAxo Tests QA](tests_qa.png)
---
**Desarrollado por Axel Reyes** | *Junior Quality Assurance Professional & Python Developer*
