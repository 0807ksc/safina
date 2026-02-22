# Safina Workflow

## Purpose
- Keep Safina-specific domain decisions separate from reusable context workflow.

## Source Documents
- Product/Domain context: `doc/project-context-Safina.md`
- Reusable context operations: `doc/context-workflow.md`

## Project-Specific Flow
1. Check task fit against project domain scope.
2. Resolve requirement details from product context and active request scope.
3. Apply code/document changes within requested scope only.
4. If implementation conflicts with project context, record change proposal instead of forced decision.
5. Verify output remains inside project boundaries.

## Usage
- Use this file for domain decisions.
- Use `doc/context-workflow.md` for capture/log/carry-over/pruning mechanics.
