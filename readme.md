Code to reproduce Spring Boot issue [#10131](https://github.com/spring-projects/spring-boot/issues/10131).
=============



Steps to reproduce:

1. Clone this repository
2. Download HashiCorp Vault ([Mac](https://releases.hashicorp.com/vault/0.8.1/vault_0.8.1_darwin_amd64.zip) | [Linux](https://releases.hashicorp.com/vault/0.8.1/vault_0.8.1_linux_amd64.zip)).
3. Unzip Vault
4. Start Vault with `$ ./vault server --dev --dev-root-token-id=00000000-0000-0000-0000-000000000000`
5. Start `com.example.bug10131.Bug10131Application` and expect:

```
APPLICATION FAILED TO START
***************************

Description:

Binding to target [Bindable@7a84788f type = java.net.URL, value = 'provided', annotations = array<Annotation>[[empty]]] failed:

    Reason: Unable to get value for property u-r-l
```
