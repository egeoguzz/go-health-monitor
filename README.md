# Go Health Monitor

A simple Go application designed to periodically check the health status of specified web services and send notifications when a failure threshold is breached.

## Features

-   **YAML Configuration:** Easily configure services and settings through a `config.yaml` file.
-   **Configurable Thresholds:** Define how many consecutive failures trigger an "unhealthy" status.
-   **Webhook Notifications:** Sends alerts on both service failure and recovery events.
-   **Testable Code:** Written with interfaces and dependency injection to be fully unit-testable.
-   **Clean Architecture:** Logic is separated into distinct packages (`monitor`, `notifier`) for better maintainability.

## Getting Started

### Prerequisites

-   Go 1.18 or higher

### Installation & Running

1.  Clone the repository:
    ```sh
    git clone https://github.com/egeoguzz/go-health-monitor.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd go-health-monitor
    ```
3.  Install dependencies:
    ```sh
    go mod tidy
    ```
4.  Run the application:
    ```sh
    go run cmd/monitor/main.go
    ```

The monitor will start checking the services defined in `config.yaml` at the specified interval.
