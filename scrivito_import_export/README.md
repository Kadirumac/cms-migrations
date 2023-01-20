# Scrivito/Fiona 8 Importer and Exporter

These scripts can be used to export a snapshot of the Scrivito/Fiona 8 content to disk and to load
it back into a Scrivito/Fiona 8 tenant.

Note that the importer removes all existing content from the tenant prior to importing content!

## Requirements

HTTPS access to Fiona 8 or Scrivito.
Provide these env variables: `SCRIVITO_BASE_URL`, `SCRIVITO_TENANT`, `SCRIVITO_API_KEY`.

```
export SCRIVITO_BASE_URL=https://api.scrivito.com # or your Fiona 8 backend URL
export SCRIVITO_TENANT=
export SCRIVITO_API_KEY=

Trox Current
export SCRIVITO_TENANT=trox
export SCRIVITO_API_KEY=973e440afa5c185e1647fbc11fdfe27e

Trox New Tenant
export SCRIVITO_TENANT=9686a259f7dc0245c2234580617618ff
export SCRIVITO_API_KEY=1100275b25a03e1db0066e36c13f932d
```

## Usage of the exporter

```
bundle exec ruby scrivito_export.rb "./export" | tee export.log
```

## Usage of the importer

```
bundle exec ruby scrivito_import.rb "./export" | tee import.log
```
