# IDEA — MoneyPrinterTurbo (mi versión)

Objetivo: personalizar y extender MoneyPrinterTurbo para generar videos cortos con IA.

## Tareas

### APP-001: Revisar estructura del proyecto
Paths: app/services/llm.py, app/services/video.py, app/services/voice.py, app/services/subtitle.py
Verify: pytest test/services/test_llm.py test/services/test_video.py
Depends on: none

### APP-002: Configurar entorno de desarrollo local
Paths: config.example.toml, requirements.txt, pyproject.toml, Dockerfile
Verify: python -c "import app; print('ok')"
Depends on: none

### APP-003: Ejecutar suite de pruebas existentes
Paths: test/
Verify: pytest test/ -x -q
Depends on: APP-002

### APP-004: Añadir nuevo proveedor de TTS
Paths: app/services/voice.py
Verify: pytest test/services/test_voice.py
Depends on: APP-001

### APP-005: Personalizar pipeline de generación de video
Paths: app/services/task.py, app/services/video.py
Verify: pytest test/services/test_task.py
Depends on: APP-001
