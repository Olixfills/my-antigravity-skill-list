---
name: brand-identity
category: olix
description: Asks the user questions about their brand and generates a localized brand identity skill in their project. Use when the user wants to enforce UI consistency, voice/tone, or brand guidelines.
---

# Brand Identity Scaffolder

## When to use this skill
- The user acts to configure a brand identity for a new or existing project.
- The user wants consistent styling, voice, or design tokens mapped to their application framework.

## Workflow

### 1. Plan & Gather Requirements
Before generating any files, you MUST ask the user the following questions to understand their brand:
1. **Brand Details**: What is the name of the brand/project, and what is its core mission?
2. **Design Tokens**: What are the primary and secondary brand colors (hex codes)? What is the primary font family?
3. **Tech Stack**: Are there any specific frameworks (e.g., React, Tailwind, shadcn/ui) that the design system should align with?
4. **Voice & Tone**: How should the application address users? (e.g., formal, playful, technical, concise)?

**STOP and wait** for the user's responses before proceeding to Step 2.

### 2. Scaffold the Local Skill
Once the user provides the information, map their answers to a new local skill inside their project's `.agent/skills/brand-identity/` directory.

Copy the template files from this global skill's `resources/` directory and replace the placeholders with the gathered information:
- `resources/design-tokens.json` -> `.agent/skills/brand-identity/resources/design-tokens.json`
- `resources/tech-stack.md` -> `.agent/skills/brand-identity/resources/tech-stack.md`
- `resources/voice-tone.md` -> `.agent/skills/brand-identity/resources/voice-tone.md`

Finally, generate the local `SKILL.md` (named e.g., `applying-brand-identity`) that tells the agent to always check these local `resources/` when asked to implement UI or write copy for the project.

### 3. Validation & Review
Notify the user of the generated files and ask them to verify and fine-tune the local configurations.

## Instructions
- Replace `[INSERT BRAND NAME]` and similar placeholders with the user's actual answers.
- Do not make assumptions for colors or fonts—if the user omits them, provide sensible modern defaults but let them know you did so.
- Make the local `SKILL.md` highly constrained, instructing the local agent to never deviate from the defined colors or voice standards.

## Resources
- [design-tokens.json](resources/design-tokens.json): Template for colors, typography, border radii.
- [tech-stack.md](resources/tech-stack.md): Template for UI component implementation rules.
- [voice-tone.md](resources/voice-tone.md): Template for copywriting persona and terminology.
