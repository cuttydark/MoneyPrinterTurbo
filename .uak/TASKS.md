# Backlog · MoneyPrinterTurbo

## APP-001
Title: Revisar estructura del proyecto
State: PLANNED
Priority: P0
Paths: app/services/llm.py, app/services/video.py, app/services/voice.py, app/services/subtitle.py
Verify: pytest test/services/test_llm.py test/services/test_video.py
Depends on: none

## APP-002
Title: Configurar entorno de desarrollo local
State: PLANNED
Paths: config.example.toml, requirements.txt, pyproject.toml, Dockerfile
Verify: python -c "import app; print('ok')"
Depends on: none

## APP-003
Title: Ejecutar suite de pruebas existentes
State: PLANNED
Paths: test/
Verify: pytest test/ -x -q
Depends on: APP-002

## APP-004
Title: Añadir nuevo proveedor de TTS
State: PLANNED
Paths: app/services/voice.py
Verify: pytest test/services/test_voice.py
Depends on: APP-001

## APP-005
Title: Personalizar pipeline de generación de video
State: PLANNED
Paths: app/services/task.py, app/services/video.py
Verify: pytest test/services/test_task.py
Depends on: APP-001
