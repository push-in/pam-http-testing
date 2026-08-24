<!-- pam:product-page:start -->
<div align="center">

# PAM HTTP Testing

**Exercise your HTTP application without opening a socket.**

In-memory requests, fluent response assertions, fakes, and deterministic test helpers for PAM HTTP applications.

[![Release](https://img.shields.io/github/v/release/push-in/pam-http-testing?style=flat-square&label=stable)](https://github.com/push-in/pam-http-testing/releases)
[![CI](https://img.shields.io/github/actions/workflow/status/push-in/pam-http-testing/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/push-in/pam-http-testing/actions)
![PHP](https://img.shields.io/badge/PHP-8.5-777BB4?style=flat-square&logo=php&logoColor=white)
![License](https://img.shields.io/github/license/push-in/pam-http-testing?style=flat-square)

**[Documentation](https://push-in.github.io/pam-docs/packages/http/) · [Why this exists](#why-this-exists) · [What you can build](#what-you-can-build) · [Quick start](#quick-start) · [Issues](https://github.com/push-in/pam-http-testing/issues)**

</div>

---

## Why this exists

In-memory requests, fluent response assertions, fakes, and deterministic test helpers for PAM HTTP applications.

| | |
| --- | --- |
| **Role** | Testing toolkit |
| **Execution path** | PHPUnit-compatible in-memory HTTP harness |
| **This repository owns** | Application-level HTTP test ergonomics |
| **Boundary** | Transport, TLS, proxy, and kernel behavior still require integration tests |

## What you can build

- Fast controller and middleware tests
- JSON, headers, status, and validation assertions
- Regression suites for routes without network flakiness

## Quick start

```bash
pam composer require --dev pushinbr/pam-http-testing
```

The **[PAM documentation](https://push-in.github.io/pam-docs/packages/http/)** covers prerequisites, production setup, and the complete workflow. PAM projects keep normal manifests and lockfiles; product features stay in the package that owns them.
<!-- pam:product-page:end -->

Fast in-memory tests for applications built with `pushinbr/pam-http`.

## See it in action

```php
$client = new Pam\Http\Testing\TestClient($app);
$client->get('/users/42')
    ->assertSuccessful()
    ->assertJsonPath('id', '42');
```

## License

Free and open-source under the [Apache License 2.0](LICENSE). You may use,
modify, and distribute this package for any purpose, including commercially.
