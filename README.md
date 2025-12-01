# Práctica Profesional I – Generación automática de problemas de optimización con IBEX y modelos generativos

Este repositorio contiene todos los archivos correspondientes a mi Práctica Profesional I en la Escuela de Informática y Telecomunicaciones (EIT) de la Universidad Diego Portales (UDP).

El proyecto consiste en la generación automática de problemas de optimización (.bch) utilizando modelos de lenguaje locales, como GPT4All / Phi-3, y su posterior validación mediante IBEXOpt.


## 📁 Estructura del repositorio

/data/
├── Avance practica I.pdf → Informe parcial de avance
├── ejemplos generados (.bch) → Archivos .bch creados con la IA
├── carpeta easy (original IBEX) → Ejemplos válidos para entrenamiento
└── logs / pruebas → Resultados de ejecución



## 🚀 Objetivo del proyecto

- Generar automáticamente ejercicios de optimización con restricciones y dominios válidos.
- Validar sintaxis mediante ejecución real en **IBEXOpt**.
- Construir un workflow reproducible para:
  1. Entrenar o guiar al modelo generativo.
  2. Generar nuevos archivos `.bch`.
  3. Validarlos (tiempo, nodos, errores).
  4. Registrar resultados.


## 🛠️ Archivos principales

### 🔹 Código Python
- `client_pipe.py`  
  Envía solicitudes de generación al worker C++ usando **named pipes**.

### 🔹 Código C++
- `worker_ibex`  
  Ejecuta IBEXOpt y retorna resultados (nodos, tiempo, errores).

### 🔹 Archivos `.bch` generados  
Todos se suben, incluso los que fallan.  
Sirven para estudiar qué estructura entiende mejor el modelo generativo.


## 📚 Herramientas utilizadas

- **IBEX / IBEXOpt**
- **GPT4All (modelo Phi-3 Mini Instruct 4B)**
- Python 3.10
- C++17
- Linux Ubuntu
- Named Pipes


## 📄 Informe

El informe completo de la práctica se encuentra en:

📌 `data/Avance practica I.pdf`



## 👩‍💻 Autora

**Valentina Aguirre Marambio**  
Estudiante de Ingeniería Civil Informática y Telecomunicaciones  
Universidad Diego Portales  


## 📬 Contacto

Para dudas o revisiones:  
valentina.aguirre@mail.udp.cl
