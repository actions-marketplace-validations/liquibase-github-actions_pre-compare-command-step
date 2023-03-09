# Liquibase Pre Compare Command Step Action
Official GitHub Action to run Liquibase Pre Compare Command Step in your GitHub Action Workflow. For more information on how pre compare command step works visit the [Official Liquibase Documentation](https://docs.liquibase.com/commands/home.html).
## Pre Compare Command Step
null
## Usage
```yaml
steps:
- uses: actions/checkout@v3
- uses: liquibase-github-actions/pre-compare-command-step@v4.20.0
  with:
    # The JDBC database connection URL
    # string
    # Required
    url: ""

    # 
    # string
    # Optional
    compareControl: ""

    # 
    # string
    # Optional
    database: ""

    # The default catalog name to use for the database connection
    # string
    # Optional
    defaultCatalogName: ""

    # The default schema name to use for the database connection
    # string
    # Optional
    defaultSchemaName: ""

    # Types of objects to compare
    # string
    # Optional
    diffTypes: ""

    # The JDBC driver class
    # string
    # Optional
    driver: ""

    # The JDBC driver properties file
    # string
    # Optional
    driverPropertiesFile: ""

    # Objects to exclude from diff
    # string
    # Optional
    excludeObjects: ""

    # Objects to include in diff
    # string
    # Optional
    includeObjects: ""

    # 
    # string
    # Optional
    objectChangeFilter: ""

    # Output schemas names. This is a CSV list.
    # string
    # Optional
    outputSchemas: ""

    # Password to use to connect to the database
    # string
    # Optional
    password: ""

    # Schemas names on reference database to use in diff. This is a CSV list.
    # string
    # Optional
    referenceSchemas: ""

    # Schemas to include in diff
    # string
    # Optional
    schemas: ""

    # 
    # bool
    # Optional
    skipDatabaseStep: ""

    # 
    # string
    # Optional
    snapshotTypes: ""

    # Username to use to connect to the database
    # string
    # Optional
    username: ""

```

### Secrets
It is a good practice to protect your database credentials with [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

## Optional Liquibase Global Inputs
The liquibase pre compare command step action accepts all valid liquibase global options as optional parameters. A full list is available in the official [Liquibase Documentation](https://docs.liquibase.com/parameters/command-parameters.html).

### Example
```yaml
steps:
  - uses: actions/checkout@v3
  - uses: liquibase-github-actions/pre-compare-command-step@v4.20.0
    with:
      url: ""
      headless: true
      licenseKey: ${{ secrets.LIQUIBASE_LICENSE_KEY }}
      logLevel: INFO
```

## Feedback and Issues
This action is automatically generated. Please submit all feedback and issues with the [generator repository](https://github.com/liquibase/github-action-generator/issues).
