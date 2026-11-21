# Lesson 05 — Scripting Routine Support Automations with AI

## Project Overview

This project documents my work in Lesson 5 of the **Per Scholas AI Skills for IT Support** program.

I practiced using ChatGPT to design, review, and troubleshoot a PowerShell automation function intended to collect Windows laptop diagnostic information for Tier 2 escalation.

The primary focus was creating clear technical requirements, identifying potentially unsafe code, handling errors, and distinguishing simulated results from verified execution.

**Project Type:** Guided PowerShell scripting and code review exercise  
**Environment:** Windows 11 / Windows PowerShell 5.1  
**Tools:** ChatGPT, PowerShell, Windows diagnostic commands  
**Progress:** 2 of 3 lesson sections completed

## Troubleshooting Scenario

A Tier 2 lead requests a diagnostic collection tool that Tier 1 technicians can use during remote support sessions.

The tool should gather relevant laptop information without requiring administrator privileges or changing system settings.

The proposed function is named `Export-EscalationSnapshot`.

## Project Requirements

The automation must collect five diagnostic categories:

1. Windows operating system version and build.
2. Time since the last system restart.
3. Available disk space on each drive.
4. Network adapter status and driver information.
5. Critical and error events from the Windows System event log.

### Input Parameters

- `HoursBack`: Optional parameter specifying the event-log lookback period in hours. Default: 24.
- `OutFolder`: Optional parameter specifying where the report should be saved. Default: current folder.

### Expected Output

A timestamped text report named `Tier2-Laptop-Facts`, saved in the specified output folder without overwriting existing files.

## Project Activities

### 1. Created a PowerShell Specification

I defined the function's purpose, trigger, inputs, processing steps, expected output, and failure conditions.

The specification required the function to collect diagnostic information without restarting the computer, changing settings, deleting files, or modifying system logs.

### 2. Developed AI Scripting Instructions

I used ChatGPT to help design a PowerShell function under specific technical constraints:

- Compatible with Windows PowerShell 5.1.
- Uses built-in Windows commands.
- Does not require administrator privileges.
- Does not install external modules.
- Uses a single function with a parameter block.
- Can be pasted into a PowerShell window where `.ps1` files are blocked.
- Provides numbered lines for easier review and debugging.

I also established requirements for documenting assumptions and identifying functionality that still required testing.

### 3. Reviewed AI-Generated Code

I used a structured code review process covering four categories:

**Hallucinated Commands:** Identify commands that might not exist in the required PowerShell environment.

**Destructive Operations:** Identify operations that create, change, delete, disable, or transmit data.

**Failure Gaps:** Identify missing handling for invalid parameters, empty results, and permission failures.

**Security:** Review administrator requirements, credential exposure, and data-sharing risks.

I examined the use of `Get-WinEvent` for collecting Windows System event information and identified concerns about safely writing the output report.

### 4. Evaluated Report-Saving Behavior

I identified that the report must not overwrite an existing file.

My review recommended using a unique output filename and testing the file-writing behavior before approving the script for operational use.

### 5. Practiced Debugging and Test Documentation

I worked through a debugging exercise involving the `HoursBack` parameter.

The exercise identified a potential interpretation error in which the parameter was treated as days instead of hours.

I documented the need to clarify the specification and rerun the affected test.

The saved coursework contains placeholders for three expected and actual test results, so successful execution has not been independently established.

### 6. Reviewed README Accuracy

I evaluated whether the proposed documentation accurately reflected the function's requirements, limitations, and testing status.

My decision was **Needs revision**, because the script and documentation required additional verification before approval.

## Expected Error Handling

The proposed function should:

- Validate its input parameters.
- Report sections that cannot be read.
- Display `No matching events found` when appropriate.
- Avoid inventing diagnostic results.
- Preserve existing output files.
- Avoid changes to Windows settings and system logs.

## Test Log

| Test | Status |
|---|---|
| Default 24-hour diagnostic collection | Not verified |
| Custom `HoursBack` value | Not verified |
| Custom output folder | Not verified |
| Invalid parameter handling | Not verified |
| Existing report protection | Not verified |
| Missing event-log results | Not verified |

The course record documents a debugging scenario involving the interpretation of `HoursBack`, but does not provide completed execution logs confirming successful results.

## Still Unverified

Before considering the function ready for real IT support use, the following must be confirmed:

- PowerShell 5.1 compatibility.
- Availability of required commands.
- Execution under standard-user permissions.
- Correct interpretation of `HoursBack` in hours.
- Accurate collection of all five diagnostic categories.
- Proper handling of missing or inaccessible data.
- Safe report creation without overwriting files.
- Accurate documentation of actual test results.

## Skills Demonstrated

- PowerShell automation planning
- AI-assisted scripting
- Technical requirements documentation
- PowerShell command review
- Error-handling analysis
- Debugging methodology
- Safe file-output design
- Test planning and validation
- Tier 1 to Tier 2 escalation preparation
- Responsible use of generative AI

## Relevance to Tier 1 Help Desk

This exercise demonstrates my understanding of how diagnostic automation can help IT support technicians collect consistent information for escalation.

It also reinforces the importance of verifying AI-generated code, protecting user systems, and documenting what has and has not been tested.

## Supporting Evidence

Supporting coursework evidence will be added separately. This project does not claim a completed production deployment or verified successful execution.

## Training

**Program:** Per Scholas — AI Skills for IT Support  
**Lesson:** 05 — Scripting Routine Support Automations with AI

*This is a guided training exercise using fictional support scenarios.*
