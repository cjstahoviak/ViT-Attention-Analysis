# ViT-Attention-Analysis
A research toolkit for analyzing and visualizing attention mechanisms in Vision Transformers (ViT). Explores how different attention heads and layers process visual information, with tools for generating attention maps and overlays.

# Lab steps

From the following list, chose at least 4 points (marked in parenthesis) and implement the suggested improvements. Note that you can also select and implement your own improvements to the lab. The goal is for you to gain some practical experience dealing with vision transformers and attention mechanisms.

---

### 1. **Compare Attention Across Layers** (1 pt) ✅

Observe how attention patterns evolve from early to deeper layers

- Modify the visualization code to extract and visualize attention maps from **multiple layers**, and overlay them over the analysis image..
- Plot them side-by-side for comparison.
- Describe how attention focuses shift from broad/global in early layers to fine/local in deeper ones.


---

### 2. **Compare Attention Across Heads** (1 pt) ✅

See how different heads focus on different regions.

- Instead of averaging attention across all heads, visualize each head separately.
- Identify if some heads focus on textures, edges, or object parts.

---

### 3. **Compare ViT vs CNN Attention** (2 pts)

Contrast global vs local focus.

- Run a CNN (e.g., ResNet) with Grad-CAM on the same image.
- Compare the attention overlay to the ViT visualization.


---

### 4. **Visualize Attention for Misclassified Images** (1 pt)

Diagnose model behavior.

- Feed images the model misclassifies.
- Visualize where it looked via class token attention.
- Figure out why the model failed.


---

### 5. **Use Different Patch Sizes** (1 pt)

Investigate effect of patch resolution.

- Change the model (e.g., `vit_base_patch32_224`) to use a larger patch size.
- Re-run visualizations and compare granularity.


---

### 6. **Visualize Attention Rollout** (3 pts)

Understand cumulative attention across layers.

- Implement **attention rollout** (recursive multiplication of attention matrices).
- Visualize the result for each token’s final impact on the class token.

**Resources**: [Abnar & Zuidema 2020](https://arxiv.org/abs/2005.00928)


---

### 7. **Finetune ViT on Custom Dataset and Visualize Attention**  (2 pts)

Apply ViT to a new task and study adaptation.

- Use a small dataset like CIFAR-10 or Oxford Pets.
- Finetune a ViT model and compare attention before/after finetuning.
- Hypothesize what changes and why.


---

### 8. **Propose and implement your own** (points vary)

Propose your own extension in a way that can potentially help you deepen your understanding of ViTs and/or help you with the final project. Talk to me to decide on the number of points