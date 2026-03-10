# Olix Usage: How to Use Skills in Your Projects

Welcome to the **Olix AI Skill Library**! This repository is designed as a centralized "Master Library" for AI agent instructions and skills. 

Rather than including every skill in every project (which would overwhelm the AI's context window), we recommend using the **"Pick and Move" Strategy**.

## The "Pick and Move" Strategy

When starting or updating a project, you should manually copy *only the specific skills you need* from this Master Library into your project's local AI instruction directory.

Both Antigravity and Cursor typically look for a `.agent/skills`, `.agent`, or `.cursor/rules` folder in the root of your project.

### Basic Workflow

1. **Identify the project requirements.** (e.g., "This is a Next.js frontend with a Node.js backend").
2. **Create the local skills directory** in your project root:
   ```bash
   mkdir -p ./MyProject/.agent/skills
   ```
3. **Copy the relevant skills** from your Master Library to the project directory.

Below are some common "Bundle" examples to help you quickly assemble the right set of skills for different types of projects.

---

## Example Skill Bundles

### 1. The Frontend Web Bundle
Use this bundle when working on a modern UI projects. It ensures the AI follows best practices for UI, state management, and styling.

```bash
# Create the local folder
mkdir -p ./.agent/skills

# Copy frontend-specific skills
cp ~/Documents/AI-Skill-Library/skills/react-best-practices/SKILL.md ./.agent/skills/react-best-practices.md
cp ~/Documents/AI-Skill-Library/skills/tailwind-patterns/SKILL.md ./.agent/skills/tailwind-patterns.md
cp ~/Documents/AI-Skill-Library/skills/frontend-dev-guidelines/SKILL.md ./.agent/skills/frontend-guidelines.md
cp ~/Documents/AI-Skill-Library/skills/typescript-expert/SKILL.md ./.agent/skills/ts-expert.md
```

### 2. The Backend API Bundle
Ideal for Node.js backend services, microservices, or API development. It provides guidelines on architecture, database design, and API security.

```bash
# Create the local folder
mkdir -p ./.agent/skills

# Copy backend-specific skills
cp ~/Documents/AI-Skill-Library/skills/nodejs-backend-patterns/SKILL.md ./.agent/skills/nodejs-backend.md
cp ~/Documents/AI-Skill-Library/skills/api-design-principles/SKILL.md ./.agent/skills/api-design.md
cp ~/Documents/AI-Skill-Library/skills/database-design/SKILL.md ./.agent/skills/database-design.md
cp ~/Documents/AI-Skill-Library/skills/api-security-best-practices/SKILL.md ./.agent/skills/api-security.md
```

### 3. The Full-Stack "Makers" Bundle
For solo developers or small teams building full-stack applications quickly. This combines frontend patterns with backend principles and deployment basics.

```bash
# Create the local folder
mkdir -p ./.agent/skills

# Copy full-stack skills
cp ~/Documents/AI-Skill-Library/skills/nextjs-app-router-patterns/SKILL.md ./.agent/skills/nextjs-app-router.md
cp ~/Documents/AI-Skill-Library/skills/drizzle-orm-expert/SKILL.md ./.agent/skills/drizzle-orm.md
cp ~/Documents/AI-Skill-Library/skills/vercel-deployment/SKILL.md ./.agent/skills/vercel-deploy.md
cp ~/Documents/AI-Skill-Library/skills/clean-code/SKILL.md ./.agent/skills/clean-code.md
```

### 4. The AI Agent Development Bundle
When building your own AI agents, LLM wrappers, or RAG chains, use this bundle to ensure your prompt engineering and orchestration are top-notch.

```bash
# Create the local folder
mkdir -p ./.agent/skills

# Copy AI-specific skills
cp ~/Documents/AI-Skill-Library/skills/ai-agent-development/SKILL.md ./.agent/skills/ai-agent-dev.md
cp ~/Documents/AI-Skill-Library/skills/prompt-engineering-patterns/SKILL.md ./.agent/skills/prompt-engineering.md
cp ~/Documents/AI-Skill-Library/skills/langgraph/SKILL.md ./.agent/skills/langgraph.md
cp ~/Documents/AI-Skill-Library/skills/llm-evaluation/SKILL.md ./.agent/skills/llm-eval.md
```

### 5. The DevOps & Security Audit Bundle
If your current focus is on securing an application, building CI/CD pipelines, or auditing code, load up these specialized skills.

```bash
# Create the local folder
mkdir -p ./.agent/skills

# Copy DevOps and Security skills
cp ~/Documents/AI-Skill-Library/skills/security-audit/SKILL.md ./.agent/skills/security-audit.md
cp ~/Documents/AI-Skill-Library/skills/docker-expert/SKILL.md ./.agent/skills/docker-expert.md
cp ~/Documents/AI-Skill-Library/skills/github-actions-templates/SKILL.md ./.agent/skills/github-actions.md
cp ~/Documents/AI-Skill-Library/skills/aws-serverless/SKILL.md ./.agent/skills/aws-serverless.md
```

---

## Best Practices

1. **Keep it lean:** Do not copy 50 skills into a single project. The more instructions you give the AI, the more likely it is to get confused or drop important context. Aim for 3-7 core skills per project.
2. **Rename on copy:** As shown in the examples above, it is often helpful to rename `SKILL.md` to something descriptive (like `react-best-practices.md`) so you know exactly what is in your `.agent/skills` folder.
3. **Commit local skills:** Commit your local `.agent/skills` or `.cursor/rules` to your project's repository. This way, any other developer (or AI) picking up the repository instantly has the correct operational context.
4. **Update periodically:** If the Master Library receives updates, remember to re-copy the updated `SKILL.md` files into your active projects.
