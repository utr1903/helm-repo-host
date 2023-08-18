# Steps

## Developing

### Create a Helm chart

Move into the `helm` directory and create a Helm chart

```bash
cd ./helm
helm create myapp
```

Adapt according to your needs

## Hosting

After merging a branch into the `main` branch and releasing a new version of the app, perform the following steps within the `main` branch.

### Package the Helm chart

Package the helm chart into the `charts` folder in the root directory of the repo

```bash
mkdir charts
helm package ./helm/myapp -d ./charts
```

### Create/update the index.yaml

```bash
helm repo index ./charts
```
