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

{{< callout type="danger" title="Danger" >}}
Missing required fields invalidates the submission.
{{< /callout >}}

## Notes

- All fields must be explicitly present.
- Null values are not permitted.
