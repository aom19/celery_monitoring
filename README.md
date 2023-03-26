# Celery Monitoring

Celery Monitoring is a sample project that demonstrates how to monitor Celery tasks using Prometheus, Grafana, and Flower.

## Overview

The project consists of a simple web application that generates random cat images using the [TheCatAPI](https://thecatapi.com/). The images are generated asynchronously using Celery tasks. The project also includes a Celery worker and a Flower instance for monitoring the Celery tasks.

## Installation

To install and run the project, follow these steps:

1. Clone the repository:
```bash
git clone https://github.com/aom19/celery_monitoring.git
 ```
2. Change to the project directory:
```bash
 cd celery_monitoring
```
3. Build the Docker containers:
```bash
docker-compose build
```
4. Start the containers:
```bash
docker-compose up
```

5. Access the web application at http://localhost:8000.
6. Access Flower at http://localhost:5555.
7. Access Prometheus at http://localhost:9090.
8. Access Grafana at http://localhost:3000.

## Monitoring

To monitor the Celery tasks, follow these steps:

1. Open Grafana at http://localhost:3000.
2. Log in using the default credentials (username: admin, password: admin).
3. Add Prometheus as a data source:
1. Click on the "Add data source" button.
2. Select "Prometheus".
3. Set the URL to http://prometheus:9090.
4. Click on "Save & Test".
4. Import the Celery dashboard:
1. Click on the "Create" button and select "Import".
2. Enter 8919 as the dashboard ID.
3. Select "Prometheus" as the data source.
4. Click on "Import".
5. View the Celery dashboard to monitor the Celery tasks.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



### Sceenshot Grafana Dashboard 
![Screenshot 2023-03-27 at 12.51.36 AM.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fpg%2Fwlshlqj96dz82_v0k9pvr3b40000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_WdvXiA%2FScreenshot%202023-03-27%20at%2012.51.36%20AM.png)

### Screenshot Celery Flower
![Screenshot 2023-03-27 at 12.55.34 AM.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fpg%2Fwlshlqj96dz82_v0k9pvr3b40000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Rqflmg%2FScreenshot%202023-03-27%20at%2012.55.34%20AM.png)