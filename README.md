# hw1

Как запустить сервис:
1) скачать репозиторий
2) перейти в корень репоитория
3) применить конфигурации командой `kubectl apply -f deployment.yaml -f service.yaml -f ingress.yaml --validate=false`
4) прописать домен arch.homework в локальный файл /etc/hosts командой `echo "$(minikube ip) arch.homework" | sudo tee -a /etc/hosts`
5) проверить работоспособность `curl -i http://arch.homework/health/`

Получим ответ от сервиса `'{"status": "ok"}'`
