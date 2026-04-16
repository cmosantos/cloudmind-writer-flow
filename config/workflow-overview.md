# Workflow Overview

CloudMind Writer Flow is a multi-agent workflow built to support the creation of technical articles about technology, artificial intelligence, and cloud computing.

The workflow transforms a single topic into a complete editorial package by dividing the process into specialized stages. Instead of relying on one large prompt, the system distributes responsibilities across multiple agents, each focused on a specific task.

## Workflow sequence

1. **Agent 1 – Web Researcher**  
   Searches for 3 reliable and relevant sources related to the topic.

2. **Agent 2 – Consolidator**  
   Consolidates the selected sources into a single clear and organized foundation.

3. **Agent 3 – Summarizer**  
   Turns the consolidated material into a strategic summary with thesis, message, and subtopics.

4. **Agent 4 – Writer**  
   Writes the full technical article in Markdown, with introduction, development, and conclusion.

5. **Agent 5 – Final Editor**  
   Refines the article for publication and generates the editorial package for Hashnode, including SEO fields.

6. **Agent 6 – EN Translator**  
   Translates the full editorial package into English while preserving structure and technical meaning.

7. **Agent 7 – Image Generator**  
   Generates a professional cover image based on the editorial image prompt.

## Main input fields

- `topic`
- `language`
- `article_length`
- `tone`

## Main output

The workflow can generate:

- Final title
- Final subtitle
- Full article in Markdown
- Short summary
- SEO Title
- SEO Description
- Meta description
- Tags
- Slug
- English version
- Image prompt
- Cover image concept

## Editorial focus

This workflow is designed for technical blog publishing, especially on platforms such as Hashnode, with themes related to:

- Artificial intelligence
- Cloud computing
- Automation
- Infrastructure
- APIs
- Technical productivity
- Innovation
