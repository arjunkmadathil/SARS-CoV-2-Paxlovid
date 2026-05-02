flowchart TD

A1["Singapore NCID Paxlovid Cohort<br>Treated patients<br>Longitudinal viral load<br>Clinical covariates"]
A2["China Untreated Omicron Dataset<br>Population viral kinetics<br>Control viral load trajectories"]
A3["Hong Kong Viral Load Dataset<br>Subject-level untreated viral loads<br>External viral dynamics comparison"]
A4["PBPK Simulation Dataset<br>Nirmatrelvir concentration-time profiles<br>Virtual populations and dosing regimens"]

B1["Data harmonisation<br>Ct to log10 viral load conversion<br>Infection-time alignment<br>LOD handling"]
B2["PBPK exposure processing<br>Concentration-time profiles<br>Age-sex mapping<br>Exposure interpolation"]

C1["Untreated viral dynamics model<br>Susceptible, refractory, infected cells, virus<br>Innate and acquired immune response"]
C2["Treated PBPK-PD-VD model<br>PBPK-driven drug exposure<br>PD inhibition of viral production<br>Treatment-related parameter estimation"]

D1["Control model fitting<br>Baseline viral kinetics<br>Reference untreated population"]
D2["Treated model fitting<br>Singapore Paxlovid cohort<br>Drug effect and immune-response parameters"]

E1["Virtual cohort simulations<br>Large-scale patient-strategy simulations<br>Timing, dose, duration, adherence"]
E2["Subgroup analysis<br>Healthy adults, older adults, CKD<br>DM and comorbidity subgroups"]
E3["Rebound analysis<br>End-of-treatment viral burden<br>Post-treatment viral regrowth<br>Rebound probability and magnitude"]
E4["Mechanistic counterfactual simulations<br>One-factor-at-a-time regimen changes<br>Individual-level mechanistic interpretation"]
E5["Viral phenotype analysis<br>Early-clearance and late-clearance phenotypes<br>Phenotype-specific treatment response"]

F1["Outcome metrics<br>Viral suppression<br>Time to negativity<br>Viral rebound probability<br>Rebound magnitude"]
F2["Mechanistic interpretation<br>Drug exposure<br>Immune activation timing<br>Residual viral burden<br>Treatment optimisation"]

A1 --> B1
A2 --> B1
A3 --> B1
A4 --> B2

B1 --> C1
B2 --> C2
C1 --> D1
D1 --> C2
C2 --> D2

D1 --> E1
D2 --> E1
E1 --> E2
E1 --> E3
E1 --> E5
D2 --> E4

E2 --> F1
E3 --> F1
E4 --> F1
E5 --> F1
F1 --> F2
