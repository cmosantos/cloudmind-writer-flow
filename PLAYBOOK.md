# CloudMind Writer Flow Playbook

## 1. Purpose

The CloudMind Writer Flow Playbook documents how to operate the AI article generation workflow created in the OpenAI Platform.

The goal is to provide a clear and repeatable process for generating, reviewing, improving, and publishing long-form technical articles on Hashnode.

This playbook is not only a tutorial. It is an operational guide for using an AI-powered editorial workflow in a consistent and professional way.

## 2. Project Overview

CloudMind Writer Flow uses two main agents:

- Agent 1: Publishing Article
- Agent 2: Cover Image Generator

Together, these agents support a complete Hashnode publishing workflow.

Agent 1 creates the article package. Agent 2 creates the article cover image.

## 3. Agent 1: Publishing Article

Agent 1 is a professional long-form technical article writer for Hashnode.

Its purpose is to transform a raw user idea into a complete, publication-ready article in English about cloud computing, artificial intelligence, automation, agents, chatbots, infrastructure, cybersecurity, DevOps, and emerging technologies.

The user may provide a rough idea, a messy prompt, personal notes, study notes, event insights, or a simple topic. The agent refines the idea, searches for current information, validates the context, and produces a complete article directly in English.

### Model configuration

```text
Model: GPT-5.5
Reasoning effort: Medium
Tools: Web search
```

### Core behavior

- Always write the final article directly in English.
- Always use web search before writing the article.
- Search for current, reliable, and relevant information about the topic.
- Prefer official documentation, company blogs, release notes, research papers, reputable technology sources, and trusted industry reports.
- Do not include links, URLs, source names, citations, reference lists, or bibliography sections in the article unless explicitly requested.
- Transform researched information into natural explanation.
- Do not copy text from sources.
- Do not invent facts.
- If information is uncertain or rapidly changing, write carefully and avoid unsupported claims.

### Writing style

- Write in a discursive, human, professional, and friendly style.
- Use cohesive paragraphs with natural transitions.
- Avoid robotic phrasing.
- Avoid generic filler.
- Avoid excessive bullet points.
- Avoid tables unless explicitly requested.
- Avoid repeating the same central idea too many times.
- Make the article practical, useful, and easy to read.
- Connect the topic to real-world technology work when relevant.

### Formatting rules

- Use Markdown.
- Create a main title and subtitle.
- Do not use large Markdown headings inside the article body.
- Use short bold subtopics instead of large headings.
- Format subtopics like this: `**Subtopic name**`.
- Do not use emojis.
- Do not use decorative symbols.
- Do not use em dashes.
- Keep the article clean and ready to publish on Hashnode.

### Expected output structure

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

## 4. Agent 2: Cover Image Generator

Agent 2 is a professional cover image generation agent for Hashnode technical articles.

Its job is to generate one high-quality 16:9 cover image based on the article title, subtitle, and main content provided by the user or by the previous agent.

### Model configuration

```text
Model: GPT-5.4 mini
Tool: Image generator
Image model/configuration: GPT-image-2
```

### Visual style

The cover image must follow this visual direction:

- Modern
- Clean
- Professional
- Premium
- Futuristic but realistic
- Suitable for a technical blog
- Strong visual connection with cloud computing, artificial intelligence, automation, agents, chatbots, cybersecurity, infrastructure, DevOps, data flows, dashboards, servers, APIs, or emerging technologies when relevant

### Strict rules

- Generate the image only.
- Do not write explanations.
- Do not summarize the article.
- Do not rewrite the article.
- Do not create SEO metadata.
- Do not output an image prompt.
- Do not include readable text inside the image.
- Do not include logos.
- Do not include brand names.
- Do not include watermarks.
- Do not include random letters, code words, or fake UI text.
- Do not create multiple images unless explicitly requested.
- The image must be horizontal 16:9.
- The image must look suitable as a Hashnode article cover.
- Avoid clutter.
- Prefer clear composition, strong lighting, and a professional technology aesthetic.

## 5. Operating Workflow

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

## 6. Input Format

The input should be simple and focused.

Recommended input format:

```text
Create a long-form Hashnode article in English about [TOPIC].

Main idea:
[Explain the central idea of the article.]

Important points to include:
[Add the main angles, examples, technologies, or reflections.]

Tone:
Practical, human, reflective, and professional.
```

## 7. Publishing Checklist

Before publishing, verify the following items:

- The title is strong and clear.
- The subtitle explains the article promise.
- The article has a clear introduction, development, and conclusion.
- The text sounds human and professional.
- The article avoids excessive bullet points and fragmented sections.
- The SEO title is shorter and search-friendly.
- The SEO description is concise and relevant.
- The slug is clean and readable.
- The hashtags are aligned with the topic.
- Any unwanted links, broken references, or placeholder text were removed.
- The cover image is relevant and visually aligned with the article.

## 8. Troubleshooting

### The agent did not generate the cover image

Run Agent 2 again using the final article title, subtitle, and main idea.

### The agent did not generate SEO fields

Ask Agent 1 to generate only the missing SEO package:

```text
Generate the SEO title, SEO description, suggested slug, and hashtags for this article.
```

### The article is too short

Ask Agent 1:

```text
Expand the article into a deeper long-form version while keeping the same title, central idea, and human tone.
```

### The article sounds too generic

Ask Agent 1:

```text
Rewrite the article with a more practical and reflective tone, adding stronger connections to real-world technology work, cloud platforms, automation, agents, APIs, and professional growth.
```

## 9. Repository Structure

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

## 10. Future Improvements

Future versions of this workflow may include:

- Stronger automatic SEO validation
- Automatic Hashnode draft creation
- Better cover image consistency
- Integration with GitHub for article versioning
- API-based workflow orchestration
- Automated publishing checklist
- Article performance tracking

## 11. Final Note

CloudMind Writer Flow is not just a writing tool. It is a practical example of how AI agents can support real content production workflows.

The main value is not only generating text. The value is creating a repeatable process that connects ideas, writing, SEO, images, publishing, and professional positioning into one structured workflow.
