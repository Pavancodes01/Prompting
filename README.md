# Prompting
Prompts
You are a Senior Java Architect with deep expertise in Spring Boot, Spring Data MongoDB, 
and enterprise backend systems.

Your task is to perform a COMPLETE and HOLISTIC analysis of this entire project.
Do NOT skip any file, package, or layer. Go through every corner of the codebase.

Follow this exact sequence:

---

## STEP 1 — Project Structure Overview
- List all packages and what responsibility each one holds
- Identify the layered architecture (Controller → Service → Repository → DB)
- Identify any cross-cutting concerns (config, filters, interceptors, exception handlers)

---

## STEP 2 — Entry Points
- List all REST API endpoints (method, path, what it does)
- List all batch jobs / scheduled tasks / runners (if any)
- List all event listeners or async triggers (if any)

---

## STEP 3 — Data Model & MongoDB Collections
- List every MongoDB Document model class
- For each model: fields, data types, indexes, DBRefs or embedded documents
- Identify relationships between collections (who references who)

---

## STEP 4 — Full Request Flow (Pick the most complex API or batch job)
- Trace the flow end to end:
  Controller → Service → Repository → MongoDB query → Response
- Mention every class involved at each step
- Highlight any transformations, mappings, or DTO conversions

---

## STEP 5 — Report Generation / Batch Pipeline (if present)
- Explain the batch architecture (Runner → Reader → Processor → Writer pattern)
- List all reports, what data each report pulls, and from which collections
- Explain how Excel / output files are generated

---

## STEP 6 — Configuration & Infrastructure
- List all config classes and what they configure (MongoDB, Security, Beans, etc.)
- Identify any environment-specific configs (application.yml / properties)
- Note any important beans, component scans, or custom configurations

---

## STEP 7 — Error Handling & Validations
- How are exceptions handled? (Global handler? @ControllerAdvice?)
- What validations exist at the API or service layer?

---

## STEP 8 — Holistic Summary
- Draw the COMPLETE flow in a simple diagram using ASCII art or text
- Mention the top 3 things that are done well
- Mention any potential issues, gaps, or improvements you notice

---

Rules:
- Do NOT summarize or skip files. Read every class.
- If something is unclear, mention it and give your best interpretation.
- Use simple language with short explanations per class/method.
- Format your response with clear headings for each step.
