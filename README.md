# JVM-Sandbox Refactoring: Collaborative Quality Optimization 🚀

Este proyecto presenta una refactorización integral del **Alibaba JVM-Sandbox**, enfocada en la optimización de código, reducción de deuda técnica y cumplimiento de estándares de calidad profesional mediante **SonarQube**.

## 👥 Equipo de Desarrollo
Este trabajo es el resultado de una colaboración multidisciplinar:
*   **Axel:** Optimización de utilidades de String y descriptores de comportamiento.
*   **Gaby:** Refactorización de controladores de eventos y gestión de Servlets.
*   **Lizeth:** Mejora de la arquitectura de `AdviceListener` y el Core Module Manager.
*   **Antonela:** Gestión avanzada de Classloaders y el Event Weaver.
*   **Kevin Llugcha** Reducción de complejidad cognitiva en orquestadores de eventos y estandarización de nombres.

## 🛠️ Mejoras Clave Implementadas

### 1. Reducción de Complejidad Cognitiva
Se transformó el método `switchEvent` de `AdviceAdapterListener.java` (un "Brain Method" altamente complejo) en una estructura modular y mantenible, extrayendo la lógica en manejadores específicos.

### 2. Cumplimiento de Estándares Java
*   Renombrado de métodos que violaban las convenciones de Java (ej. `_transform` -> `doTransform`).
*   Corrección de la Regla **S1186** mediante la documentación de métodos vacíos en clases adaptadoras.

### 3. Modernización de APIs
Se eliminaron dependencias obsoletas en `SandboxStringUtils`, reemplazando métodos deprecados de `IOUtils` por el estándar moderno **try-with-resources** y codificación explícita en UTF-8.

### 4. Encapsulación y Cohesión
Mejora de la visibilidad de métodos internos en `FamilyClassStructure`, moviendo utilidades de filtrado a clases anónimas internas para reducir el acoplamiento.

## 📊 Auditoría de Calidad (SonarQube)
El proyecto fue sometido a escaneos incrementales para documentar el impacto de cada refactorización.
*   **Project Key:** `V2-analisis`
*   **Quality Gate:** Mejorado significativamente mediante la eliminación de Code Smells críticos y reducción de la deuda técnica.

## 🚀 Cómo Ejecutar
1. Levantar el entorno de análisis: `docker-compose up -d`
2. Compilar el proyecto: `mvn clean compile -DskipTests`
3. Ejecutar el scanner: `sonar-scanner`

---
*Proyecto realizado para la asignatura de Ingeniería de Software / Auditoría de Código.*
