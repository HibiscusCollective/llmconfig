# 0001 - Decision log format and process

**Status:** Accepted
**Driver:** @pfouilloux
**Date:** 01-01-2025

## Executive summary

In the context of technical decision documentation,
facing the need for standardized decision records,
we decided for Markdown Architectural Decision Records (MADR) with Y-Statement summaries
and against alternative documentation formats.
This achieves structured, traceable decision history,
accepting the complexity of a formal documentation process.

## Context and problem statement

We need a standardized format for recording architectural and technical decisions that meets the following requirements:

### Must have

- Clear structure for decision documentation
- Traceable decision history
- Context preservation
- Straightforward to write and review
- Searchable content

### Nice to have

- Template automation
- Version control friendly
- Links to related decisions
- Status tracking
- Impact assessment

## Decision drivers

- Need for consistent decision documentation
- Requirement for traceable decision history
- Importance of preserving context
- Need for efficient review process
- Need for searchable content

## Considered options

- Option 1: MADR with Y-Statement
- Option 2: RFC Process
- Option 3: Wiki-based documentation
- Option 4: Custom format

## Decision outcome

Chosen option: "MADR with Y-Statement"

Rationale:

- Provides structured format for consistent documentation
- Includes executive summary for quick understanding
- Integrates well with version control
- Supports linking between related decisions
- Allows for automated tools and validation

### Positive consequences

- Standardized decision documentation
- Clear review process
- Preserved context and rationale
- Version-controlled history
- Automated template generation
- Integrated status tracking

### Negative consequences

- Additional work for documentation
- Implementation delay for review and approval process
- Potential format drift over time
- Learning curve for new team members
- Risk of over/under documentation

## Benefits and drawbacks of options

### Markdown architectural decision records (MADR) with y-statement executive summary

- Good, because it provides structured documentation
- Good, because it includes executive summary
- Good, because it integrates with version control
- Good, because it supports automation
- Bad, because it requires more initial setup
- Bad, because its formal structure adds complexity

### Request for comment (RFC) process

- Good, because it is familiar to many developers
- Good, because it is flexible in format
- Bad, because it lacks structured templates
- Bad, because it is more difficult to track status
- Bad, because it is less consistent across documents

### Wiki-based documentation

- Good, because it is straightforward to edit
- Good, because it is accessible
- Bad, because it lacks version control
- Bad, because it is more difficult to review changes
- Bad, because it is less structured

### Custom format

- Good, because it is possible to tailor it to exact needs
- Good, because it can evolve with team
- Bad, because it requires maintenance
- Bad, because it lacks external tools support
- Bad, because it needs documentation
