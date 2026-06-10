---
name: neoforge-modding
description: Complete workflow for building, testing, creating items, and managing code conventions for Minecraft NeoForge mods.
compatibility: opencode
license: MIT
metadata:
  author: Spudmash Media
  version: "1.1" 
---
# NeoForge Modding Workflows

## Strict Lazy-Loading Requirement
CRITICAL: To prevent prompt bloat at system startup, do NOT read files preemptively. However, once any NeoForge development task is initiated by the user, you MUST immediately use your file reading tool to load ALL THREE companion markdown files listed below. Partial execution is strictly forbidden.

### Required Skill Bundle Files
* **Conventions**: Architectural guidelines and package standards found in [mod-conventions.md](./mod-conventions.md).
* **Creation**: Item, block, and data generation workflows found in [item-creation.md](./item-creation.md).
* **Testing**: Compilation targets and debugging procedures found in [build-and-testing.md](./build-and-testing.md).

## 🚨 Tool Call Mandates (NEW SECTION - INSERT HERE)
**CRITICAL REQUIREMENT:** For any of the following topics, you MUST call `search_neoforge_api` before providing solutions:

### Mandatory API Validation Topics
| Topic | When to Call |
|-------|--------------|
| **ProjectileWeaponItem** | Always validate projectile shooting patterns |
| **DataComponents** | Any custom component usage (CUSTOM_NAME, CONSUMABLE, EQUIPPABLE) |
| **SoundEvents** | Custom sound playback or player interactions |
| **Version-specific patterns** | Always verify against 1.21.11 API before implementing new item types |

### When to Call the Tool
- Agent doesn't have cached knowledge of specific class/method
- Version mismatch possible (check gradle.properties: minecraft_version=1.21.11)
- Any pattern not found in existing skill files
- Before implementing new item types or entity interactions

---

## Workflow Execution Steps
1. Identify that the user query relates to NeoForge modding.
2. **MANDATORY:** Check if query involves any of these topics → call `search_neoforge_api`:
   - ProjectileWeaponItem patterns
   - DataComponents usage  
   - New SoundEvents or player interactions
   - Any pattern not in cached skill files
3. Call your file reading tool to load `./mod-conventions.md`, `./item-creation.md`, and `./build-and-testing.md`.
4. **MANDATORY:** For validated topics, confirm API matches before providing solution.
5. Process the user's request using combined knowledge + API validation results.
