El proyecto fue desarrollado originalmente como trabajo académico en Google Colab.

---

# 🚀 Emotion Music – MLOps & Serving

Este repositorio contiene la **Fase 2 (Producción)** del proyecto **“Ponele música a tus emociones”**. Aquí transformamos el modelo de investigación en un microservicio escalable y listo para la nube.

> **Estado:** 🚧 En Desarrollo (Migración desde fase de Research).

## 🎯 Objetivo de esta Fase

El foco principal es la **operacionalización**. Buscamos garantizar que el modelo entrenado sea reproducible y accesible a través de una API, eliminando el _Training-Serving Skew_ mediante la contenedorización.

## 🛠️ Stack de Ingeniería

- **Servicio de API:** FastAPI (Python).
- **Contenedorización:** Docker.
- **Orquestación/Cloud:** Vertex AI (Google Cloud Platform).
- **Inferencia:** TensorFlow Serving / Custom Container.

## 🧱 Arquitectura del Microservicio

1. **Endpoint REST:** Recibe una imagen enviada desde el Frontend (React).
2. **Pre-processing Layer:** Replicamos exactamente las transformaciones de la fase de research (48x48, Grayscale, Normalización).
3. **Inferencia:** El modelo predice la emoción dominante.
4. **Respuesta:** Devuelve un JSON con la emoción y los metadatos necesarios para la recomendación musical.

## 🐳 Cómo ejecutar (Local con Docker)

_(Próximamente instrucciones de `docker build` y `docker run`)_

---

🎨 _Este repositorio se complementa con el trabajo de investigación disponible en [emotion-music-training](https://github.com/ClaudiaMetz/emotion-music-training)._

⏭️ **Nota de evolución:** El desarrollo del proyecto continúa en la versión 2.0 dentro del repositorio [emotion-music-mlops-v.2.xx](https://github.com/ClaudiaMetz/emotion-music-mlops-v.2.xx).