[![Build on Push](https://github.com/TaurMorchant/qubership-core-utils-tmp/actions/workflows/build-on-commit.yaml/badge.svg?branch=main)](https://github.com/TaurMorchant/qubership-core-utils-tmp/actions/workflows/build-on-commit.yaml)

# Core Utils - TLS Utilities

A lightweight Java library providing TLS (Transport Layer Security) configuration and authentication utilities for secure communications.

## Features

- Default TLS configuration with PKIX trust manager
- Customizable TLS configurations via SPI
- SSL Context and trust/key store management  
- Machine-to-Machine (M2M) authentication support
  - Pluggable M2M token providers via SPI
  - Priority-based provider selection
  - Default dummy implementation for testing
  - Token management with type, value and expiration tracking
- Service Provider Interface (SPI) for extensibility

## Requirements

- Java 17+
- Maven 3.x

## Installation

Add the dependency to your Maven project:

```xml
<dependency>
    <groupId>org.qubership.cloud.security.core.utils</groupId>
    <artifactId>tls-utils</artifactId>
    <version>2.0.0-SNAPSHOT</version>
</dependency>
```

## M2M Authentication

The M2MManager interface provides a flexible way to handle machine-to-machine authentication:

- Implement custom token providers by extending M2MManager
- Configure provider priority to control which implementation is used
- Token includes type, value, issuedAt and expiresAt timestamps
- Default DummyM2MManager provided for testing scenarios

## Documentation

- [Contributing Guide](CONTRIBUTING.md)
- [Code of Conduct](CODE-OF-CONDUCT.md) 
- [Security Policy](SECURITY.md)

## License

Apache License 2.0 - see [LICENSE](LICENSE)

