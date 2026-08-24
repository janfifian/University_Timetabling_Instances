# University Course Timetabling — Benchmark Instances

This directory holds three timetabling instances using the YAML schema (`schema_version: 1`):

 - top-level entity blocks (`faculties`, `buildings`, `institutes`, `study_fields`,
`semesters`, `classrooms`, `lecturers`, `subjects`, `students_groups`, `students`)
 - a fully-built `problem_instance` block carrying the denormalised sets the solver consumes (`P`, `C`, `G`, `R`, `T`, room/course groupings, linking data, etc.).

## Contents

Detailed description can be found in the source paper.

| Path | What it is | Size (key sets) |
|------|------------|-----------------|
| `artificial_64_suite/` | 64 synthetically generated instances, organised in difficulty tiers (`easy` / `medium` / `hard` / `extreme`) | varies per tier |
| `lato/LATO_instance.yaml` | One real-world instance derived from a UniTime XML export of a summer ("lato") semester. | 229 lecturers · 697 subjects · 58 rooms · 105 groups · 1629 students |
| `three_studies/3_studies_instance.yaml` | One real-world instance spanning three study programmes of a single faculty. | 55 lecturers · 126 subjects · 52 rooms · 12 groups · 259 students |

## Anonymisation

All three items are anonymised. The only human-readable label kept is the faculty acronym `FTIMS` in case of the real-life data instances. 

## Reproducibility note

The anonymisation of `3_studies` is a consistent, deterministic relabelling: each distinct source string maps to exactly one token, applied everywhere, so all cross-references and the optimisation structure are preserved unchanged. The reverse mapping is **not** included here for obvious reasons.