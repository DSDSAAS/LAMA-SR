Rope only version.

This project is used together with [BasicSR](https://github.com/xinntao/BasicSR).
# concise abstract
Objective  
Remote sensing image super-resolution (RSISR) aims to recover high-resolution (HR) images from low-resolution inputs, yet current CNN- and Transformer-based methods struggle to balance local texture reconstruction, global dependency modeling, and computational cost. Although Mamba offers efficient long-range modeling, its direct application to vision suffers from unidirectional scanning, broken 2D structure, and weak local semantics.  
Method  
We propose LAMA-SR, a local-aware Mamba framework tailored for RSISR. To preserve spatial continuity, a 2D rotary position embedding (RoPE-2D) is first applied to encode relative geometry before scanning. The enriched features are then processed by a Two-Dimensional Selective Scan (SS2D) for efficient global modeling. To strengthen local detail reconstruction, we introduce a Multi-Scale Mixture-of-Experts (MoE) Local Information Aggregator (LIA) that extracts small-, medium-, and large-receptive-field features, with a lightweight channel-attention–based soft routing mechanism to adaptively fuse them according to image content.  
Results  
Experiments on UCMerced, RSSCN7, AID, and WHU-RS19 datasets under ×2, ×3, and ×4 upscaling show that LAMA-SR consistently outperforms CNNs, Transformers, and Mamba-based baselines. On UCMerced ×4, LAMA-SR achieves 29.26 dB PSNR with only 8.10M parameters and 20.23G FLOPs, surpassing MambaIR by a large margin. Ablation results confirm that RoPE-2D improves spatial coherence, while LIA enhances texture recovery.  
Conclusion  
LAMA-SR effectively integrates global modeling efficiency with strong local fidelity, producing sharper boundaries and more natural textures while maintaining a favorable accuracy–efficiency balance. The results demonstrate that state-space models can be well adapted to high-resolution remote sensing imagery, offering a promising direction for lightweight super-resolution research.
# result
<img width="1185" height="829" alt="Graph1" src="https://github.com/user-attachments/assets/a0331f59-635d-4d1b-b827-604744dc9540" />  

# dataset
[UCMerced](http://weegee.vision.ucmerced.edu/datasets/landuse.html)  
[RSSCN7](https://github.com/palewithout/RSSCN7)  
[AID](https://github.com/palewithout/RSSCN7)  
[WHU-RS19](https://github.com/palewithout/RSSCN7)  
