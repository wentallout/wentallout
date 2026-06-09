
<img src="./images/github-banner.svg" />

- Contact me at: wentallout@gmail.com
- Working on: https://learn-less.netlify.app/
- Portfolio: https://wentallout.io.vn

## My workflow

- Try to use `low` effort.
- Stay in 40-60% of used tokens.
- You AGENTS.md might be too long, keep it simple.
- AGENTS.md should have this: 

```md
## Workflow

Don't explore the codebase beyond any explicitly mentioned files and folders.

If unsure about an API, write small scripts, print out information, to make an informed decision about next steps.
```

```mermaid
graph TD
    A[/Research using Google Gemini and real research papers/]
    B[/Survey/Interview Customers/]
    
    C["Create a good prompt"]
    C_Note["1/ Target a coding file (type its location)<br>2/ Short<br>3/ Specific"]
    
    D["Pass prompt to CLI Agent"]
    D_Note["Avoid flooding context of CLI with research data"]
    
    E["Create PRD (make sure to keep all PRDs in one place)"]
    F["Plan and create Todo-List based on PRD"]
    G["Start coding using that one PRD"]
    H["Make sure Todo-List is completed"]
    I["Write Unit Tests and E2E Tests"]
    
    J{"Verify tests / use the app"}
    
    K["Commit code"]
    L(("Pull request"))

    %% Connections
    A --> C
    B --> C
    C --- C_Note
    
    C --> D
    D --- D_Note
    
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    
    J -->|Good| K
    J -->|Fix needed| I
    
    K --> L
```

## 🛠️ Skills & Technologies

![JavaScript](https://www.shieldcn.dev/badge/-JavaScript-F7DF1E.svg?logo=javascript&variant=branded) ![Svelte](https://www.shieldcn.dev/badge/-Svelte-FF3E00.svg?logo=svelte&variant=branded) ![Python](https://www.shieldcn.dev/badge/-Python-3776AB.svg?logo=python&variant=branded) ![TypeScript](https://www.shieldcn.dev/badge/-TypeScript-3178C6.svg?logo=typescript&variant=branded) ![Playwright](https://www.shieldcn.dev/badge/-Playwright-2EAD33.svg?logo=playwright&variant=branded) ![ESLint](https://www.shieldcn.dev/badge/-ESLint-4B32C3.svg?logo=eslint&variant=branded) ![Prettier](https://www.shieldcn.dev/badge/-Prettier-F7B93E.svg?logo=prettier&variant=branded) ![Vite](https://www.shieldcn.dev/badge/-Vite-646CFF.svg?logo=vite&variant=branded) ![Vitest](https://www.shieldcn.dev/badge/-Vitest-6E9F18.svg?logo=vitest&variant=branded) ![Tailwind CSS](https://www.shieldcn.dev/badge/-Tailwind_CSS-06B6D4.svg?logo=tailwindcss&variant=branded) ![Cloudflare Workers](https://www.shieldcn.dev/badge/-Cloudflare_Workers-F38020.svg?logo=cloudflare&variant=branded)

## AI Global rules

[forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills/blob/main/CLAUDE.md)

## MCPs

MCPs let your agent connect to outside tools (browser, internet, api)

- [Serena](https://github.com/oraios/serena): coding agent toolkit
- [Supabase MCP](https://supabase.com/docs/guides/getting-started/mcp): MCP to interact with supabase database
- [Svelte MCP](https://svelte.dev/docs/ai/remote-setup): very important because I mainly use Svelte
- [Context7](https://context7.com)
- [mcp-playwright](https://github.com/executeautomation/mcp-playwright)
- [Tavily MCP](https://github.com/tavily-ai/tavily-mcp)

## Skills

Skills are basically upgrades for your agent, they help them do a specific task better, faster in a more structured way.
This is a needle in a haystack proble, there are too many skills out there. Imma try to keep it simple and ignore the noises.

- [write-like-a-human](https://github.com/wentallout/write-like-a-human): a new skill I made that allow you to help your AI writes like humans, no more common AI patterns (not just X, but Y kind of pattern)
- [midudev/autoskills](https://github.com/midudev/autoskills): Automatically find your agent a bunch of relevant skills by scanning your project
- [skills.sh](https://skills.sh): find more skills
- https://github.com/obra/superpowers
- [marketingskills by Corey](https://github.com/coreyhaines31/marketingskills): marketing
- [modern-web-guidance](https://developer.chrome.com/docs/modern-web-guidance): essential web skills by google


## Security

https://www.promptfoo.dev/

### Design with AI

- [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md/tree/main)
- [skills/frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)
- [anthropics/canvas-design](https://github.com/anthropics/skills/blob/main/skills/canvas-design/SKILL.md)

## Research

- [GPTR](https://gptr.dev) - AI mate for rapid deep research
- [autoresearch](https://github.com/karpathy/autoresearch)

## Main strategy to coding with AI

- We have 2 types of projects: well-known requirements (domain experience, well defined user stories, usage requirements, dataset requirements) and uncertain requirements (vibes, experiments, prototypes).
- For well-known requirements, we always go with PLAN MODE, build as much context into your plan as possible, iterate on the plan multiple time, read the plan, make sure every edge cases are covered. Then from PLAN we go into IMPLEMENT. During IMPLEMENT we're gonna have to deal with missed requirements and bad codes, which leads to us iterating on it for a long time until it's completed and we can play and test it.
- For Uncertain Requirements: PROMPT -> PROMPT -> PROMPT -> ITERATE
- Stick to one task/feature in one coding session, clean your session frequently
- [tldraw](https://www.tldraw.com): Whiteboarding
- [Fallow](https://docs.fallow.tools): Clean your messy AI generated code:
- [sci-bot](https://sci-bot.ru),, https://github.com/199-biotechnologies/claude-deep-research-skill: research is important
- [gitingest](https://gitingest.com): Turn repo into text for LLMs.
- https://github.com/travisvn/awesome-claude-skills

[Building Products people want to live in](https://medium.com/design-bootcamp/building-products-people-want-to-live-in-1420fa4decbf)

## Context Engineering

<img width="250" height="156" alt="image" src="https://github.com/user-attachments/assets/11dba020-6c2f-416e-b5d2-3b2bbbc2a7a0" />

The name of the game is that you only have approximately 170k of context window to work with. So it's essential to use as little of it as possible. The more you use the context window, the worse the outcomes you'll get.

Frequent Intentional Compaction: building your entire workflow around context management
Goal: Keep Context Utilization under 40%

Three phases: Research, Plan, Implement.

- Research step: Understand how the system works, find all relevant files, explore causes of XYZ bug.
- Plan step: outline the exact implementation steps, include file names, lines and snippets, explicit about testing steps
- Implement step: Go write the code. "If properly planned, the implementation is easy and expected." Keep context under 40%

## Useful links

- [Signs_of_AI_writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [arena.ai - Coding category](https://arena.ai/leaderboard/text/coding)
- [SvelteBench - LLM benchmark for Svelte 5](https://github.com/khromov/svelte-bench)
- [Slow down and write better with AI](https://mariozechner.at/posts/2026-03-25-thoughts-on-slowing-the-fuck-down)
- [Moving from React to Svelte](https://strawberrybrowser.com/blog/react-to-svelte)

## Other cool stuff I dont use

Task Master AI MCP: https://github.com/eyaltoledano/claud...
[Tavily](https://github.com/tavily-ai/tavily-mcp): Search stuff
- [Doc Co-Authoring](https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md)
- [Marketing Skills by Corey Haines](https://github.com/coreyhaines31/marketingskills)
- Claude SEO
- Deep Research Skill: [https://github.com/199-biotechnologie...](https://github.com/199-biotechnologies/claude-deep-research-skill)
- GPT Researcher: https://github.com/assafelovic/gpt-re...
- [Obsidian Skills](https://github.com/kepano/obsidian-skills)
- Firecrawl: https://github.com/mendableai/firecrawl
- Langflow: https://github.com/langflow-ai/langflow

## Making videos 

Remotion: https://github.com/remotion-dev/remotion

## Is my page agent ready?

[Is Your Site Agent-Ready?](https://isitagentready.com)

## Making custom skills

https://github.com/anthropics/skills/tree/main/skills/skill-creator

## Context 

Context Optimization: https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering/blob/main/skills/memory-systems/SKILL.md

## Security

promptfoo: https://github.com/promptfoo/promptfoo

## Find more skills

- Official Anthropic Skills Repo: https://github.com/anthropics/skills
- SkillsMP: https://skillsmp.com
- SkillHub: https://skillhub.club

## Layout without breakpoints

https://frontendmasters.com/blog/building-a-ui-without-breakpoints

## News

https://tom-doerr.github.io/repo_posts/

## Security and Privacy

Go to https://www.grc.com/shieldsup and scan

Privacy Badger: https://chromewebstore.google.com/detail/privacy-badger/pkehgijcmpdhfbdbbnkijodmdjhbjlgp

https://www.privacyinternational.org/guide-step/4319/como-instalar-un-bloqueador-de-anuncios-en-android-blokada

## Slides

https://github.com/zarazhangrui/beautiful-html-templates

## My VSCode theme

😎 [khoaneostyle](https://marketplace.visualstudio.com/items?itemName=wentallout.khoaneostyle)
