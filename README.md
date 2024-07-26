# Heva Helm Charts

## Contributing

### Requirements
* https://github.com/helm/chart-testing
* https://github.com/bitnami/readme-generator-for-helm

### CI

Run linter in chart directory:
```
ct lint --chart-dirs . --charts .
```

Update chart parameters in readme
```
readme-generator -v values.yaml -r README.md
```
