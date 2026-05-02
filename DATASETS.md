# DATASETS

This document describes the datasets used in this study and their role within the PBPK–PD–Viral Dynamics framework.


## 1. Singapore NCID Paxlovid Cohort

**Description**  
A real-world clinical dataset comprising patients treated with nirmatrelvir–ritonavir (Paxlovid) during the Omicron wave in Singapore.

**Contents**
- Longitudinal viral load measurements (RT-PCR, log10 copies/mL)
- Treatment information (dose, timing, duration)
- Patient demographics (age, sex)
- Clinical covariates (e.g., comorbidities, renal function where available)

**Usage in Study**
- Primary dataset for **model calibration and validation**
- Used to:
  - Fit viral dynamics parameters
  - Evaluate treatment strategies
  - Quantify viral rebound dynamics

**Availability**
- Not publicly available due to data governance and patient confidentiality
- Access subject to institutional approval (NCID / NUHS)

---

## 2. NBA SARS-CoV-2 Viral Load Dataset

**Source**
- Public dataset from NBA cohort (Hay et al., Owens et al.)

**Reference**
- Owens et al., *JCI Insight*, 2024 :contentReference[oaicite:0]{index=0}

**Description**
A large longitudinal dataset capturing SARS-CoV-2 viral kinetics with frequent testing independent of symptoms.

**Contents**
- ~1,500 infections with ≥4 viral load measurements
- High-frequency sampling including presymptomatic phase
- Variant information (pre-VOC, Alpha, Delta, Omicron)
- Vaccination and reinfection status

**Usage in Study**
- Used for:
  - Model structure validation
  - Parameter initialization
  - Understanding heterogeneity in viral dynamics
- Supports mechanistic assumptions on:
  - Immune response timing
  - Viral rebound mechanisms
  - Shedding variability

**Availability**
- Publicly available via GitHub (original study repository)

---

## 3. Mainland China Viral Load Dataset

**Description**
Aggregated viral load dataset from published studies of untreated SARS-CoV-2 infection.

**Contents**
- Viral load trajectories across infection time
- Symptom onset alignment data
- Population-level viral kinetics

**Usage in Study**
- Used for:
  - Infection time alignment (incubation shift)
  - Baseline viral dynamics calibration
  - Supporting untreated infection trajectories

**Availability**
- Derived from published literature (various studies)

---

## 4. Hong Kong Viral Dynamics Dataset

**Description**
Subject-level dataset containing longitudinal viral load measurements.

**Contents**
- Individual-level viral load time series
- Clinical and epidemiological annotations (where available)

**Usage in Study**
- Used for:
  - External validation of viral kinetics
  - Cross-cohort consistency checks
  - Supporting untreated infection modeling

**Availability**
- Not publicly distributed; derived from collaborator/shared datasets

---

## 5. PBPK Simulation Data (Simcyp)

**Description**
Simulated pharmacokinetic profiles of nirmatrelvir–ritonavir generated using Simcyp.

**Contents**
- Plasma concentration-time profiles
- Virtual populations (e.g., healthy, elderly, CKD)
- Different dosing regimens

**Usage in Study**
- Used as **input driver for PD/viral dynamics model**
- Enables:
  - Exposure-response analysis
  - Treatment strategy evaluation
  - Virtual cohort simulations (~10⁵–10⁶ scenarios)

**Availability**
- Not publicly available (Simcyp license required)
- Can be reproduced using the same model setup

---

## 6. Virtual Cohort Dataset (Generated)

**Description**
Synthetic dataset generated through simulation.

**Contents**
- ~720,000 simulated patient–strategy combinations
- Physiological variability (age, comorbidities, renal function)
- Treatment strategies (dose, timing, duration, adherence)
- Outcome metrics:
  - Viral suppression
  - Rebound probability
  - Time to clearance

**Usage in Study**
- Core dataset for:
  - Strategy optimisation
  - Machine learning analysis
  - Risk stratification

**Availability**
- Derived data may be shared upon request
- Full dataset not publicly hosted due to size

---

## Notes on Data Handling

- All patient-level data were de-identified prior to analysis
- Ethical and institutional approvals were obtained where required
- No identifiable patient information is included in this repository

---

## Reproducibility

- Scripts for processing and analysis are available in `code/`
- Example or synthetic datasets may be provided where possible
- Full reproducibility requires:
  - Access to restricted clinical datasets
  - Simcyp PBPK simulation setup

---
