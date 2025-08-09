# Monitoring with Docker Compose using InfluxDB, Telegraf and Grafana

This repository contains a Docker Compose setup for creating containers for InfluxDB, Telegraf, Modbus Generator, and Grafana, providing a comprehensive monitoring solution.

## Quick Start

### Download docker desktop

### Clone the Repository

```bash
git clone https://github.com/thanakritju/modbus-monitoring
cd modbus-monitoring
```

### Deploy the Stack

```bash
docker-compose up -d
```

1. **Access Grafana**:
   - Open your browser and navigate to `http://localhost:3000`
   - Default credentials: username and password are both `admin`

## Using the Repository

### Configuring Telegraf

- Telegraf configuration files are located in the `telegraf` directory.
- After modifying the configuration files, restart the Telegraf container:
  ```bash
  docker-compose restart telegraf
  ```

### Viewing Metrics in Grafana

1. Open Grafana and add InfluxDB as a data source.
2. Create dashboards and panels to visualize the metrics collected by Telegraf.

## Service Descriptions

1. **InfluxDB**: A time-series database designed for high write and query loads, used to store metrics collected by Telegraf.

2. **Telegraf**: An agent for collecting, processing, aggregating, and writing metrics. It gathers data from the host and Docker containers, sending it to InfluxDB.

3. **Grafana**: A web-based interface for visualizing metrics stored in InfluxDB, allowing creation of dashboards and panels for monitoring.

4. **Modbus Generator**: A simulator for Modbus data.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.