# data-minimization helm charts

The helm chart provided in this repo allows you to deploy tools from the [peng-data-minimization org](https://github.com/peng-data-minimization) on Kubernetes.

Currently, we provide charts for the following tools:

- [Streaming Provider Interface (SPI)](https://github.com/peng-data-minimization/kafka-spi)

## Deployment
Install the helm repo.

```
helm repo add dm-helm-charts https://peng-data-minimization.github.io/helm-charts
```

Install the SPI worker.

```
helm install --name dm-spi dm-helm-charts/spi -f PATH_TO_YOUR_SPI_CONFIG
```
For more information on the configuration, refer to the documentation of the SPI.

Run `kubectl get pods` to make sure that pods have been started correctly.


## Development
To install this chart form source run 
```
helm install spi charts/spi/ -f PATH_TO_YOUR_SPI_CONFIG
```


