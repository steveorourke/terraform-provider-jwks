---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "jwks_from_certificate Data Source - terraform-provider-jwks"
subcategory: ""
description: |-
  Calculates a JSON Web Key Set from a given certificate.
---

# jwks_from_certificate (Data Source)

Calculates a JSON Web Key Set from a given certificate.

## Example Usage

```terraform
data "jwks_from_certificate" "pem_example" {
  key = file("${path.module}/certificate.pem")
}

data "jwks_from_certificate" "pem_example_2" {
  key = file("${path.module}/certificate.pem")
  kid = "123"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `pem` (String) Requires a PEM-encoded single certificate or correctly ordered certificate chain that starts with an end-entity certificate.
							Each certificate in the chain is the certificate of the CA that issued the previous certificate.

### Optional

- `kid` (String) Used to override the kid field of the JWK

### Read-Only

- `id` (String) The ID of this resource.
- `jwks` (String) The calculated JWKS

