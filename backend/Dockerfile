ARG PYTHON_VERSION=3.11-alpine
FROM python:3.11-alpine

WORKDIR /app

# Для целей безопасности создаём не root-пользователя
RUN addgroup -g 1000 -S appgroup && adduser -u 1000 -S appuser -G appgroup 

COPY app.py .

USER appuser

EXPOSE 8080

CMD ["python", "app.py"]
