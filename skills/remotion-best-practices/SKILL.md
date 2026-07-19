---
name: remotion-best-practices
description: Best practices for Remotion
metadata:
  tags: remotion, video, react, animation, composition
---

## New project setup

If no Remotion project currently exists, load [Create a new Remotion project](remotion-create/REFERENCE.md)

## React Markup Best Practices

If you are writing Remotion React Markup, load [Remotion Markup Best Practices](remotion-markup/REFERENCE.md)

## Mediabunny Skills

For achieving multimedia tasks in the browser, such as trimming, cropping videos, or getting metadata from them, load [Mediabunny Best Practices](mediabunny/REFERENCE.md)

## Improving Interactivity

By structuring the Remotion markup well, we can allow users to interactively change things in the Studio and write back to code. If relevant: [Interactivity Best Practices](remotion-interactivity/REFERENCE.md)

## Rendering

For advanced rendering beyond simple `npx remotion render`, see: [Rendering Best Practices](remotion-render/REFERENCE.md)

## Captions

When working with Captions, load [Remotion Captions](remotion-captions/REFERENCE.md).

## Creating a SaaS, automation or application

Use the [Remotion SaaS skill](remotion-saas/REFERENCE.md) for knowledge about Remotion-powered SaaS apps, such as `<Player>`, rendering on Lambda, Vercel, Cloudflare, via Express.js, client-side rendering, or for finding the right SaaS template.

## Looking up Remotion APIs and documentation

To find and read current Remotion documentation, load [Remotion Docs](remotion-docs/REFERENCE.md).


## Codex troubleshooting

When running inside Codex, first try starting the Remotion Studio normally:

```bash
npx remotion studio
```

Only if that fails with file watcher limits such as `EMFILE: too many open files, watch`, retry with polling and without opening a browser from Codex:

```bash
npx remotion studio --no-open --webpack-poll 1000
```

If Studio still fails to start from Codex, ask the user to start it manually from their macOS Terminal and then continue using the already-running Studio. Sandbox errors while launching Chromium from Codex are likely caused by the Codex/macOS sandbox rather than the Remotion project.
