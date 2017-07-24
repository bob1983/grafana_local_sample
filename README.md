# grafana_local_sample
## Usage
### Define grafana dashboard

1. `docker-compose up`
2. Open http://localhost:3000 with your browser
  - admin:admin
3. Define datasource
  - Type: influxDB
  - Http settings
    - Url: http://localhost:8086
    - Access: direct
  - InfluxDB Details
    - Database: telegraf
4. Define metrics

### Send sample metrics

echo "myservice.sample:1|c" | nc -w 1 -u localhost 8125
