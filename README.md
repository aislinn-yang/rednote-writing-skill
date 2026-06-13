<div align="right">

**English** · [简体中文](README.zh-CN.md)

</div>

# rednote-writing-skill

A [Claude Code](https://claude.com/claude-code) skill that turns scattered ideas, notes, and raw material into a finished Rednote (Xiaohongshu) post. It keeps your judgment and voice, and never fabricates content.

## What it does

This is not a "one-click viral post" generator. It does three things: structures your scattered thoughts, lifts the phrasing to your own best level, and pushes the thinking further. You bring the judgment, the stance, and the real material. It reworks the wording and structure. It will boldly rewrite and reorganize, but it never makes up facts.

Three modes:

- **Collage**: start from links, screenshots, or raw material
- **Co-create**: start from a few rough ideas, iterate together into a finished draft
- **Review**: critique a draft you already wrote

Two things that set it apart:

1. **Voice is not driven by a generic template.** It uses a set of real posts (`examples.md`) as the only reference, so the tone and transitions have to read like the author, or it does not pass.
2. **Two gates before publishing.** First a mechanical scan for banned punctuation, AI-tells, and platform-throttling words (so the post is not silently suppressed), then a fresh "does this read like a real person" pass that hunts for AI-sounding lines. Title and cover come last.

## Files

| File | What's inside | When it's read |
| --- | --- | --- |
| `SKILL.md` | The entry point. Account positioning, the four non-negotiable rules (keep the voice and judgment but not the original words; extend the thinking but never invent facts; keep writing and checking separate; drive every step toward a finished draft), and the step-by-step workflow for each mode. | First, every time |
| `examples.md` | Eight real published posts, each tagged by type with notes on how it opens, transitions, and mixes judgment with personal detail. The single source of truth for voice. | While writing the body |
| `checks.md` | The hard-rule scan: banned punctuation, AI-tell phrases, structural AI-tells, and Rednote risk words (absolute-claim ad terms plus platform-throttling words). Mechanical and objective, a hit means fix. | After the body is done |
| `cover-title.md` | How to write the 2-3 cover lines and 3-5 titles, plus the hard "no" list (no em-dashes, emoji, filler or clickbait words, no absolute claims). | After both gates pass |
| `evals.md` | Three regression scenarios and how to run them against a baseline, to confirm a big edit did not degrade the voice or the flow. | Maintainers only, never while writing |

## Install

Clone this repo into your Claude Code skills directory:

```bash
git clone https://github.com/aislinn-yang/rednote-writing-skill.git ~/.claude/skills/xhs-post
```

Then trigger it inside Claude Code with prompts like "帮我写小红书", "我有个灵感", or "帮我审稿".

## Make it yours

This skill is tuned to one specific account (AI product growth x going-global). `examples.md` holds that account's real posts. To adapt it to your own voice:

1. Replace `examples.md` with your own representative posts. This matters most.
2. Update the positioning section in `SKILL.md`.
3. Tune the platform-risk word list in `checks.md`.
4. The "save to Notion" step is optional: fill in your own database link, or remove it.

## License

[MIT](LICENSE)
