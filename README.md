# Pterodactyl Helm Chart

This Helm chart deploys Pterodactyl, an open-source game server management panel, onto a Kubernetes cluster.

## Quick Start

1. Add the Helm chart repository:

   ```bash
   helm repo add pterodactyl-helm-chart https://memorybay.github.io/pterodactyl-helm-chart/
   ```

2. Install the Pterodactyl Helm chart:

   ```bash
   helm install pterodactyl-release pterodactyl-helm-chart/pterodactyl-panel
   ```

3. Access the Pterodactyl game panel:

   - Retrieve the panel's external IP address:

     ```bash
     kubectl get svc pterodactyl-release-ptero-panel -o jsonpath='{.status.loadBalancer.ingress[0].ip}'
     ```

   - Open your web browser and navigate to the provided IP address.

4. Follow the on-screen instructions to set up and configure your Pterodactyl instance.

## Configuration

The Helm chart provides various configuration options that can be customized. Refer to the `values.yaml` file for a list of available configurations.

To override the default values, create a custom `values.yaml` file and use it during installation:

```bash
helm install pterodactyl-release pterodactyl-helm-chart/pterodactyl-panel -f custom-values.yaml
```

## Contributing

We welcome contributions! If you encounter issues or have suggestions, please [open an issue](https://github.com/memorybay/pterodactyl-helm-chart/issues) or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
