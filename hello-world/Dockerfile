#Базовый образ ноды (легковесный)
FROM node:18-alpine

# Данная команда создает рабочую директорию внутри контейнера
WORKDIR /app

# Шаг 3: Копируем package.json и package-lock.json в /app
COPY package*.json ./
# Установка зависимостей
RUN npm install
# Копируем оставшиеся файлы
COPY . .
#Сборка приложения
RUN npm run build
#Запускаем приложение
CMD ["npm", "start"]



