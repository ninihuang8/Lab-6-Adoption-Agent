# Emerging Technology Adoption Agent v0.1

This is the Phase 2 development candidate for NYU MASY1-GC 1800 Assignment 6. It supports contextual adoption decisions for Agentic AI in semiconductor scheduling and disruption management. It is a prompt-based specialist for the supplied ChatGPT runtime, not a deployed factory system. No API key, framework, new dependency, or custom orchestration is required.

Status: development files and controlled inputs prepared; behavioral tests, revisions, independent student judgment, and final Agent Record remain pending. Read records/phase2_audit.md for actual structural check results.

## File guide

| Relative to agents/adoption_agent/ | Purpose |
| --- | --- |
| agent_metadata.json | Specialist identity and 0.1-student version |
| specialist_instructions.md | Six postures, nine factors, qualitative gates, three-level analysis, one self-review pass, source rules and authority boundaries |
| cases/primary.json | Constructed fast-follower manufacturer |
| cases/contrast_1.json | Changes only adoption_posture |
| cases/contrast_2.json | Changes only S-VALIDATION in additional_context |
| records/evidence_log.md | Dated original sources, verification locations, applicability limits and gaps |
| records/development_decision_log.md | Actual design provenance and reserved student entries; no invented test history |
| records/phase2_audit.md | Structural validation, requirements traceability, baseline limitations and readiness |
| README.md | This guide, controlled test design and student upload SOP |

## Three controlled cases

All three keep technology, application, organization, staff/infrastructure assumptions, consequences, human approval, alternatives, management question, horizon, and external source capsules fixed. Primary and Contrast 2 use the same moderate/fast-follower posture. Contrast 1 changes only the posture to conservative/risk-averse.

Contrast 2 weakens the availability and traceability of operational validation artifacts, without changing actual system quality or other organizational capabilities. No case includes candidate performance results. A reviewable plan or baseline trace is not successful LLM-agent validation. These scenarios support conditional analytical decisions only.

Proposed fixed decision date 2026-10-28, initial review 2026-11-28, horizon end 2027-04-28. These are explicit constructed choices, not professor-specified dates. Student review is pending. Do not silently shift dates between cases.

No expected recommendation labels are stored in cases. Same labels may be defensible if scope, conditions or confidence differ. General technology findings must not change merely because organizational posture changes. Weaker evidence must not create stronger confidence in the same operational claim without a specific reason.

## Exact GitHub upload SOP for the student

1. Download Assignment6_Phase2_Adoption_Agent_v01.zip and unzip it locally. The archive contains an agents folder, then adoption_agent, then these nine files. It contains no frozen scaffold files.
2. Open https://github.com/ninihuang8/Lab-6-Adoption-Agent and select assignment-6-adoption using the branch selector. Verify the branch name before proceeding. Do not upload to main.
3. From the repository root, choose Add file, then Upload files. Drag the extracted agents folder into the upload area so nested paths are preserved. Upload the extracted folder, not the ZIP and not a screenshot. Do not select individual files in a way that flattens cases or records.
4. Inspect every previewed destination. There must be exactly nine NEW files, all beginning agents/adoption_agent/. They are the nine paths in the file guide above. No agents/agents nesting, no top-level adoption_agent, no _template changes, no __MACOSX or .DS_Store, and no changes under core/, tools/, docs/, examples/, or work/. If the preview flattens or relocates paths, cancel the upload and preserve the folder structure before retrying.
5. Review the instructions, evidence limits and constructed dates/assumptions. A suitable commit message is Add Adoption Agent v0.1 development candidate. Choose Commit directly to the assignment-6-adoption branch, then commit yourself. Do not create a new branch or pull request for this step.
6. On GitHub, open the new commit and verify Files changed contains exactly those nine additions. Copy the resulting full commit SHA for later verification. The baseline commit quoted in this package is not the new development commit.
7. Confirm the branch selector still shows assignment-6-adoption and main still has its original baseline history. Stop and request a read-only upload verification. Do not execute the Primary/Contrast tests until separately approved.

Baseline note: the inspected branch at 6bae06f949d29208ac169cf01b67be61f523d4a4 has one newline in agents/_template/responses/.gitkeep. This does not affect the Frozen Core, but exact original-scaffold parity is PARTIAL. If exact parity is to be restored, the student should separately make that file zero bytes and record that housekeeping commit. It is not included in this specialist upload and is not an agent revision.

## Later execution workflow requiring separate approval

The commands below are reproduction instructions only. Do not run them as part of the current upload step. From a full working scaffold root, the unchanged supplied builder can later generate a prompt packet:

```bash
python tools/check_frozen_core.py
python tools/build_prompt.py --agent agents/adoption_agent --case agents/adoption_agent/cases/primary.json --out work/adoption_agent_primary_v01_prompt.txt
python tools/build_prompt.py --agent agents/adoption_agent --case agents/adoption_agent/cases/contrast_1.json --out work/adoption_agent_contrast_1_v01_prompt.txt
python tools/build_prompt.py --agent agents/adoption_agent --case agents/adoption_agent/cases/contrast_2.json --out work/adoption_agent_contrast_2_v01_prompt.txt
```

Prompt packets must be submitted to ChatGPT individually using the same documented runtime/settings and fixed evidence snapshot. Use fresh conversations or otherwise avoid importing previous decisions. Save the first complete raw response exactly, before repair. A future responses/ folder can hold primary_v01_raw.txt, contrast_1_v01_raw.txt, and contrast_2_v01_raw.txt. Do not create illustrative responses now.

The supplied validator can later check a real saved response:

```bash
python tools/validate_response.py agents/adoption_agent/responses/primary_v01_raw.txt
```

Its PASS is only a basic contract check. Also check the complete frozen schema, all factors, evidence references, gates, self-review disposition, stable/changed findings, and approval boundary. Record actual validation output and substantive weaknesses separately. Do not overwrite the raw response, change a case just to obtain a favorable result, or invent a failure to satisfy the assignment. Preserve frozen tools. A malformed raw response stays intact; any later repair needs a separate file and explanation.

## Remaining assignment work

After approved executions, document a genuine weakness, revision and retest, an actual qualified/non-binary case, the student's own adoption judgment, a completed copy of the separately uploaded A-F Word Record, AI/verification note, and team handoff. Handoff needs the posture, strongest driver, likely reversal condition, and an issue for the Organizational Adoption Agent. No final Section F is drafted here.

The PDF rubric has four 20-point criteria including Self-Reflection; Common Instructions uses different weights. Address all substantive criteria and do not infer a grade conversion. No A or A++ outcome is guaranteed. Count preparation already spent toward the professor's 60-90 minutes; stop at 90 unless the instructor directs otherwise and preserve unresolved limitations rather than extending the project.
