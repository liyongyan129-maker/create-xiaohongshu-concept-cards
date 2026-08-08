---
name: create-xiaohongshu-concept-cards
description: 规划、撰写、生成并修改面向 AI 小白的小红书概念词解或知识图解图文笔记，适用于 LLM、AIGC、Agent、RAG 等概念，输出包含封面、故事化逐页脚本、统一字体与角标、3:4 配图、标题方案及 200 字以内正文。当用户说“做一篇小红书概念词解”“做一篇小红书知识图解”，或明确调用 $create-xiaohongshu-concept-cards 时使用；也适用于沿用已确认的银灰橙色复古未来视觉系统，或根据标注截图迭代图片。
---

# Create Xiaohongshu Concept Cards

Produce a complete, reusable Xiaohongshu concept-explainer post. Treat content accuracy, page planning, and visual consistency as separate approval gates.

## Load references

- Read [references/workflow.md](references/workflow.md) before planning any post.
- Read [references/visual-system.md](references/visual-system.md) before writing image prompts or editing images.
- Read [references/content-rules.md](references/content-rules.md) before researching or drafting copy.
- Use the approved images under `assets/approved-llm-example/` as visual references, not as content templates that must be copied literally.

## Required workflow

1. Clarify the term, target reader, intended takeaway, style choice, deliverable format, and any ambiguous meaning.
2. Research “是什么、为什么、怎么用/做” from multiple reliable sources when the term needs current or technical verification. If the user explicitly says not to browse, use already collected material and state that constraint internally. Never browse again merely to reconfirm settled material.
3. Propose the page count and page-by-page narrative before generating images. Require explicit confirmation. Default to at least four pages; do not assume an upper limit.
4. Draft one recommended title, two alternatives, a body under 200 Chinese characters, and the complete page script.
5. Generate or edit one page at a time with the image generation skill. Preserve approved pages and save revisions with versioned filenames.
6. Validate every page for text accuracy, 3:4 dimensions, hierarchy, corner labels, margins, orange consistency, and scene clarity.
7. Present the complete set for approval. Do not package a new reusable style until the example set is approved.

## Approval gates

Do not skip these gates:

- Gate A — meaning and audience confirmed.
- Gate B — page count and page script confirmed.
- Gate C — cover direction confirmed.
- Gate D — content-page visual system confirmed.
- Gate E — full-set consistency confirmed.

When feedback is local, change only the named page or element. Do not regenerate unrelated pages.

## Image production rules

- Use 1086 × 1448 px, 3:4 portrait.
- Keep the cover headline centered and dominant.
- Keep content-page headlines left aligned with identical top and left margins, font size, weight, line spacing, and orange brightness across the set.
- Put explanations only at the top or bottom; reserve the middle for the visual scene.
- Use fixed corner labels: top-left `2026`, top-right `ZHELI`, bottom-left `AI`, bottom-right the variable keyword of no more than four characters.
- Keep corner labels small and thin.
- Use one visual idea per page. Remove decorative modules that do not clarify the concept.
- Use the exact approved orange consistently across headlines, emphasized explanation text, and restrained machine accents.
- Preserve source images and save `v2`, `v3`, and later versions instead of overwriting.
- Inspect each local image before editing it. Inspect every generated output before delivery.

## Delivery

Deliver:

- one recommended title and two alternatives;
- body copy under 200 Chinese characters;
- confirmed page count and page-by-page script;
- final PNG set in sequence;
- dimensions and saved paths;
- a short note listing the final visual and content invariants.

Do not promise editable source files unless requested. Raster PNG delivery is sufficient by default.
