# Dex Component

![Component version](https://img.shields.io/badge/dynamic/yaml?color=blue&label=component+version&query=$.entries.dex[0].version&url=https%3A%2F%2Frepository.platform.karavel.io%2Funstable%2Findex.yaml&style=for-the-badge)
[![Dex version](https://img.shields.io/badge/dynamic/yaml?color=blue&label=dex+version&query=$.entries.dex[0].appVersion&url=https%3A%2F%2Frepository.platform.karavel.io%2Funstable%2Findex.yaml&style=for-the-badge)](https://dexidp.io)
[Documentation](https://docs.karavel.io/components/dex)

## Overview

Dex is an identity service that uses OpenID Connect to drive authentication for other apps.

Dex acts as a portal to other identity providers through “connectors.” This lets Dex defer authentication to LDAP servers,
SAML providers, or established identity providers like GitHub, Google, and Active Directory.
Clients write their authentication logic once to talk to Dex, then Dex handles the protocols for a given backend.

## License

The Dex Component is licensed under the [Apache 2.0 license](LICENSE).

The Karavel Container Platform is licensed under the [Apache 2.0 license](https://github.com/projectkaravel/platform/blob/main/LICENSE).
