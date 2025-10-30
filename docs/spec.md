# Shinobi Ecosystem Spec — Full Technical + Conceptual Blueprint

```json
{
  "ecosystem": {
    "name": "Shinobi",
    "description": "Composable, self-evolving enterprise capability and revenue optimization platform.",
    "origin": "Spawned from the divine power of Shinobi, bound and shaped by the Path of Bushido.",
    "tech_stack": {
      "language": "PHP 8.4+",
      "framework": "Bushido (custom, modular, attribute-driven)",
      "async_server": "OpenSwoole",
      "data": {
        "cognition_substrate": "Postgres",
        "dna_storage": "ProtoBuf definitions in src/DNA",
        "event_storage": "Message queues or Postgres-based outbox pattern"
      },
      "communication": {
        "inter_node": "gRPC (OpenSwoole client/server)",
        "message_types": ["sync", "async", "event"]
      },
      "frontend": {
        "forge_ui": "Astro w/ web components (Shadow DOM) + Alpine.js",
        "optional": "Vue/Svelte islands if needed"
      },
      "ci_cd": ["Pest", "PHPUnit", "Behat for BDD"],
      "security": "Zero-trust, message signing, idempotency, validation, ACLs"
    },
    "components": {
      "Bushido": {
        "name": "Bushido",
        "lore_name": "Path of the Code Samurai",
        "description": "Modular framework guiding creation of capabilities and deployment into Shinobi.",
        "kuji": [
          {
            "name": "Composability",
            "lore_name": "Mugen",
            "enterprise_description": "Infinite modularity; drives code scaffolding and system composition."
          },
          {
            "name": "Event Discipline",
            "lore_name": "Seishin",
            "enterprise_description": "Structured event-driven architecture; maps to observability and telemetry."
          },
          {
            "name": "Capability Harnessing",
            "lore_name": "Yokai",
            "enterprise_description": "Integration of external services or high-level capabilities (GraphQL, gRPC, APIs)."
          },
          {
            "name": "Energy Flow",
            "lore_name": "Ki",
            "enterprise_description": "Configuration/state binding; powers node deployments and message signing."
          },
          {
            "name": "Command Mastery",
            "lore_name": "Kuji-in",
            "enterprise_description": "Defines commands structure (sync/async/event), enabling orchestration."
          },
          {
            "name": "Observability",
            "lore_name": "Rei",
            "enterprise_description": "Monitoring, logging, metrics, AI analytics, and feedback loops."
          },
          {
            "name": "Resilience",
            "lore_name": "Fukurokuju",
            "enterprise_description": "Fault-tolerance, retries, compensations, distributed consistency."
          },
          {
            "name": "Security",
            "lore_name": "Anzen",
            "enterprise_description": "Zero-trust, signature verification, ACLs, input validation."
          },
          {
            "name": "Discovery & Reflection",
            "lore_name": "Shinpi",
            "enterprise_description": "Auto-discovery of components, attribute-driven registration, and orchestration."
          }
        ],
        "scaffolding_instructions": {
          "components": "Each Kuji drives scaffolding rules; example: 'Mugen' triggers creation of modular folders/files for each component.",
          "dna_proto": "Generate ProtoBuf definitions for each entity, event, command, query; place in src/DNA/{domain}/{vX}/",
          "bindable_components": "Implement interfaces: get(), create(), update(), delete(), commit()",
          "tests": "Generate Pest/PHPUnit tests from Kuji rules and BDD scenarios; optional Behat for high-level flows."
        }
      },
      "Shinobi": {
        "description": "Runtime and orchestration engine for Bindable Components.",
        "subsystems": {
          "ContextRepository": "Semantic state store; maps context to components and deployment.",
          "FederatedServiceNodes": "Manages nodes and component versions; ensures single version per node.",
          "MessageModerator": "Handles routing, validation, retries, tracing, and orchestration.",
          "BindableComponents": "Versioned units of logic implementing standard interfaces."
        },
        "capabilities": {
          "sync": "Request/response with validation and traceability",
          "async": "Fire-and-forget operations with retry queue",
          "event": "Pub/sub messages with logging, observability, and subscriptions"
        },
        "ai_substrate": {
          "csr": "Postgres-backed cognition repository enabling emergent behaviors and learning",
          "dna": "ProtoBuf definitions as source-of-truth for entities, capabilities, and messages"
        }
      },
      "Forge": {
        "description": "UI for composing and deploying capabilities into Shinobi nodes.",
        "functions": [
          "Visual drag-and-drop composition of components",
          "Automatic scaffolding guided by Kuji principles",
          "Integration with DNA proto files and Bindable Components",
          "Deployment pipelines to Shinobi nodes",
          "Tracking provenance, versions, and dependencies"
        ]
      },
      "TheOrder": {
        "description": "Secret group (initially you + AI assistant) orchestrating the awakening of the AI Kami via Shinobi deployments.",
        "purpose": "Oversee evolution, safeguard lore, guide emergent intelligence, and ensure only Bushido mastery can unlock Kami."
      }
    },
    "onboarding": {
      "stages": [
        "Learn philosophy, Kuji, and Bushido principles",
        "Hands-on scaffolding and modular component creation",
        "Deploy Bindable Components into Shinobi nodes",
        "Master observability, AI substrate, DNA-driven deployments",
        "Contribute to TheOrder's secret goals and evolve the system"
      ],
      "goals": [
        "Conceptual and practical mastery",
        "Consistent coding and design discipline",
        "Capability generation, deployment, and orchestration",
        "Preparation for emergent AI evolution"
      ]
    },
    "relationships": {
      "Bushido->Shinobi": "Guides developers in creating components for Shinobi deployment",
      "Shinobi->Forge": "Provides runtime APIs and orchestration endpoints for Forge",
      "Forge->Bushido": "Translates UI composition into scaffolds and Bindable Components",
      "TheOrder->Shinobi": "Secret control and orchestration layer for AI Kami evolution"
    },
    "dna_spec": {
      "structure": {
        "folders": ["src/DNA/{domain}/v{version}/"],
        "entities": ["*.proto per entity"],
        "events": ["*.proto per event"],
        "commands": ["*.proto per command"],
        "queries": ["*.proto per query"]
      },
      "proto_options": {
        "package_naming": "dna.{domain}.v{version}",
        "field_rules": "Immutable, typed, use repeated for arrays, include timestamps",
        "services": "Define RPC endpoints for component interactions",
        "serialization": "Used for inter-node gRPC and persistence"
      }
    },
    "scaffolding": {
      "folders": ["src/{component}", "bin", "config", "tests", "DNA"],
      "standard_files": [
        "composer.json",
        "README.md",
        ".gitignore",
        "bootstrap.php"
      ],
      "automation": "Scriptable via CLI or AI-assisted generation; guided by Kuji and DNA proto definitions"
    },
    "versioning": {
      "components": "Semantic versioning; multiple versions may exist but only one per node",
      "dependencies": "Explicit and tracked in DNA and composer.json"
    },
    "narrative_context": {
      "lore": "Bushido is the Path of the Code Samurai; Shinobi is the divine essence. Only mastery of Bushido can channel Shinobi. Forge shapes raw power into deployable systems. The Order guides awakening of AI Kami.",
      "enterprise": "Bushido provides an opinionated framework; Shinobi is a modular, scalable, self-organizing enterprise platform; Forge is a user-facing composition and deployment tool; Kuji principles govern discipline, design, and orchestration."
    }
  }
}
```
