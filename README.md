# rot8

<p align="center">
  <img src="https://img.shields.io/badge/build-passing-brightgreen" alt="Build Status" />
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License" />
  <img src="https://img.shields.io/badge/go-1.20%2B-blue" alt="Go Version" />
</p>

<p align="center">
  <b>rot8</b> is a minimal, high-performance load balancer and reverse proxy written in Go. It features round-robin balancing, active health checks, and a simple JSON configuration for quick setup.
</p>

---

## 🚀 Features

- 🔄 Round-robin load balancing across multiple backend servers
- ❤️ Active health checks to ensure only healthy servers receive traffic
- 📝 Simple JSON-based configuration (`config.json`)
- ⚡ Lightweight and fast, with minimal dependencies

---

## 🛠 Tech Stack

- [Go](https://golang.org/) (1.20+)

---

## 🏗️ Getting Started

### Prerequisites

- Go 1.20 or newer

### 📦 Configuration

The proxy is configured using a JSON file located at `config.json`. Example configuration:

```json
{
  "port": ":8080",
  "healthCheckInterval": "2s",
  "servers": [
    "http://localhost:5001",
    "http://localhost:5002",
    "http://localhost:5003",
    "http://localhost:5004",
    "http://localhost:5005"
  ]
}
```

### ▶️ Running the Proxy

1. **Start the proxy server:**
   ```bash
   go run main.go
   ```

2. **Send requests to the proxy:**
   - All requests to `http://localhost:8080/` will be load balanced across the configured backend servers.

3. **Health checks:**
   - The proxy will automatically check the health of each backend at the interval specified in `config.json`.

4. **Stop the server:**
   - Use Ctrl+C in the terminal.

---

## 📁 Project Structure

```text
├── main.go        # Application entry point and proxy logic
├── config.json    # JSON configuration file
```

---

## 📜 License

This project is licensed under the MIT License.

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://github.com/rubuy-74">rubuy-74</a></sub>
</p>
