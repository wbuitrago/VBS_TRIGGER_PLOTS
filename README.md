# VBS_TRIGGER_PLOTS

This analysis reproduces trigger efficiencies for VBF and MET categories using NanoAODv15 for Summer24 RUN3 VBSWZJJ To Jets + MET samples.

The efficiencies are computed as:

$\epsilon = \frac{N_{\text{events passing HLT}}}{N_{\text{offline baseline}}}$

with Clopper–Pearson confidence intervals as is proposed in [Ref. Triggers Run3](https://cds.cern.ch/record/2875709/files/DP2023_076.pdf).

### VBF topology baseline

For the forward jets, it was selected the two AK4 jets with maximum $m_{jj}$.


$N_{jets}^{AK4} \ge 2$
$p_T(j_1) > 20~\mathrm{GeV}$, $\quad p_T(j_2) > 20~\mathrm{GeV}$
$m_{jj} > 500~\mathrm{GeV}$, $\quad |\Delta\eta(j_1,j_2)| > 2.5$

This defines denom_VBS — the common baseline for all categories.

### MET Selection

For both resolved and boosted categories:

$E_T^{miss} = PuppiMET_{pt} > 250~\mathrm{GeV}.$

### W reconstruction (Resolved Category)

The resolved W candidate is built from central AK4 jets in the event.

Jets are considered central if they satisfy:

$|\eta| \le 2.4$,$\qquad p_T > 25~\mathrm{GeV}$.

All possible pairs $(j_1, j_2)$ of these central jets are formed. Among all dijet pairs, the one whose invariant mass is closest to $m_W = 80.4~\mathrm{GeV}$

A mass window requirement is applied around the W pole mass:

$|m_{jj}^{(W)} - 80.4~\mathrm{GeV}\,| < 15~\mathrm{GeV}.$

Events that satisfy the above conditions are marked as hasW_res = True — meaning a valid resolved W candidate exists.

The transverse momentum p_T(W) used in the efficiency plots is that of this dijet candidate.

### W reconstruction (Boosted Category)

The boosted W candidate is reconstructed from AK8 Fatjets.

FatJets are required to satisfy:

$p_T > 200~\mathrm{GeV}$, $\qquad |\eta| < 2.4.$

Only jets with a soft-drop mass compatible with a W boson are kept:

$65 < m_{\text{SD}} < 105~\mathrm{GeV}$.

Candidate selection:

Among all AK8 jets passing the above cuts, the jet with a soft-drop mass closest to $m_W = 80.4~\mathrm{GeV}$ is selected as the boosted W candidate.

Events with at least one such candidate are marked as hasW_boost = True.

The transverse momentum $p_T(W)$ in the boosted efficiency plots corresponds to the selected AK8 jet p_T.


### Triggers VBF:

| VBF TRIGGERS RUN3 SUMMER 24 (NanoAODV15)| 
| ------------ | 
| HLT_VBF_DiPFJet125_45_Mjj1050 | 
| HLT_VBF_DiPFJet125_45_Mjj1200 | 
| HLT_VBF_DiPFJet75_45_Mjj800_DiPFJet60 | 
| HLT_VBF_DiPFJet75_45_Mjj850_DiPFJet60 | 
| HLT_VBF_DiPFJet80_45_Mjj650_PFMETNoMu85 | 
| HLT_VBF_DiPFJet80_45_Mjj750_PFMETNoMu85 | 


<img width="1472" height="832" alt="vbf_eff_vs_mjj" src="https://github.com/user-attachments/assets/b454819c-8195-4dd6-a454-d18def0dd6a6" />

### Triggers MET:

## Boosted
<img width="1472" height="832" alt="vbf_eff_vs_pTW_boosted" src="https://github.com/user-attachments/assets/75f4f7c9-672d-4d9c-8090-010ed8ff7ca0" />




