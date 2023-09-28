# Prepares a Runner for Provisioning (Apple)

A Github Action that allows you to easily import provisioning profiles and signing certificates to prepare a runner for code signing and the building of artifacts.

## Usage

```yaml
- name: Import Profiles
        uses: ./
        with:
        signing_certificate: ${{ secrets.DISTRIBUTION_CERTIFICATE_BASE64 }}
        signing_certificate_password: ${{ secrets.DISTRIBUTION_CERTIFICATE_PASSWORD }}
          profiles: |
          	${{ secrets.DISTRIBUTION_PROFILE }}
          	${{ secrets.EXTENSION_DISTRIBUTION_PROFILE }}
```

## Additional Arguments

There are a number of additional, optional arguments that can be provided to more closely control the creation of the keychain to import a signing certificate into. See [action.yml](action.yml) for more information.
