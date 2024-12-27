FROM node:alpine
#LABEL authors="Tona Chheun"

WORKDIR /app/

COPY package*.json ./

RUN npm install

#COPY --from=builder /app .
COPY . .

RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

EXPOSE 8080

ENTRYPOINT ["node", "app.js"]