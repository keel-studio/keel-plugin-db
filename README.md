# keel plugin: Database

Connect a database. You see its tables and an ER diagram. Agents get read-only SQL tools.

> **Status: planned.** The code still lives in [keel-v2](https://github.com/MiladNalbandi/keel-v2). It moves here step by step, as
> [the plugin plan](https://github.com/MiladNalbandi/keel-v2/tree/main/docs/plugins) says. There is nothing to install yet.

| | |
| --- | --- |
| id | `db` |
| needs | keel core (plugin SDK 1), Code |
| works with | Map |
| parts | engine · api · web · content · migrations |
| trust level | runs code in keel |

**What it adds to keel**

- Code › Database tab
- Database connections
- `db:*` actions
- `keel-db` tools for agents
- the ER tab in Map (when Map is installed)

**Where the code is today (keel-v2)**

- `engine/keel_engine/plugins/db`
- `keel.api.plugins.Database` (api)
- `web/src/components/plugins/DbTool.tsx`
- `content/plugins/db`

## Layout

```
keel-plugin.yml   the manifest
engine/           Python package for keel's engine
api/              Kotlin, a thin Spring Boot jar
web/              React pages and slots (an ES module)
content/          workflows, agents, skills, commands
migrations/       its own database tables (own Flyway history)
```

## Install

When it is released: in keel, **Control › Plugins › Marketplace › Database › Install**. keel checks the file's
signature, shows what the plugin may do, and asks you before it installs.

## License

MIT
