# RDUK - Loggly transport factory for Winston

this module is a [Loggly transport](https://www.npmjs.com/package/winston-loggly-bulk) factory for the [Winston](https://www.npmjs.com/package/winston) implementation of [RDUK logger](https://www.npmjs.com/package/@rduk/logger)

## Installation

```sh
npm i --save --save-exact @rduk/logger @rduk/logger-winston-provider @rduk/logger-winston-loggly-factory
```

## Configuration

```yaml
# config.yml (see @rduk/configuration for detail)
---
logger:
  default: winston
  providers:
    -
      name: winston
      type: '@rduk/logger-winston-provider'
      level: debug
      factories:
        loggly: '@rduk/logger-winston-loggly-factory'
      transports:
        loggly: # options passed to factory
          token: ${LOGGLY_TOKEN}
          subdomain: ${LOGGLY_SUBDOMAIN}
          tags:
            - my-api
          json: true
```

That's it!

## License and copyright

See [LICENSE](LICENSE) file
