# BP Review Skill

A Codex skill for reviewing investor-facing business plans and pitch decks. The skill name is `bp-investor-review`.

## Capabilities

- **Evidence review:** map each BP module to screening questions, evidence gaps and concrete next actions.
- **Competitive advantages:** distinguish shared market opportunities from supported, team-specific advantages.
- **Funding consistency:** connect budgets, business assumptions, cash flows, milestones and adverse scenarios.

The executable skill and capability cards are primarily in Chinese, with English trigger phrases.

## Install

Clone this repository into your Codex skills directory using the directory name `bp-investor-review`, or copy this repository there. Start a new Codex session after installation.

## Use

Ask Codex:

> Use bp-investor-review to review this pitch deck. Identify the evidence gaps and the three most important improvements.

Or:

> 用 bp-investor-review 检查这份融资计划：预算、业务假设、现金跑道和里程碑是否一致？

Provide the deck or its text and supporting data. Missing data should produce a fillable review framework, not invented conclusions.

## Repository layout

- `SKILL.md`: skill entrypoint and capability routing.
- `references/`: three capability cards, source overview, glossary and quick reference.
- `source/`: editable Cangjie capability bundle used to compile the skill.
- `BUILD_MANIFEST.json`: compiler version and generated-file hashes.
- `evals/`: nine behavioral cases and the independent static review report.

Edit the source bundle and recompile rather than hand-editing generated files. Using an installed Cangjie v2.5.0 toolchain, compile `source/` in `single` mode into a staging directory, validate it, then replace only the generated files. The compiler itself is an external dependency and is not bundled here.

## Validation

The initial compiled skill passed structural validation with zero errors or warnings and nine static behavior checks. These checks are not an empirical host-discovery or multi-model benchmark. The cash-flow example checks that unchanged expenses remain unchanged when conversion drops.

## Source and limits

Distilled with Cangjie from [天使、VC投资：商业计划书筛选的底层逻辑](https://www.bilibili.com/video/BV1yidtBoEeK/), by 棋从断處生. Source audio was automatically transcribed; source citations refer to that transcript version. The full transcript and audio remain in the original delivery and are not included in this repository.

The skill separates source statements from executable adaptations. Teaching examples are not verified investment outcomes, and numerical examples are not universal thresholds. It does not provide investment guarantees, live valuations or legal due diligence.
