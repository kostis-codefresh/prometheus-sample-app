# Example Go app that exposes Prometheus metrics

[![Go Report Card](https://goreportcard.com/badge/github.com/kostis-codefresh/prometheus-sample-app)](https://goreportcard.com/report/github.com/kostis-codefresh/prometheus-sample-app)


Original code modified from https://gabrieltanner.org/blog/collecting-prometheus-metrics-in-golang


## How to build

Run:

 *  `go build` to get the executable OR
 *  `docker build . -t example-app` to create a container image if you prefer docker instead or don't have access to a Go dev environment

## How to run the application on its own

 * `go run .` OR
 * `docker run -p 8080:8080 example-app`

 Then visit http://localhost:8080 or http://localhost:8080/metrics

 ## How to run with Prometheus and Graphana

 Run `docker-compose up`

 You can access Prometheus at http://localhost:9090 and Graphana at http://localhost:3000

1. Login into Graphana. Default user/password for Graphana is admin/admin
1. Add a datasource for type Prometheus at address http://localhost:9090 and auth type "Browser" 
1. Import [graphana/graphana-dashboard.json] as a premade dashboard