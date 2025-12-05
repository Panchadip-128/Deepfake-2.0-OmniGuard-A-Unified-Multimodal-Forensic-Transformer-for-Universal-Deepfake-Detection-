# OmniGuard — A Unified Multimodal Deepfake Detection & Provenance Framework

OmniGuard is a novel research framework targeting **A\*/A+ conference–level deepfake forensics**.  
It introduces the first unified system capable of:

- Video deepfake detection  
- Audio spoof detection  
- Lip-sync + biometric consistency analysis  
- Metadata & forensic artifact reasoning  
- Editing Chain Reconstruction (ECR): predicting manipulation operator sequences  
- Operator Embedding Space (OES): representing each manipulation type as a learnable vector  

This research is **non-incremental**, **multimodal**, and **provenance-aware**, aiming for top-tier venues (CVPR, ICCV, NeurIPS, ICLR, ICASSP).

---

##  Responsible Use Policy

- This repository **does NOT generate deepfakes**.  
- No manipulated media is included.  
- Only **detection, analysis, provenance, and evaluation** code is provided.  
- Users must rely solely on **public datasets** such as FF++, DFDC, Celeb-DF, WaveFake, ASVspoof, etc.  
- Privately created operator-labelled samples must **never be redistributed**.  

OmniGuard complies with Responsible AI and A*/A+ conference ethics guidelines.

##  Key Research Novelties

OmniGuard introduces nine major innovations:

### 1. Unified Multimodal Deepfake Forensics
First system to jointly analyze **video + audio + biometric + metadata** signals in one model.

### 2. Editing Chain Reconstruction (ECR)
Predicts the manipulation sequence (e.g., FaceSwap → Wav2Lip → NeuralTTS → Recompress).  
A brand-new task in the deepfake forensics community.

### 3. Operator Embedding Space (OES)
Each manipulation type is represented as a **learnable operator vector**.

### 4. Cross-modal Artifact–Operator Contrastive Learning (CAOCL)
Aligns multimodal artifacts to operator embeddings.

### 5. Provenance-Aware Loss Framework
Combines:
- detection loss  
- ECR loss  
- operator contrastive loss  
- calibration loss (Brier score)

### 6. Multimodal Inconsistency Profiling (MIP)
Models:
- lip-sync mismatch  
- face–voice identity mismatch  
- temporal AV inconsistencies  
- compression/metadata irregularities  

### 7. Compositional Multimodal Benchmark Protocol
Built on public datasets; supports operator-labelled evaluation **without releasing any fakes**.

### 8. Operator-aware Meta-Learning
Zero-shot generalization to unseen manipulation families.

### 9. Safe Artifact Release Policy
Only operator vocab, weights, and evaluation code are released.  
No manipulated media is included.

---

## 📁 Dataset Setup

### Supported public datasets:
- FaceForensics++  
- DFDC  
- Celeb-DF  
- WildDeepfake  
- ASVspoof 2019/2021  
- WaveFake  

### Required CSV format (`annotations.csv`)

---

# **SECTION 5 — METRICS + CITATION + DISCLAIMER**

```markdown
## 📊 Evaluation Metrics

### Detection
- AUC  
- EER  
- Brier Calibration Score  

### ECR (Editing Chain Reconstruction)
- Operator sequence edit distance  
- Token-level accuracy  
- BLEU score  

### Multimodal consistency
- Lip-sync error  
- Face↔voice identity distance  
- AV misalignment score  

---

---

## Disclaimer
This repository is intended **strictly for defensive research**.  
It must not be used to generate, distribute, or promote manipulated media and if used authors are kindly requested to acknowledge this contribution if ever this is used for any kind; even if a part of this has been put into use.

The authors and contributors are not responsible for misuse.