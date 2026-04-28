# AI-Voice-Solutions

## 🖥️ Interfaz de Usuario (Gradio)
El proyecto incluye una aplicación web sencilla para probar la transcripción de audio (STT) en tiempo real:

- **Micrófono:** Transcribe voz en vivo.
- **Archivos:** Soporta carga de archivos `.mp3` o `.wav` de larga duración mediante chunking de 30 segundos.

Para ejecutar la demo:
```bash
python src/stt_gradio_app.py
