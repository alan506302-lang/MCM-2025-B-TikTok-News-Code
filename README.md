# MCM-2025-B-TikTok-News-Dissemination-Code
Code for 2025 MCM Problem B: TikTok News Dissemination Modeling

## Overview
This repository contains complete Python code for solving 2025 MCM Problem B, focusing on the dynamics of news dissemination on TikTok. The code implements mathematical models for user penetration rate fitting, fact-checking tool effectiveness evaluation, multi-platform competition analysis, and multi-objective regulation strategy optimization, with reproducible results and visual outputs.

## Code Structure
| File Name | Corresponding Problem | Core Function |
|-----------|------------------------|---------------|
| `Q1_penetration_bass_decay` | Problem 1: User Penetration Rate Modeling | Fit penetration evolution with improved Bass model; analyze age-group differences |
| `Q2_factcheck_SIR_SR` | Problem 2: Fact-Checking Tool Effectiveness | Improved SIR model with fact-checking mechanism; quantify false news suppression rate |
| `Q3_platform_migration` | Problem 3: Multi-Platform Competitive Dynamics | Coupled user migration model; simulate platform share evolution |
| `Q4_optimization_policy` | Problem 4: Multi-Objective Regulation Optimization | Multi-objective optimization of fact-checking strategies; robustness analysis |

## Module Details
### 1. Q1_penetration_bass_decay
- **Model**: Improved Bass diffusion model (incorporating decay term)
- **Key Tasks**:
  - Fit the time-evolution curve of TikTok's news penetration rate among 18–29-year-olds
  - Estimate core parameters (innovation coefficient `p`, imitation coefficient `q`, saturation penetration rate `M`, decay timescale `tau`)
  - Quantify penetration differences between 18–22 and 23–29 age groups (conversion proxy `p*M`, t50 index)
- **Outputs**:
  - Fitted curves & residual plots (saved in `figs/`)
  - Sensitivity heatmaps for terminal penetration and t50
  - Simulated datasets (saved in `data/`)

### 2. Q2_factcheck_SIR_SR
- **Model**: Improved SIR propagation model (integrating fact-checking intensity `If` and intervention delay `Delta`)
- **Key Tasks**:
  - Define false news suppression rate (SR)
  - Analyze correlation between verification timeliness and suppression effect
  - Explore impacts of different fact-checking intensities on propagation dynamics
- **Outputs**:
  - Propagation curves under varying fact-checking intensities
  - SR vs. intervention delay (Delta) plot
  - 2D heatmap of SR with respect to `If` and `Delta`

### 3. Q3_platform_migration
- **Model**: Multi-platform coupled user migration dynamics model
- **Key Tasks**:
  - Introduce platform attractiveness coefficient (related to features, algorithms, content quality)
  - Simulate user share evolution of TikTok, YouTube, and Instagram
  - Predict steady-state market share after TikTok's algorithm optimization (+20% attractiveness)
- **Outputs**:
  - User share trajectory comparison (baseline vs. optimized scenario)
  - Steady-state share comparison bar chart
  - Sensitivity heatmap for TikTok's share gain

### 4. Q4_optimization_policy
- **Model**: Multi-objective optimization model (weighted by SR and normalized cost)
- **Key Tasks**:
  - Construct optimization function with news dissemination effectiveness and cost constraints
  - Solve optimal fact-checking strategies under different weight preferences
  - Analyze strategy robustness under varying cost coefficients
- **Outputs**:
  - Cost-SR trade-off curve for optimal policies
  - Optimal strategy comparison under different cost weights
  - Quantitative results of optimal `If` (intensity) and `Delta` (delay)

## Environment Requirements
- Python 3.8+
- Dependencies:
