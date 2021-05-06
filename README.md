# arillo/silverstripe-fluent-misdirection

Replacement of MisdirectionRequestFilter for interop with Fluent.

## Config

Add a config file e.g. `misdirection.yml` with the following contents:

```yaml
---
name: arillo-misdirection-request-filters
After:
  - '#misdirection-request-filters'
---
SilverStripe\Core\Injector\Injector:
  SilverStripe\Control\RequestProcessor:
    properties:
      filters:
        - '%$Arillo\Misdirection\FluentMisdirectionRequestFilter'

```