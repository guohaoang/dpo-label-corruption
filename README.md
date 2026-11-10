# Random Noise or Systematic Bias? Label Corruption in DPO

Course project for Stanford CS329H (Machine Learning from Human Preferences), Autumn 2026.

**Question.** At a fixed fraction of flipped preference labels, does it matter whether the
flips are random or aligned with response length? And do the KL strength β and noise-robust
losses (cDPO, rDPO) protect against the two kinds of corruption equally?

**Design.** The same preference pairs are corrupted at the same flip rate in two ways
(uniformly at random, and targeted so the longer response wins). A small language model is
then trained with DPO across β and across losses. The primary outcome is how much longer
the trained policy's generations become, relative to a clean-label run.

## Status

Pre-analysis stage. No experiments have been run and there is no experiment code yet.
Code, setup instructions and reproduction steps will be added here as the project proceeds.

## Planned layout

```
configs/    one configuration file per run
src/        data corruption, training (DPO / cDPO / rDPO), evaluation, plotting
scripts/    end-to-end and quickstart entry points
results/    metrics and figures produced by the scripts
```
