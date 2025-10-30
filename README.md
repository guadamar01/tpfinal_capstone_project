# 🤖 Menta - Asistente de Bienestar Alimenticio con IA

<div align="center">

### Proyecto Final – Samsung Innovation Campus 2025  
**Equipo:** Guadalupe · Fabiana · Rocco

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Telegram](https://img.shields.io/badge/Telegram-Bot-blue.svg)](https://telegram.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

</div>

---

## 🧠 Descripción

**Menta** es un bot inteligente de Telegram que combina **4 tecnologías de IA** para acompañar a los usuarios en la mejora de sus hábitos alimenticios y su relación emocional con la comida.

El asistente interpreta emociones expresadas por voz o texto, analiza imágenes de comidas, detecta patrones y ofrece **recomendaciones personalizadas** para promover una alimentación consciente, educativa y equilibrada.

---

## ⚙️ Funcionalidades de IA

| # | Funcionalidad | Tecnología | Estado |
|---|--------------|------------|---------|
| 1️⃣ | **Análisis de sentimientos** | Transformers (RoBERTuito) | ✅ |
| 2️⃣ | **Respuestas automáticas** | Dataset personalizado JSON | ✅ |
| 3️⃣ | **Audio → Texto** | Groq Whisper Large V3 | ✅ |
| 4️⃣ | **Análisis de imágenes** | Groq Vision (Llama 3.2 90B) | ✅ |

### 🎯 Características destacadas

- 🎤 **Reconocimiento de voz:** Transcribe y analiza mensajes hablados
- 💬 **Análisis emocional:** Detecta frustración, motivación, ansiedad y más
- 📸 **Vision AI:** Identifica alimentos en fotos y evalúa su valor nutricional
- 🧠 **Memoria contextual:** Recuerda el estado emocional previo del usuario
- 📊 **Seguimiento de progreso:** Registra evolución emocional a lo largo del tiempo
- 🌱 **Tono empático:** Respuestas personalizadas en español argentino

---

## 🚀 Tecnologías utilizadas

### Backend & IA
- **Python 3.10+**
- **PyTelegramBotAPI** - Framework del bot
- **Groq Cloud AI** - APIs de Whisper y Vision
- **Transformers (Hugging Face)** - Modelo de sentimientos
- **PyTorch** - Deep Learning

### Herramientas
- **python-dotenv** - Gestión de variables de entorno
- **matplotlib** - Visualización de progreso emocional
- **pandas** - Análisis de datos

---

## 📂 Estructura del proyecto

```
proyecto-menta/
├── data/
│   ├── dataset.json           # Base de conocimientos (recomendaciones)
│   ├── user_logs.json         # Historial de interacciones
│   ├── user_memory.json       # Memoria contextual por usuario
│   └── temp/                  # Archivos temporales (audio/imágenes)
│
├── src/
│   ├── bot_voz.py            # 🤖 Bot principal (COMPLETO)
│   ├── gui_app.py            # Interfaz gráfica local (opcional)
│   │
│   ├── analysis/
│   │   ├── sentiment_analysis.py      # Análisis de sentimientos
│   │   ├── habit_recommender.py       # Sistema de recomendaciones
│   │   ├── image_analysis.py          # Análisis de imágenes (IA Vision)
│   │   └── emotion_trends.py          # Gráficos de progreso
│   │
│   └── utils/
│       ├── memory_manager.py          # Gestión de memoria contextual
│       └── progress_logger.py         # Registro de interacciones
│
├── .env                      # ⚠️ Credenciales (NO SUBIR A GITHUB)
├── .env.example              # Plantilla de configuración
├── .gitignore                # Archivos ignorados
├── requirements.txt          # Dependencias Python
├── README.md                 # Este archivo
└── simular_usuario_local.py  # Testing sin Telegram
