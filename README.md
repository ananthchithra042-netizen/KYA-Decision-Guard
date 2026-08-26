# KYA-Decision-Guard
### Know Before You Act — An AI System That Knows When It Should Not Act

## Overview
KYA is a reliability and decision layer that wraps around an existing AI prediction model. 
Instead of letting a model act on every prediction, KYA computes a calibrated **Action 
Readiness Score (ARS)** from four independent signals and routes each decision to one of 
three lanes: **ACT**, **REVIEW**, or **STOP**.

## Core Formula
ARS = [0.3·C + 0.3·F + 0.2·Q − 0.2·U] × (1 − R)

Where:
- **C** — Confidence: how certain the model is about its top prediction
- **F** — Familiarity: how similar the input is to known training data
- **Q** — Input Quality: signal integrity (noise, corruption, completeness)
- **U** — Uncertainty: predictive spread / ambiguity
- **R** — Risk multiplier: cost of an incorrect autonomous action (0 = low-stakes, 1 = max stakes)

## Decision Bands
| ARS Score | Action |
|-----------|--------|
| < 0.40    | STOP   |
| 0.40–0.75 | REVIEW |
| ≥ 0.75    | ACT    |

## Tech Stack
- Frontend: HTML, CSS, JavaScript
- (Backend / Model: add your stack here)

## Team
**Tech Titans**
- Deepika A
- Aasiya Viyashree J
- Abhirami R

Department: Artificial Intelligence and Data Science

## Live Demo
🔗 https://quiet-sorbet-54335e.netlify.app/

## Problem Statement
AI systems can produce confident predictions even on unfamiliar or noisy inputs. KYA adds 
a decision layer that checks whether a prediction is reliable enough to act on, before 
allowing it to trigger a downstream action.

## Event
AI Innovation Challenge 2026 — Round 3, AI Evolution
