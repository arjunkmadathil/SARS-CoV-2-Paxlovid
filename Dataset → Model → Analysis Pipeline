```mermaid
flowchart TD

%% ======================
%% DATA SOURCES
%% ======================

A1[Singapore NCID Paxlovid Cohort<br/>• Treated patients<br/>• Longitudinal viral load<br/>• Clinical covariates]

A2[NBA Viral Load Dataset<br/>• Untreated infections<br/>• High-frequency sampling<br/>• Variant & immune context]

A3[China / Hong Kong Datasets<br/>• Viral kinetics<br/>• Infection timing alignment]

A4[PBPK Simulations (Simcyp)<br/>• Nirmatrelvir exposure<br/>• Different doses & populations]

%% ======================
%% PREPROCESSING
%% ======================

B1[Data Harmonisation<br/>• Viral load standardisation<br/>• Time alignment (infection onset)<br/>• Log transformation]

B2[PBPK → PD Input Mapping<br/>• Concentration-time profiles<br/>• Interpolation to observation grid]

%% ======================
%% MODEL CORE
%% ======================

C1[Mechanistic Viral Dynamics Model<br/>• Target cell limited structure<br/>• Innate + adaptive immunity<br/>• Drug effect (Emax)]

%% ======================
%% FITTING
%% ======================

D1[Control (Untreated) Fitting<br/>• Estimate baseline viral kinetics<br/>• Immune parameters]

D2[Treated (Paxlovid) Fitting<br/>• Drug effect calibration<br/>• PBPK-driven forcing]

%% ======================
%% ANALYSIS BLOCKS
%% ======================

E1[Rebound Analysis<br/>• Post-treatment dynamics<br/>• Immune–drug interplay<br/>• Stability behavior]

E2[Mechanistic Counterfactuals<br/>• Timing shifts<br/>• Dose variations<br/>• Duration changes]

E3[Virtual Cohort Simulation<br/>• Large-scale sampling<br/>• Parameter variability<br/>• Scenario expansion]

E4[Subgroup Analysis<br/>• Age<br/>• CKD<br/>• Comorbidities<br/>• Exposure differences]

%% ======================
%% OUTPUTS
%% ======================

F1[Outcome Metrics<br/>• Viral suppression<br/>• Time to clearance<br/>• Rebound probability]

F2[Mechanistic Insights<br/>• Drivers of rebound<br/>• Role of immune timing<br/>• Exposure–response relationships]

%% ======================
%% FLOW CONNECTIONS
%% ======================

A1 --> B1
A2 --> B1
A3 --> B1

A4 --> B2

B1 --> C1
B2 --> C1

C1 --> D1
C1 --> D2

D1 --> E1
D2 --> E1

D1 --> E2
D2 --> E2

D1 --> E3
D2 --> E3

E3 --> E4

E1 --> F1
E2 --> F1
E3 --> F1
E4 --> F1

F1 --> F2
