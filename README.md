# AI Engineering Learning Journey

> A public learning log of a QA automation engineer (10 years, Java/Selenium) moving into AI engineering: prompt engineering, token efficiency, Agent Skills (`SKILL.md`), MCP servers, and AI-powered testing workflows.

## What this repo is

This repo tracks my month-long, 45-minutes-a-day plan to learn how to build practical AI workflows. Everything here is learned by applying it to real QA tasks, such as generating test cases, summarising test reports, formatting bug reports and driving a browser with AI.

If you are a tester or developer who wants to start using AI seriously without a huge time commitment, you can follow the same plan, reuse the prompts and skills, or read my notes.

## What you'll find here

| Folder | Contents |
|---|---|
| `notes/` | Weekly notes: what I learned, what confused me, what worked |
| `prompts/` | A prompt library with before/after versions and token comparisons |
| `skills/` | Custom `SKILL.md` skills I wrote (e.g. test-case writer, bug-report formatter) |
| `mcp/` | Notes and config for connected MCP servers, plus my own MCP server |
| `flows/` | Small AI workflows (chained prompts, tool use) |
| `evals/` | Test cases and pass/fail checks for my AI flows (the QA mindset applied to AI) |

## About me

- QA engineer, 10 years of experience
- Strong in Java, Selenium, Maven, TestNG, Docker, Git
- Beginner in Playwright (JavaScript/TypeScript)
- Goal: build AI flows that remove repetitive work, connect to tools through MCP, write reusable skills, and keep token usage low

## Daily rhythm (45 minutes)

- **10 min:** read or watch one focused resource
- **30 min:** hands-on practice using a real QA task
- **5 min:** write a short note in `notes/` and commit

Mon–Sat are study days. Sunday is rest or a light review.

---

## 1-Month Learning Plan

### Week 1: Prompt engineering and token efficiency

**Goal:** get reliable output on the first try while using fewer tokens.

| Day | Topic | Practice |
|---|---|---|
| 1 | How tokens and context windows work | Count tokens for a few of your usual prompts |
| 2 | Prompt anatomy: role, context, task, constraints, output format | Rewrite 3 real QA prompts |
| 3 | Structure: XML tags, few-shot examples, JSON output | Generate test cases from a user story in a fixed format |
| 4 | Token diet: concise wording, length limits, fresh chat per task, right-sized model | Compare a long and a tight prompt for the same result |
| 5 | First mini-flow | User story → test cases → Selenium/Playwright code |
| 6 | Make it testable | Save prompts in `prompts/`, run each on 5 inputs, note failures |
| 7 | Rest / weekly review | |

### Week 2: Agent Skills and MCP basics

**Goal:** write reusable skills and connect AI to real tools.

| Day | Topic | Practice |
|---|---|---|
| 1 | What a Skill is, and how skills load only when needed | Read the overview, study an existing skill |
| 2 | Write skill #1 (`test-case-writer`) | `SKILL.md` with name, description and instructions |
| 3 | Write skill #2 (`bug-report-formatter`) | Test on 3 inputs; refine the description so it triggers correctly |
| 4 | What MCP is: clients, servers, tools, resources | Read the intro, list what MCP could do for QA |
| 5 | Connect existing MCP servers (Playwright MCP, filesystem, GitHub) | Complete one browser task via MCP |
| 6 | Use MCP for QA | Have the AI explore a site and draft tests; record token usage |
| 7 | Rest / weekly review | |

### Week 3: Build an MCP server and AI flows

**Goal:** build your own tool and chain steps into a flow.

| Day | Topic | Practice |
|---|---|---|
| 1 | MCP server quickstart (TypeScript SDK) | Hello-world tool |
| 2 | Real tool: parse a TestNG/Surefire XML report | Return a clean summary of failures |
| 3 | Second tool and error handling | Test both from an MCP client |
| 4 | Claude API basics: messages, system prompt, `max_tokens` | Make your first API call |
| 5 | Tool use and chaining | Turn a manual QA task into a multi-step flow |
| 6 | Cost control: prompt caching, model choice, usage logging | Log tokens per run in `flows/` |
| 7 | Rest / weekly review | |

### Week 4: Capstone and evals

**Goal:** ship one end-to-end QA agent and prove it works.

| Day | Topic | Practice |
|---|---|---|
| 1 | Design the capstone | Write a one-page spec: user story → tests → run → report |
| 2 | Build part 1 | Test generation using your skill |
| 3 | Build part 2 | Execution/reporting using your MCP server |
| 4 | Integrate | Combine skill + Playwright MCP + your MCP server |
| 5 | Evals | 10 test cases with pass/fail criteria; measure accuracy and tokens |
| 6 | Polish | Clean the repo, update this README, record a short demo |
| 7 | Retro | Write what worked, and plan month 2 |

---

## Progress tracker

- [ ] Week 1: Prompting and token efficiency
- [ ] Week 2: Skills and MCP basics
- [ ] Week 3: MCP server and AI flows
- [ ] Week 4: Capstone and evals

**Start date:** ____ **Target finish:** ____

## Study resources

### Prompt engineering and tokens
- [Anthropic: Prompt engineering overview](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview)
- [Anthropic prompt engineering interactive tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial) (hands-on, free)
- [Anthropic Courses](https://github.com/anthropics/courses)
- [DeepLearning.AI short courses](https://www.deeplearning.ai/short-courses/)

### Agent Skills (`SKILL.md`)
- [Agent Skills overview (Claude docs)](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [Equipping agents for the real world with Agent Skills (Anthropic Engineering)](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)
- [Anthropic open-source skills repo](https://github.com/anthropics/skills): read real examples before writing your own

### MCP (Model Context Protocol)
- [modelcontextprotocol.io](https://modelcontextprotocol.io): official docs and quickstarts
- [Reference MCP servers](https://github.com/modelcontextprotocol/servers)
- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
- [Playwright MCP](https://github.com/microsoft/playwright-mcp)

### Claude API and docs
- [Claude platform docs](https://platform.claude.com/docs): API reference, tool use, prompt caching, token counting

### Playwright (for the TypeScript side)
- [playwright.dev](https://playwright.dev)

## Notes on using this repo

- Commit daily, even if it is just a note. The commit history is the proof of progress.
- Use real QA tasks for practice. It sticks better than toy examples.
- If a week runs over, repeat it rather than rushing.

## License

MIT, so feel free to reuse prompts and skills.
