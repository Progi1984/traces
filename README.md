# Traces

Traces is a micro CLI application that is able to get all contributors and their contributions in 
"developer-readable" JSON format for a specified repository.
 
 
## Installation
 
The authentication is a basic login/password for GitHub.
 
```bash
 $ composer require prestashop/traces
 
 $ ./vendor/bin/traces <repositoryOwner/repositoryName> <login> <password> --config="config.yml"
```

> Note: If your Github login uses two-factor authentication, use an API token instead of password

A file named ``contributors.js`` will be generated, you can manipulate it using any programming language.

## Configuring
 
There are a number of settings that can be configured via the config file. Take a look at the `config.dist.yml` file for an example.

Option | Description
-------|-------------
exclusions | List of excluded users.
keepExcludedUsers | Set to `true` to flag excluded contributors instead of filtering them out from the output.
fieldsWhitelist | List of fields to keep from the API result. Leave blank if you want to keep them all.

## License

This project is released under the MIT license.
