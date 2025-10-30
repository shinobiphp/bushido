# Bushido Framework

**_Bushido_** is the 'Way of the Warrior' for modern PHP development. It is an **opinionated, modular framework** forged from decades of engineering mastery, best practices, and composable patterns. Designed for PHP 8.4+, it provides the foundation to build scalable, maintainable, and high-performing applications — web, CLI, or asynchronous Swoole-powered services.

## The Nine Kujis of Bushido

Bushido is built for developers who seek discipline, clarity, and mastery. Its core principles — the **Nine Kujis** — are your guide to writing enduring, battle-ready code:

- **Modularity:** Self-contained, discoverable components that can be reused across projects.
- **Composability:** Assemble complex systems from simple, predictable building blocks.
- **Event-Driven:** Full support for synchronous and asynchronous flows, enabling resilient architectures.
- **Observability:** Logging, metrics, and tracing baked in for complete operational insight.
- **Security:** Zero-trust by default, signed messages, and idempotent operations to defend your systems.
- **Discipline:** Opinionated conventions, patterns, and code standards to maintain consistency.
- **Scalability:** Architect for growth, performance, and distributed workloads from the start.
- **Extensibility:** Plug-in modules, adapters, and integrations for evolving business requirements.
- **Resilience:** Automated retries, failure compensation, and fault-tolerant orchestration.

## Getting Started

1. Install via Composer:

```bash
composer require shinobiphp/bushido
```

2. Boot the framework:

```php
use Bushido\Bushido;

$app = Bushido::boot();
// Initialize and configure your app here
$app->run();
```

3. Explore modular components, create services, and integrate with your chosen runtime.

## Documentation

Full documentation, guides, and tutorials can be found at [shinobiforge.online](https://shinobiforge.online)
