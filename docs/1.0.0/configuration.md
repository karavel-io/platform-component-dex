# Configuration

```hcl
component "dex" {
  namespace = "dex"

  # Params default values

  publicURL = "" # required, the full URL to reach the Dex instance, e.g. https://oauth.company.com

  connectors = [
    # Add your connectors here
    # ...
    # See https://dexidp.io/docs/connectors/ for available choices and their configuration schema

    # Example entry
    {
      type = "github" # required, specify "github" for GitHub
      id = "github"   # required, Connector ID
      name = "GitHub" # required, Connector human readable name
      config = {
        # ... config fields as specified in https://dexidp.io/docs/connectors/github/
      }
  ]

  secret = {
    # override this section only if you are not using the default store from the external-secrets component
    store = {
      name = "default"
      kind = "ClusterSecretStore"
    }
    key = "" # required, should be the store-specific key to the secret, e.g. the Vault or AWS Secrets Manager key
  }
}
```

## Secrets

Secrets referenced by the configuration must be provisioned in the backend service of your choice before installing Dex.

Unless you changed the configuration of the External Secret component or manually provisioned a custom `SecretStore` resource, you don't need to override the `store` section of each secret reference.
