# Lesson 04 — Automating Routine IT Tasks with AI

## Project Overview

This project documents my work in Lesson 4 of the Per Scholas **AI Skills for IT Support** course.

I practiced using AI to plan a routine IT automation workflow, evaluate its safety, and test proposed rules before allowing changes to a ticketing system.

The project focused on automating the quarterly archiving of closed IT incidents while protecting ticket records, attachments, and audit information.

**Project Type:** Guided IT support automation simulation  
**Tools and Concepts:** ChatGPT, CSV data analysis, ticketing systems, automation planning, audit logging, and risk assessment  
**Progress:** 2 of 3 lesson sections completed

## Business Scenario

An IT department needs to archive older, closed incident tickets every quarter.

The automation must identify eligible incidents while ensuring that protected records and attachments are preserved.

The workflow must support scheduled quarterly execution and manual initiation by an authorized technician.

### Requirements

- Include only incident tickets closed more than 90 days ago.
- Exclude records marked `Keep`.
- Preserve attachments and original ticket records.
- Compare eligible records against an expected count of 4,112.
- Require technician approval before changing archive flags.
- Record processed, archived, skipped, and failed items.
- Stop processing when validation fails.

## Project Activities

### 1. Created an Automation Specification

I documented the workflow's trigger, inputs, processing steps, expected output, and failure conditions.

The specification established clear boundaries for what the automation was allowed to change.

### 2. Used AI to Develop an Automation Plan

I prompted ChatGPT to produce a structured automation plan with numbered steps.

I required each step to be classified as:

- **READ:** Retrieves information without modifying records.
- **WRITES A FILE:** Produces reports or audit documentation.
- **CHANGES STATE:** Modifies ticket information and requires a rollback plan.

I also requested that ChatGPT identify assumptions and explain potential reasons not to automate the workflow.

### 3. Evaluated Automation Risks

I reviewed the proposed workflow for actions that exceeded the original requirements.

I identified potential risks involving:

- Accidental deletion of tickets or attachments.
- Incorrect assumptions about ticket eligibility.
- Processing tickets marked `Keep`.
- Archiving records without technician approval.
- Continuing when validation counts do not match.

I determined that ticketing system administrators must verify the archive rules and expected record count before production changes are permitted.

### 4. Tested Archive Rules Using Sample Data

The guided exercise used a 28-row CSV sample containing closed incidents and desk tasks.

I requested a report-only analysis that would classify records as eligible or ineligible without modifying the original data.

The exercise used September 20, 2026, as its reference date, with June 22, 2026, as the 90-day cutoff.

The proposed output included a `would_archive` field and an `archive-report.csv` file.

### 5. Manually Verified Sample Records

I reviewed three example records:

- `INC0012316`
- `TASK0048105`
- `INC0012313`

My review identified that `TASK0048105` was a task rather than an incident and therefore should not be archived.

I determined that the proposed rule needed modification to ensure only qualifying incidents were selected.

**Decision:** Modify the automation rule before proceeding.

## Results

The coursework demonstrated the importance of testing and validating automation logic before using it in production.

My review established that:

- Ticket type must be included in eligibility checks.
- Protected records must remain unchanged.
- Attachments must be preserved.
- Unexpected record counts require investigation.
- Technician review is necessary before state-changing operations.

The exercise did not establish that a production automation script was deployed or that a live ticketing system was modified.

## Skills Demonstrated

- AI-assisted IT automation planning
- Requirements gathering and specification writing
- CSV-based data validation
- Ticket lifecycle management
- Risk identification
- Human approval checkpoints
- Audit logging requirements
- Safe automation design
- Troubleshooting and quality assurance

## Relevance to Tier 1 Help Desk

This project strengthened my understanding of how IT support teams can use automation to reduce repetitive administrative work while maintaining accuracy and accountability.

It also reinforced the importance of verifying AI-generated recommendations, documenting decisions, and escalating changes that require higher-level authorization.

## Supporting Evidence

Coursework evidence may include my completed automation specification, AI prompt, risk review, and report-only testing decisions.

## Training

**Program:** Per Scholas — AI Skills for IT Support  
**Lesson:** 04 — Automating Routine IT Tasks with AI

*This project is based on a fictional training scenario. All ticket identifiers and systems are simulated.*
