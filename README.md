# VBS_TRIGGER_PLOTS

This analysis reproduces trigger efficiencies for VBF and MET categories using NanoAODv15 for Summer24 RUN3 VBSWZJJ To Jets + MET samples.

The efficiencies are computed as:

$\epsilon = \frac{N_{\text{events passing HLT}}}{N_{\text{offline baseline}}}$

with Clopper–Pearson confidence intervals as is proposed in [Ref. Triggers Run3](https://cds.cern.ch/record/2875709/files/DP2023_076.pdf).

### VBF topology baseline

For the forward jets, it was selected the two AK4 jets with maximum $m_{jj}$.


$ N_{jets}^{AK4} \ge 2 $
$ p_T(j_1) > 60~\mathrm{GeV}$, $\quad p_T(j_2) > 45~\mathrm{GeV} $
$ m_{jj} > 500~\mathrm{GeV}$, $\quad |\Delta\eta(j_1,j_2)| > 2.5 $

This defines denom_VBS — the common baseline for all categories.

# Triggers VBF:
| VBF TRIGGERS RUN3 SUMMER 24 (NanoAODV15)| 
| ------------ | 
| HLT_VBF_DiPFJet125_45_Mjj1050 | 
| HLT_VBF_DiPFJet125_45_Mjj1200 | 
| HLT_VBF_DiPFJet75_45_Mjj800_DiPFJet60 | 
| HLT_VBF_DiPFJet75_45_Mjj850_DiPFJet60 | 
| HLT_VBF_DiPFJet80_45_Mjj650_PFMETNoMu85 | 
| HLT_VBF_DiPFJet80_45_Mjj750_PFMETNoMu85 | 

<img width="1472" height="832" alt="vbf_eff_vs_mjj" src="https://github.com/user-attachments/assets/b454819c-8195-4dd6-a454-d18def0dd6a6" />
