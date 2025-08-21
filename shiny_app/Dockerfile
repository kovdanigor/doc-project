# Используем официальный образ Python
FROM python:3.11-slim

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем зависимости
COPY requirements.txt .

# Устанавливаем зависимости
RUN pip install --no-cache-dir -r requirements.txt

# Копируем код приложения
COPY . .

# Открываем порт, на котором будет работать приложение
EXPOSE 8000

# Запускаем приложение
CMD ["shiny", "run", "--host", "0.0.0.0", "--port", "8000", "app.py"]