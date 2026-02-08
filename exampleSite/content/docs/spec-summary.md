---
title: "Specification Summary"
date: 2025-11-18
summary: "High-level requirements and invariants for compliance."
tags: ["spec", "requirements"]
topics: ["governance", "compliance"]
---

## Summary

The specification summary defines the minimum viable requirements for a compliant system.

## Required Fields

```txt
id: string
status: one of [draft, active, retired]
review_window_days: integer
```

<div class="callout callout--danger">
  <strong>Danger.</strong> Missing required fields invalidates the submission.
</div>

## Notes

- All fields must be explicitly present.
- Null values are not permitted.
