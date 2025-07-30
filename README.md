# TLSecho

🛡️ Высокопроизводительный TLS echo-сервер на C++20 + epoll + OpenSSL 3.0

## 📌 Цель

Создать минималистичный echo-сервер, который обрабатывает ≥10 000 RPS через TLS 1.3 с использованием только epoll и OpenSSL, без сторонних фреймворков.

## ⚙️ Особенности

- C++20, epoll, OpenSSL 3.x
- Только user-space, протестировано на Debian 12
- Без зависимостей (чистый `scratch` Docker)
- Поддержка TLS 1.3
- Port: `8443`
- Graceful shutdown по `SIGTERM`
- CI: GitHub Actions (GCC, Clang, Sanitizers, Valgrind)

## 🚀 Производительность

- ≥10 000 RPS (`wrk -t4 -c1000 -d30s`)
- p99 latency ≤1ms (loopback)
- Docker-образ <5MB

<p align="center">
  <img src="assets/wrk-benchmark.gif" width="500" alt="wrk demo">
  <img src="assets/flamegraph.svg" width="500" alt="perf flamegraph">
</p>

## 📁 Структура

