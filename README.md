# AI-Voice-Solutions

🖥️ Interfaz de Usuario (Gradio)
El proyecto incluye una aplicación web interactiva diseñada para validar la precisión del modelo Whisper en diferentes escenarios de audio:

Micrófono: Permite realizar pruebas rápidas de transcripción de voz en vivo, ideal para simular la respuesta inmediata de un cliente.

Archivos: Soporta la carga de archivos .mp3, .wav o .m4a. Implementa una lógica de chunking de 30 segundos para procesar grabaciones de larga duración sin pérdida de contexto.

⚙️ Funcionamiento Técnico
La interfaz actúa como un puente entre el usuario y el motor de inferencia:

Captura: Se recibe el flujo de audio (vía mic o archivo).

Pre-procesamiento: El audio se normaliza y se ajusta a una tasa de muestreo de 16KHz (requerido por Whisper).

Inferencia: El modelo openai/whisper-tiny (o la versión configurada) procesa los segmentos.

Salida: Se devuelve el texto limpio en un componente de Gradio para su revisión.

🚀 Cómo ejecutar la demo
Asegúrate de tener instaladas las dependencias y el motor de audio en tu sistema (Debian/Ubuntu):

# Instalación de dependencias de audio del sistema
sudo apt update && sudo apt install ffmpeg -y

# Ejecución de la interfaz
python src/stt_gradio_app.py
