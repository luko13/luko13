<h1 align="center">Luis Santiago Chillón Serratosa</h1>

<p align="center">
  <strong>Frontend / Product Engineer</strong><br/>
  React · TypeScript · Next.js · React Native
</p>

<p align="center">
  <a href="https://luko13.vercel.app/?lang=en">Portfolio</a>
  ·
  <a href="https://www.linkedin.com/in/luis-chill%C3%B3n-serratosa-00735486/">LinkedIn</a>
  ·
  <a href="mailto:luislk1996chs@gmail.com">Email</a>
</p>

---

## About me

I build web and mobile products end to end, with a strong focus on **frontend architecture, system design and engineering quality**.

My core stack is **React, TypeScript, Next.js and React Native / Expo**, complemented by PostgreSQL, SQLite and Node.js when the product requires ownership beyond the UI.

I work hands-on across architecture, implementation, testing, CI/CD, observability and production support.

My engineering experience includes:

- Frontend system design
- Modular architectures
- Microfrontend architecture
- TDD using Red-Green-Refactor
- SOLID principles
- Software design patterns
- Architecture Decision Records (ADRs)
- Monorepos and shared TypeScript domain layers
- Offline-first systems
- Data synchronization and conflict handling
- CI/CD and automated quality gates

Across my main products I maintain **160+ automated test suites**, together with integration checks and CI pipelines covering type safety, linting, testing and production builds.

---

## Selected engineering work

### [`expo-sqlite-offline-sync`](https://github.com/luko13/expo-sqlite-offline-sync)

**Inspectable offline-first architecture for React Native + SQLite.**

A reference implementation focused on the hard parts of offline synchronization rather than UI complexity.

**Architecture concepts demonstrated:**

- SQLite-first local state
- Atomic domain + outbox writes
- Durable Outbox Pattern
- At-least-once delivery
- Idempotent push operations
- Incremental pull with cursors
- Explicit conflict resolution
- Exponential retry with full jitter
- Deterministic testing
- Injectable infrastructure boundaries
- Database migrations
- Real SQLite integration tests

```text
React Native UI
       │
       ▼
Local Repository
       │
       ▼
     SQLite
   ┌────┼─────┐
 Domain Outbox Sync State
       │
       ▼
   Sync Engine
       │
       ▼
    Transport
       │
       ▼
      API
