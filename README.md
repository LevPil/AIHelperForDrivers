# Контракт. От Java к Python
{
    "sessionId": "session ID",
    "requestType": "TEXT" | "AUDIO",
    "content": "текст_запроса_пользователя", 
    "audio_file": "название_файла",
    "modelType": "LOCAL" | "GLOBAL"
} 

# Контракт. От Python к Java
{
  "sessionId": "string",
  "content": "string",
  "audio_response": "string | null"
}

# Примечание. Если присутствует флаг TEXT - ключа audio_file не будет. Если есть флаг AUDIO - ключа content не будет.

# Названия директорий
Для java: input-dir;
Для python: output-dir;

# Контракт. Префикс для хранения java-сессий в Redis
backend:session

# Запуск проекта. Команды для запуска проекта
1. mvn clean install
2. mvn spring-boot:run -pl api-realisation

# Развёртывание модели. PowerShell, Docker. Команды
Создаёшь папки на диске. в driving-ai файл docker-compose.yml

# Контейнеризация. Команды в Docker
docker compose up -d 

docker exec -it ollama-server sh (зайти в оламу в ней работать)
ollama create qwen3.5-driving -f /Modelfile (уже в bash-е внутри оламы)

ollama list (проверка наличия модели qwen в ollama)

# Порты:
Redis - 6379
Python - 8000

# **Endpoint:** `POST /api/ai-process`  
# **Content-Type:** `application/json`






# Redis и работа с Java

Добавлен Redis в Python (хранение самм. контекста сервиса) и схемы запроса и ответа(JavaRequest JavaResponse)
