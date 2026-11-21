# Lesson 03 — AI-Enabled Troubleshooting Assistants

## Project Overview

This project documents my work in Lesson 3 of the Per Scholas **AI Skills for IT Support** course.

I practiced using AI to support technical troubleshooting while independently checking its recommendations against available evidence, system information, and technical documentation.

The focus was on diagnosing a Windows 11 Wi-Fi connectivity issue, evaluating suggested troubleshooting steps, and documenting findings for escalation.

**Project type:** Guided IT support simulation  
**Operating system:** Windows 11  
**Tools and concepts:** ChatGPT, PowerShell, network adapter diagnostics, technical documentation, remote support, and ticket escalation  
**Progress:** 2 of 3 lesson sections completed

## Troubleshooting Scenario

A user reported that a Windows 11 laptop could not connect to Wi-Fi after switching from Ethernet.

The laptop used an **Intel(R) Wi-Fi 6 AX201 160MHz** adapter.

Initial evidence showed:

- The Wi-Fi adapter displayed **Disconnected**.
- Ethernet connectivity was functioning.
- The Wi-Fi driver version had not yet been confirmed.
- The troubleshooting session was being conducted remotely over a wired connection.

The objective was to restore reliable Wi-Fi connectivity without unnecessarily disrupting the user's remote session.

## Troubleshooting Process

### 1. Documented the issue

I created a troubleshooting specification identifying the symptoms, system environment, and expected successful outcome.

The success criteria included connecting to Wi-Fi without Ethernet, loading websites, and maintaining a stable connection.

### 2. Evaluated AI-generated recommendations

I prompted ChatGPT to analyze the available evidence and suggest a troubleshooting sequence.

I required the AI to distinguish confirmed information from assumptions and provide supporting references.

During my review, I identified a source that did not clearly establish compatibility with the specific Intel Wi-Fi adapter or driver version.

This demonstrated why AI-generated technical recommendations require independent verification.

### 3. Reviewed troubleshooting actions

I evaluated the proposed steps and classified them as:

- **TRUST:** Check the adapter status and driver version using PowerShell.
- **ADAPT:** Examine Windows 11 Wi-Fi settings and available networks before making changes.
- **REJECT:** Avoid reinstalling or updating the driver without confirming that the proposed instructions apply to the device.

I prioritized information-gathering steps before potentially disruptive changes.

### 4. Developed a remote troubleshooting plan

I used AI to help structure a troubleshooting plan that:

- Began with diagnostic checks.
- Prioritized less disruptive actions.
- Considered the impact of changes on the remote support session.
- Included rollback considerations.
- Excluded recommendations I had rejected during review.

### 5. Documented the outcome

The simulation work record reported that Wi-Fi connectivity was restored without reinstalling the driver.

After the wired dock was disconnected, the user confirmed that:

- Wi-Fi connected automatically.
- Websites loaded.
- Microsoft Teams worked.

A restart test was still required to confirm that the fix persisted.

A separate printer issue involving blank pages remained unresolved.

### 6. Prepared a Tier 2 escalation

I practiced creating an internal work note with four sections:

1. Findings
2. Actions Taken
3. Outcome
4. Follow-Up for Tier 2

I focused on distinguishing confirmed results from unresolved issues and avoiding unsupported assumptions.

## Results and Lessons Learned

Through this guided simulation, I demonstrated how to:

- Structure a technical troubleshooting investigation.
- Evaluate AI-generated diagnostic recommendations.
- Identify assumptions and unsupported technical claims.
- Prioritize low-risk troubleshooting steps.
- Consider remote-session disruption.
- Verify reported outcomes against defined success criteria.
- Document unresolved issues for escalation.

**Important:** This project represents a course-based troubleshooting simulation, not a production support incident or a separately
