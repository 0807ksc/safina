# AGENTS.md

## 목적
- 이 문서는 이 저장소에서 작업하는 에이전트 실행 규칙을 정의한다.
- Safina 도메인 컨텍스트의 단일 기준은 `doc/project-context-Safina.md`다.

## Skills
A skill is a set of local instructions to follow that is stored in a `SKILL.md` file. Below is the list of skills that can be used.

### Available skills
- context-workflow: Reusable context management workflow for any repo. Use when standardizing request capture, decision log, next-action queue, and pruning process. (file: `skills/context-workflow/SKILL.md`)

### How to use skills
- Discovery: skills are listed in this file with name, description, and file path.
- Trigger rules: if the user names a skill (with `$SkillName` or plain text) or task clearly matches a listed skill, use that skill for the turn.
- Missing/blocked: if a named skill is missing or unreadable, state it briefly and continue with best fallback.
- Progressive disclosure:
1. Open target `SKILL.md` and read only enough to execute.
2. Resolve relative paths from the skill directory first.
3. Load only required references, scripts, or templates.

## 프로젝트 컨텍스트 규칙
- 기능/정책/우선순위 판단은 먼저 `doc/project-context-Safina.md`를 확인한다.
- 컨텍스트와 구현이 충돌하면 임의 확정하지 않고 변경 제안을 남긴다.
- 공통 앱 Agent 조직/협업은 `doc/app-agent-organization.md`를 기준으로 적용한다.

## 문서 업데이트 원칙
- 제품 방향 변경: `doc/project-context-Safina.md` 갱신
- 에이전트 동작 규칙 변경: `AGENTS.md` 갱신
- 일반 컨텍스트 운영 규칙 변경: `doc/context-workflow.md` 갱신
- Safina 전용 운영 규칙 변경: `doc/safina-workflow.md` 갱신

## Context Management Protocol (Always Apply)
- Project workflow: `doc/safina-workflow.md`
- Standard workflow: `doc/context-workflow.md`
- Temporary context: `doc/context-inbox.md`
- Decision log: `doc/context-log.md`
- Next-action queue: `doc/next-actions.md`
- Pruning rules: `doc/context-prune-rules.md`

Working rules:
- At task start, summarize the request in `doc/context-inbox.md`.
- Record meaningful decisions in `doc/context-log.md`.
- Move unfinished work into `doc/next-actions.md` with priority.
- Before ending task, prune inbox and keep only unresolved items.
