# Continue + VS Code — AI Coding with Local & Cloud LLMs

A practical guide for using **Continue** inside VS Code with:

- 🖥️ Local LLMs through **Ollama**

- 🆓 Free/open-weight models

- ☁️ Paid cloud models

- 🔑 BYOK (Bring Your Own Key)

- 🤖 Agentic coding

- 💬 AI chat and codebase analysis

- ⚡ Autocomplete

- 🔒 Private/local development

The goal is to build a flexible AI coding environment without being locked into a single AI provider.

### Ressources

- [Ollama + Continue + VS Code: Coder avec des modèles locaux - YouTube](https://www.youtube.com/watch?v=BW7veVBWpZw&t=90s) 

---

## Table of Contents

- [1. What is Continue?](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#1-what-is-continue)

- [2. Why Continue?](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#2-why-continue)

- [3. Architecture](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#3-architecture)

- [4. Installation](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#4-installation)

- [5. Using Ollama](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#5-using-ollama)

- [6. Choosing a Local Model](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#6-choosing-a-local-model)

- [7. Using Cloud Models](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#7-using-cloud-models)

- [8. Free vs Open-Weight vs Paid Models](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#8-free-vs-open-weight-vs-paid-models)

- [9. Recommended Model Strategy](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#9-recommended-model-strategy)

- [10. Continue Configuration](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#10-continue-configuration)

- [11. Chat](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#11-chat)

- [12. Autocomplete](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#12-autocomplete)

- [13. Agent Mode](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#13-agent-mode)

- [14. Codebase Context](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#14-codebase-context)

- [15. Rules and Instructions](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#15-rules-and-instructions)

- [16. Recommended Setup for Software Engineers](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#16-recommended-setup-for-software-engineers)

- [17. Local-Only Development](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#17-local-only-development)

- [18. Hybrid Local + Cloud Development](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#18-hybrid-local--cloud-development)

- [19. Troubleshooting](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#19-troubleshooting)

- [20. Security](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#20-security)

- [21. Example Workflow](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#21-example-workflow)

- [22. Conclusion](https://chatgpt.com/c/6ab6b79b-f80c-83ea-816f-df1930e94ab4#22-conclusion)

---

# 1. What is Continue?

**Continue** is an open-source AI coding assistant that integrates with development environments such as VS Code.

Instead of forcing you to use a single AI provider, Continue allows you to connect different models.

For example:

```text
VS Code
   │
   ▼
Continue
   │
   ├── Ollama
   │     └── Local LLM
   │
   ├── OpenAI-compatible API
   │
   ├── Anthropic
   │
   ├── Google
   │
   └── Other providers
```

This means you can choose the model according to:

- cost

- speed

- privacy

- coding performance

- hardware

- reasoning capability

- context size

---

# 2. Why Continue?

A traditional AI coding setup might look like:

```text
VS Code
   │
   ▼
AI Extension
   │
   ▼
One Provider
```

Continue allows:

```text
                         ┌── Local Ollama
                         │
VS Code → Continue ──────┼── Free APIs
                         │
                         ├── Open-weight models
                         │
                         ├── Paid APIs
                         │
                         └── Multiple providers
```

This gives you more control.

### Main advantages

- Open-source

- BYOK

- Local model support

- Cloud model support

- Multiple providers

- Model switching

- Codebase context

- Chat

- Autocomplete

- Agent workflows

- Custom instructions

- Flexible architecture

---

# 3. Architecture

A typical setup can look like this:

```text
┌──────────────────────────────┐
│           VS Code            │
│                              │
│  ┌────────────────────────┐  │
│  │       Continue         │  │
│  └───────────┬────────────┘  │
└──────────────┼───────────────┘
               │
       ┌───────┴────────┐
       │                │
       ▼                ▼
   Local Models      Cloud Models
       │                │
       ▼                ▼
    Ollama          API Provider
       │                │
       ▼                ▼
  Local Machine      Internet
```

You can therefore use:

```text
Private/simple task
       ↓
Local Ollama model

Complex task
       ↓
Cloud reasoning model
```

---

# 4. Installation

## 4.1 Install VS Code

Install Visual Studio Code for your operating system.

Then open the Extensions marketplace.

Search for:

```text
Continue
```

Install the official Continue extension.

---

# 5. Using Ollama

## 5.1 What is Ollama?

**Ollama** makes it easy to run LLMs locally.

Instead of sending your code to an external API:

```text
VS Code
   ↓
Continue
   ↓
Ollama
   ↓
Local LLM
```

The model runs on your own computer.

This can be useful for:

- confidential code

- offline development

- experimentation

- avoiding API costs

- learning about local AI

---

## 5.2 Install Ollama

On Linux, install Ollama using its official installation method.

After installation, verify:

```bash
ollama --version
```

Then verify that the service is running:

```bash
ollama list
```

---

## 5.3 Download a model

For example:

```bash
ollama pull qwen2.5-coder
```

or another coding model supported by Ollama.

List installed models:

```bash
ollama list
```

You can then test a model:

```bash
ollama run qwen2.5-coder
```

---

# 6. Choosing a Local Model

The model you choose depends heavily on your hardware.

A useful rule is:

```text
More RAM/VRAM
      ↓
Larger model
      ↓
Usually better capability
      ↓
But slower / more resource intensive
```

### Typical categories

| Model size | Hardware requirement | Typical use               |
| ---------- | -------------------- | ------------------------- |
| 1–4B       | Low                  | Simple autocomplete/tasks |
| 7–8B       | Moderate             | General coding            |
| 14B        | Higher               | Better coding/reasoning   |
| 30B+       | High                 | Advanced local workloads  |
| 70B+       | Very high            | Serious local inference   |

Quantized versions can significantly reduce memory requirements.

For example:

```text
FP16 model
    ↓
Large memory requirement

Quantized model
    ↓
Lower memory requirement
    ↓
Can run on smaller hardware
```

---

# 7. Using Cloud Models

Local models aren't always the best choice.

For difficult tasks, you may want a cloud model.

Examples of providers include:

- OpenAI

- Anthropic

- Google

- Mistral

- OpenRouter

- Together AI

- Groq

- Fireworks

- Other OpenAI-compatible providers

The exact models and pricing change frequently, so check the provider's current documentation before choosing one.

The architecture becomes:

```text
VS Code
   ↓
Continue
   ↓
Cloud API
   ↓
LLM
```

You provide your API key and configure the model in Continue.

---

# 8. Free vs Open-Weight vs Paid Models

These terms are important.

## Free model

"Free" generally means that you can use the model/service without paying directly.

However, the provider may impose:

- rate limits

- usage limits

- context limits

- slower inference

- availability restrictions

---

## Open-weight model

An open-weight model provides downloadable model weights that can potentially be run yourself, subject to its license.

Examples of model families commonly available in open-weight form include:

- Qwen

- Llama

- Mistral

- DeepSeek

- Gemma

**Open-weight does not automatically mean unrestricted or completely free.**

Always check the model's license.

---

## Paid API model

You send requests to a provider and pay according to its pricing model.

Advantages:

- no local GPU required

- powerful models

- easy setup

- potentially larger context

- faster than local inference on modest hardware

Disadvantages:

- recurring usage cost

- code/data leaves your machine

- requires internet

- provider limits/policies apply

---

# 10. Continue Configuration

Continue's configuration format and UI can change between releases, so use the configuration generated by your installed version as the source of truth.

Conceptually, you want something like:

```yaml
name: Main Config
version: 1.0.0
schema: v1
models:
  - name: Qwen
    provider: Ollama
    model: qwen2.5-coder:7b
    apiBase: http://192.168.0.39:11434
    roles:
      - chat
      - edit
      - apply
  - name: Autodetect
    provider: ollama
    model: AUTODETECT
```

```yaml
models:
  - name: Local Coding Model
    provider: ollama
    model: your-local-coding-model

  - name: Cloud Coding Model
    provider: your-provider
    model: your-cloud-model

  - name: Fast Model
    provider: another-provider
    model: your-fast-model
```

The important concept is:

```text
name
provider
model
```

Continue then lets you select the appropriate model for your task.

---

# 11. Chat

Continue can be used as an AI chat interface directly inside VS Code.

Example:

```text
Explain how authentication works in this Spring Boot project.
```

The model can use relevant project context.

You can ask:

```text
Explain this service.
```

```text
Find potential problems in this authentication flow.
```

```text
Generate unit tests for this class.
```

```text
Refactor this method without changing its behavior.
```

---

# 12. Autocomplete

Autocomplete is different from agentic coding.

Autocomplete is:

```text
You type:

public class UserService {

    public User findById(Long id) {

        ...
```

The model predicts what comes next.

This requires:

- low latency

- small/optimized models

- frequent requests

Therefore, a smaller model is often preferable for autocomplete.

---

# 13. Agent Mode

Agent mode is for larger tasks.

Instead of:

```text
Generate this function.
```

you can give a task such as:

```text
Implement user authentication.

Requirements:
- Spring Boot
- JWT
- PostgreSQL
- Angular frontend
- role-based authorization
- tests
```

The agent may:

```text
1. Inspect project
       ↓
2. Understand architecture
       ↓
3. Create a plan
       ↓
4. Modify files
       ↓
5. Run commands
       ↓
6. Run tests
       ↓
7. Fix errors
       ↓
8. Explain changes
```

Agent mode should still be supervised.

Never blindly accept changes to a production repository.

---

# 14. Codebase Context

One of the most important features of an AI coding assistant is context.

A good workflow is:

```text
Question
   ↓
Relevant files
   ↓
Project architecture
   ↓
Dependencies
   ↓
Existing conventions
   ↓
LLM
```

Instead of asking:

```text
Create a login endpoint.
```

provide context such as:

```text
Analyze the existing authentication architecture
and implement login following the project's
existing conventions.
```

This reduces the chance of generating code that conflicts with the existing architecture.

---

# 15. Rules and Instructions

You can define project-specific instructions.

For example:

```text
# Project Rules

## Backend

- Spring Boot 3.x
- Java 21
- REST API
- Use DTOs
- Use Bean Validation
- Use constructor injection
- Do not expose entities directly

## Frontend

- Angular
- Standalone components
- Signals where appropriate
- Reactive forms
- Follow existing project conventions

## Database

- PostgreSQL
- Use migrations
- Never modify production data directly

## Security

- Never hard-code credentials
- Never expose secrets
- Validate all external input
```

This gives the AI a consistent development context.

---

# 16. Recommended Setup for Software Engineers

For a developer working with:

```text
Angular
Spring Boot
Laravel
PostgreSQL / SQL Server
Linux
Docker
Git
```

a useful setup is:

```text
                    VS Code
                       │
                    Continue
                       │
       ┌───────────────┼────────────────┐
       │               │                │
       ▼               ▼                ▼
   Autocomplete       Chat             Agent
       │               │                │
       ▼               ▼                ▼
 Fast local/API     Medium model     Powerful model
       │               │                │
       └───────────────┼────────────────┘
                       │
                 Your projects
                       │
              ┌────────┼────────┐
              ▼        ▼        ▼
           Angular  Spring    Laravel
```

---

# 17. Local-Only Development

If your code is confidential, you can use:

```text
VS Code
   ↓
Continue
   ↓
Ollama
   ↓
Local model
```

No external AI API is required.

Example:

```bash
ollama list
```

Then configure Continue to use the local model.

### Advantages

- Code stays on your machine

- No API bill

- Can work without internet

- Full control over the model

### Disadvantages

- Requires sufficient hardware

- Local models may be weaker than the strongest cloud models

- Large models require significant RAM/VRAM

- Inference can be slower

---

# 18. Hybrid Local + Cloud Development

For many developers, a hybrid approach is practical:

```text
                    Continue
                       │
        ┌──────────────┴──────────────┐
        │                             │
        ▼                             ▼
     Ollama                       Cloud API
        │                             │
        ▼                             ▼
   Local model                 Powerful model
        │                             │
        ▼                             ▼
Simple/private tasks           Complex tasks
```

Example:

### Local

```text
Explain this class.
Generate getters/setters.
Create a simple DTO.
Generate boilerplate.
Autocomplete.
```

### Cloud

```text
Analyze this architecture.
Refactor this entire module.
Investigate a difficult bug.
Design a complex feature.
Review a large codebase.
```

This lets you balance:

```text
Privacy
Cost
Speed
Capability
```

---

# 19. Troubleshooting

## Ollama isn't detected

Check:

```bash
ollama list
```

Then:

```bash
ollama ps
```

You can also test:

```bash
ollama run <model>
```

If the model works from the terminal but not from Continue, check:

- Continue configuration

- Ollama endpoint

- model name

- VS Code logs

- Continue logs

---

## Model is too slow

Try:

```text
Smaller model
```

or:

```text
More aggressive quantization
```

or use a cloud model.

Also check whether the model is actually using your GPU.

---

## Model produces poor code

Try:

1. A newer coding model.

2. A larger model.

3. Better project context.

4. Better project rules.

5. A stronger cloud model.

Don't assume that increasing the prompt length will solve everything.

---

# 20. Security

AI coding tools can access source code, terminals, files, and potentially other project resources depending on how they are configured.

Treat an AI agent similarly to a developer with significant access.

## Never put secrets in prompts

Avoid:

```text
API_KEY=xxxxxxxx
PASSWORD=xxxxxxxx
JWT_SECRET=xxxxxxxx
```

Instead:

```text
Use the existing environment variable.
```

---

## Use environment variables

Example:

```env
DATABASE_URL=...
DATABASE_USERNAME=...
DATABASE_PASSWORD=...
JWT_SECRET=...
```

Do not commit secrets.

Use:

```gitignore
.env
.env.*
```

when appropriate for your project.

---

## Review agent actions

For agentic workflows:

```text
AI proposes change
       ↓
You inspect
       ↓
Run tests
       ↓
Review Git diff
       ↓
Commit
```

Do not treat generated code as automatically correct.

---

# 21. Example Workflow

Imagine you have:

```text
my-project/
├── backend/
│   └── Spring Boot
│
├── frontend/
│   └── Angular
│
├── database/
│
└── docs/
```

You ask:

```text
I need to add a notification system.

Before modifying anything:

1. Analyze the existing architecture.
2. Identify where notifications should live.
3. Identify relevant backend entities and services.
4. Identify the Angular components involved.
5. Propose an implementation plan.
6. Do not modify files yet.
```

The AI analyzes the repository.

Then:

```text
Implement the approved plan.

Requirements:
- Keep the existing architecture.
- Follow existing naming conventions.
- Add tests.
- Do not introduce unnecessary dependencies.
- Do not modify unrelated files.
```

After implementation:

```text
Review the changes.

Check:
- security
- validation
- error handling
- tests
- performance
- unnecessary changes
```

Then:

```bash
git diff
```

and:

```bash
git status
```

Finally:

```bash
git add .
git commit -m "feat: add notification system"
```

---

# 22. Conclusion

Continue is particularly interesting because it separates the **IDE** from the **AI model**.

Instead of:

```text
VS Code
   ↓
One AI provider
```

you can build:

```text
VS Code
   ↓
Continue
   │
   ├── Ollama
   │     └── Local/open-weight model
   │
   ├── Free API
   │     └── Free-tier model
   │
   ├── Cloud provider A
   │     └── Coding model
   │
   ├── Cloud provider B
   │     └── Reasoning model
   │
   └── Other providers
```

The result is a flexible AI development environment where you can choose the model based on the task.

### Recommended philosophy

Don't ask:

> "Which single AI model should I use?"

Instead ask:

> "Which model is appropriate for this task?"

Use:

```text
Fast/simple task
      ↓
Small local model

Normal development
      ↓
Medium coding model

Complex architecture/reasoning
      ↓
Powerful cloud model

Confidential code
      ↓
Local Ollama model
```

This approach gives you control over **cost, privacy, speed, and capability** while keeping your development workflow inside VS Code.
