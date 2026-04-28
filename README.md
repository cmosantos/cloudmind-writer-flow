# CloudMind Writer Flow

CloudMind Writer Flow is an AI-powered editorial workflow created to generate long-form technical articles for Hashnode using agents built in the OpenAI Platform.

The project combines article generation, web research, SEO metadata, slug creation, hashtags, and cover image generation into a simple publishing process.

The goal is not only to generate text, but to document a practical workflow that connects Artificial Intelligence, cloud computing, automation, agents, and technical content creation.

## Project Purpose

This project was created to support the production of professional technical articles in English about topics such as Artificial Intelligence, cloud computing, automation, agents, chatbots, cybersecurity, infrastructure, DevOps, APIs, and emerging technologies.

The workflow helps transform raw ideas, study notes, market observations, or personal learning experiences into complete Hashnode-ready articles.

It is also a portfolio project that demonstrates practical use of AI agents, prompt design, web research, publishing workflow documentation, and content automation.

## Current Workflow

The current version of CloudMind Writer Flow uses two main agents.

**Agent 1: Publishing Article**

This agent transforms a raw idea into a complete long-form technical article in English.

It uses web search to validate current information and generates a complete Hashnode publishing package, including title, subtitle, article body, SEO title, SEO description, suggested slug, and hashtags.

**Agent 2: Cover Image Generator**

This agent generates one professional 16:9 cover image for the article.

The image is based on the article title, subtitle, and main idea. It follows a modern, clean, premium, and technology-focused visual style suitable for Hashnode technical publications.

## Workflow Overview

```text
User idea or topic
        ↓
Agent 1: Publishing Article
        ↓
Complete Hashnode article package
        ↓
Manual review
        ↓
Agent 2: Cover Image Generator
        ↓
16:9 technical cover image
        ↓
Hashnode publishing
```

## What the Workflow Generates

The workflow is designed to generate the following outputs:

- Main article title
- Subtitle
- Long-form article in English
- SEO title
- SEO description
- Suggested slug
- Hashtags
- 16:9 cover image

The article output is designed to be ready for Hashnode, while still allowing manual review and final editorial adjustments before publishing.

## Agent 1: Publishing Article

Agent 1 is configured as a professional long-form technical article writer.

**Model configuration:**

```text
Model: GPT-5.5
Reasoning effort: Medium
Tools: Web search
```

**Main responsibilities:**

- Transform rough ideas into complete articles
- Write directly in English
- Use web search before writing
- Validate current and relevant information
- Avoid unsupported claims
- Produce publication-ready Markdown
- Generate SEO metadata
- Keep the article human, practical, and professional

**Expected output structure:**

```markdown
# Title

# Subtitle

# Article

# Hashnode SEO Package

SEO Title:

SEO Description:

Suggested Slug:

Hashtags:
```

## Agent 2: Cover Image Generator

Agent 2 is configured as a cover image generation agent for technical articles.

**Model configuration:**

```text
Model: GPT-5.4 mini
Tool: Image generator
Image model/configuration: GPT-image-2
```

**Main responsibilities:**

- Generate one horizontal 16:9 cover image
- Represent the article topic visually
- Follow a professional technical blog style
- Avoid text, logos, watermarks, and fake UI words
- Keep the image clean, modern, and suitable for Hashnode

## Repository Structure

```text
cloudmind-writer-flow/
│
├── README.md
├── PLAYBOOK.md
│
├── config/
│   └── workflow-overview.md
│
├── prompts/
│   ├── agent-1-publishing-article.md
│   └── agent-2-cover-image-generator.md
│
└── tests/
    ├── sample-input.md
    └── sample-output.md
```

## Operational Playbook

This project includes a complete operational playbook documenting how the workflow works, how to operate the agents, how to review the output, and how to troubleshoot common issues.

Read the full playbook here:

[CloudMind Writer Flow Playbook](./PLAYBOOK.md)

## How to Use

Open Agent 1 in the OpenAI Platform and provide a topic, idea, or rough note.

Example input:

```text
Create a long-form Hashnode article in English about how Artificial Intelligence is becoming a layer inside apps, agents, enterprise platforms, cloud services, APIs, and workflows.

The article should explain why standalone AI apps are growing quickly, why enterprise environments still depend on platforms like Azure, AWS, Google Cloud, Microsoft 365, and Google Workspace, and why professionals in IT, cloud, automation, and support should learn how these pieces connect.
```

After Agent 1 generates the article package, review the title, subtitle, article body, SEO fields, slug, and hashtags.

Then open Agent 2 and provide the final title, subtitle, and article idea to generate the cover image.

Finally, copy the article and cover image to Hashnode, review the final formatting, and publish.

## Quality Checklist

Before publishing, check whether:

- The title is strong and clear
- The subtitle supports the article idea
- The article has a strong introduction, development, and conclusion
- The tone is human, professional, and practical
- The SEO title is under 60 characters
- The SEO description is under 150 characters
- The slug is clean and URL-friendly
- The hashtags are relevant
- The cover image matches the article topic
- There are no unwanted links, placeholders, or broken references

## Project Status

This project is active and evolving.

The current version focuses on a two-agent workflow:

```text
Article generation + Cover image generation
```

Future improvements may include better automation, article versioning, GitHub integration, Hashnode draft creation, stronger SEO validation, and workflow orchestration through APIs.

## Why This Project Matters

CloudMind Writer Flow is a practical example of how AI agents can support a real publishing workflow.

It shows how a technology professional can use AI not only as a chatbot, but as part of a structured process for research, writing, SEO, visual generation, publishing, and portfolio development.

The project reflects the growing importance of AI agents, cloud platforms, automation, APIs, and workflow design in modern technology careers.
