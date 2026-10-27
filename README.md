# STAAD MCP

**AI assistants that read and work with your Bentley STAAD.Pro model.**

STAAD MCP is a free [Model Context Protocol](https://modelcontextprotocol.io) (MCP) server for Bentley STAAD.Pro 20 to 26 (the
2020–2026 releases). Claude, Cursor, VS Code Copilot, Windsurf, Gemini, Codex and other AI assistants use it to work with
the model open in STAAD.Pro, through the STAAD.Pro API. It is one self-contained program: no plug-in inside STAAD.Pro, no .NET to install.

**Download:** [latest release](https://github.com/SHMH-MCPs/staad-mcp-releases/releases/latest) (0.1.0)

## What it does

- **Model discovery:** summary, grids, objects, slabs, mats and footings by property, thickness and material
- **Slabs and foundations:** slab, drop, ribbed, waffle, mat and footing properties; openings; geometry checks
- **Supports and soil:** point, line and area (soil subgrade) spring properties, assignments and a support audit
- **Post-tensioning:** tendon properties; tendons with profile, jacking loads and losses; tendon audit
- **Loads, analysis and results:** patterns, cases, combinations; run analysis; displacements, reactions, deflections
- **Design:** concrete beam design, strip-based slab design results, punching shear, soil pressures, detailing output
- **Database tables:** read, bulk edit and export STAAD.Pro tables (the route for what STAAD.Pro's API cannot change directly)
- **Any other STAAD.Pro API member,** through a typed generic call bound by parameter name
- **28 workflow skills,** served as MCP prompts

Changes can be previewed. Deleting, unlocking results, opening or replacing a model and overwriting files need your
confirmation. Every change is read back and reported as verified or not. Model content stays on your PC, and a read-only
mode is available. Design and analysis output is software output for the engineer's review, not proof of adequacy.

## Supported versions

| STAAD.Pro | Status |
|---|---|
| 23 | Live-verified (23.3.1): self-test 101/104 steps, 97 capabilities; punching shear and detailing not yet verified |
| 20–22, 24–26 | Designed for, not tested |

## Install

1. Download `Install-STAAD.Pro-MCP.cmd` from the [latest release](https://github.com/SHMH-MCPs/staad-mcp-releases/releases/latest) and double-click it
   (it checks the PC, downloads and verifies STAAD MCP, installs it without administrator rights and connects your AI clients).
2. Or by hand: download `staad-mcp-<version>-win-x64.zip`, unzip it to a permanent folder, run `staad-mcp.exe --doctor`, then
   `staad-mcp.exe --setup all`.
3. Restart your AI client, open a model in STAAD.Pro, and ask, for example, "Summarise the open STAAD.Pro model".

STAAD MCP is a product of the SHMH-MCPs family (Revit MCP,
Navisworks MCP, ETABS MCP, SAFE MCP, 3ds Max MCP). STAAD.Pro and OpenSTAAD are trademarks of Bentley Systems, Incorporated; STAAD MCP is not affiliated
with or endorsed by Bentley Systems.
