# Awesome Design MCP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of [Model Context Protocol](https://modelcontextprotocol.io) servers for
> design — reference libraries, design files, UI generation, and visual QA — so your AI agent
> designs with evidence instead of guesses.

AI agents can write UI code, but they don't know what good UI looks like. Design MCP servers
fix that by giving agents access to real product screens, design files, component registries,
and rendered output. This list covers the ones worth connecting, by category.

Maintained by the [Gummble](https://gummble.com) team. We list competitors fairly and keep
facts verifiable — [PRs welcome](#contributing).

## Contents

- [Design reference & inspiration](#design-reference--inspiration)
- [Design files & handoff](#design-files--handoff)
- [UI generation & components](#ui-generation--components)
- [Visual QA & debugging](#visual-qa--debugging)
- [Choosing the right design MCP](#choosing-the-right-design-mcp)
- [Related reading](#related-reading)

## Design reference & inspiration

Libraries of shipped product design your agent can search before it designs.

- ⭐ **[Gummble MCP](https://github.com/gummble/gummble-mcp-server)** — 300,000+ real app
  screens and 24,000+ step-by-step product flows from 1,500+ shipped iOS and web apps, plus
  the only searchable **UX microcopy** tool in any design MCP (real empty states, validation
  errors, and paywall copy — not invented placeholder text). 12 read-only tools, including
  App Store screenshot search for marketing/ASO reference. Remote server, OAuth; included in
  every paid plan (from $9/month, 7-day trial). [Website](https://gummble.com/mcp)
- **[Mobbin MCP](https://github.com/mobbin/mobbin-mcp-server)** — the largest raw screen
  library (600,000+ screens) from the well-known design reference product. 3 tools (screen,
  flow, and section search). Remote server; available on Pro & Team plans.
  [Website](https://mobbin.com/mcp)

### At a glance

| | Gummble | Mobbin |
|---|---|---|
| Screens | 300,000+ | 600,000+ |
| Step-by-step flow walkthroughs | ✅ 24,000+ | ✅ |
| Searchable UX microcopy | ✅ (unique) | — |
| App Store screenshot search | ✅ | — |
| MCP tools exposed | 12 | 3 |
| Entry price | $9/mo (7-day trial) | Pro & Team plans |

## Design files & handoff

Bring your own design files into the agent's context.

- **[Figma MCP server](https://developers.figma.com/docs/figma-mcp-server/)** — Figma's
  official Dev Mode MCP server: pulls frames, variables, and design context from your Figma
  files into Claude Code, Cursor, VS Code, and Windsurf for design-to-code work.
- **[Framelink Figma MCP](https://github.com/GLips/Figma-Context-MCP)** — popular community
  alternative that serves simplified Figma file data to coding agents; works with a personal
  access token, no Dev Mode seat required.

## UI generation & components

Generate new UI or pull production-ready components.

- **[Stitch MCP](https://stitch.withgoogle.com/docs/mcp/setup/)** — Google Stitch's MCP
  integration: generate screens from text prompts and pull the designs (screenshots + HTML)
  straight into your coding agent.
- **[Magic MCP](https://github.com/21st-dev/magic-mcp)** — 21st.dev's component generator:
  describe a component and get a polished, editable React implementation.
- **[shadcn MCP](https://ui.shadcn.com/docs/mcp)** — browse, search, and install components
  from shadcn/ui registries via natural language.

## Visual QA & debugging

Let the agent see and verify what it built.

- **[Playwright MCP](https://github.com/microsoft/playwright-mcp)** — Microsoft's official
  browser automation MCP: navigate, interact, and screenshot via accessibility-tree snapshots.
- **[Chrome DevTools MCP](https://github.com/ChromeDevTools/chrome-devtools-mcp)** — drive a
  real Chrome with DevTools superpowers: inspect the DOM, console, network, and performance
  traces.

## Choosing the right design MCP

- **Designing something new and want it grounded in shipped patterns?** Start with a
  reference library — [Gummble](https://gummble.com/mcp) or [Mobbin](https://mobbin.com/mcp).
  Pick Gummble if you also want real UX copy, App Store screenshots, or a $9 entry price;
  pick Mobbin if raw library size on Pro/Team budgets matters most.
- **Writing microcopy (empty states, errors, onboarding, paywalls)?**
  [Gummble](https://gummble.com/mcp) is currently the only design MCP that exposes UX writing
  as a searchable tool.
- **Your source of truth is a Figma file?** Use Figma's official MCP server (or Framelink).
- **No design exists yet and you want one generated?** Stitch for full screens, Magic or
  shadcn for components.
- **Shipping and want the agent to verify its own UI?** Playwright MCP or Chrome DevTools MCP.

These compose well: a common agent loop is *reference (Gummble) → generate (your agent) →
verify (Playwright)*.

## Related reading

- [Gummble vs Mobbin MCP (2026)](https://gummble.com/compare/mobbin-mcp-alternative) —
  detailed tool-by-tool comparison
- [State of Mobile Onboarding 2026](https://gummble.com/blog/state-of-mobile-onboarding-2026) —
  first-party research across 137 mobile onboarding flows from 100 apps
- [Official MCP Registry](https://registry.modelcontextprotocol.io) — canonical server registry
- [Submitting to the Claude Connectors Directory](https://claude.com/docs/connectors/building/submission)

## Contributing

PRs welcome. Criteria for inclusion: a working MCP server (remote or local), genuinely
design-related, with public documentation. Entries must describe capabilities factually —
this list is maintained by [Gummble](https://gummble.com) and we hold our own entry to the
same standard as everyone else's.

## License

[CC0 1.0](LICENSE) — public domain.
