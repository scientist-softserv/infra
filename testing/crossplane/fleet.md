defaultNamespace: crossplane-system
helm:
  repo: https://charts.crossplane.io/stable
  chart: crossplane
  values:
    args: ["--enable-external-secret-stores"]
    metrics:
      enabled: false
    webhooks:
      enabled: false
    configuration:
      package:
        - xpkg.upbound.io/upbound/platform-ref-aws:v0.6.0
    provider:
      package:
        - xpkg.upbound.io/upbound/provider-aws:v0.37.0
        - xpkg.upbound.io/crossplane-contrib/provider-aws:v0.39.0
        - xpkg.upbound.io/digitalocean/provider-digitalocean:v0.2.0
