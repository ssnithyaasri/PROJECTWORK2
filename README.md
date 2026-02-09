# PROJECTWORK2-Mask-Ratio-Guided Multi-Task Learning for Plant Disease Classification and Severity Prediction

This repository presents a severity-aware deep learning framework for plant disease analysis using image-based inputs. The proposed approach integrates disease classification and severity estimation into a unified multi-task learning pipeline and introduces a post-hoc severity-based evaluation strategy to assess model robustness beyond conventional accuracy metrics.

---

## 🔍 Problem Motivation

Traditional plant disease classification systems evaluate performance using aggregate metrics such as accuracy and F1-score. These metrics fail to capture how model reliability varies across different disease severity levels. In real-world agricultural applications, errors on high-severity cases are far more critical than errors on mild cases.

This project addresses this limitation by:
- Predicting disease category and severity simultaneously
- Using mask-ratio–based severity supervision
- Evaluating performance using severity-wise accuracy analysis

---

## 🧠 Proposed Methodology

- **Backbone**: DenseNet121 (ImageNet pretrained)
- **Learning Strategy**: Multi-task learning
- **Outputs**:
  - Disease classification (multi-class)
  - Severity prediction (continuous value ∈ [0,1])
- **Loss Function**:
  - Severity-aware focal loss for classification
  - Mean Absolute Error (MAE) for severity regression
- **Training Optimizations**:
  - Mixed-precision training
  - GPU acceleration
  - Fine-tuning of upper backbone layers

---

## 📊 Severity-Aware Evaluation

Instead of relying only on overall accuracy, predictions are grouped into predefined severity bins.  
Severity-wise accuracy is computed to analyze how model performance varies across:

- Mild disease cases
- Moderate disease cases
- Severe disease cases

This provides fine-grained interpretability and robustness assessment without modifying the trained model.

---
## Output

<img width="981" height="484" alt="image" src="https://github.com/user-attachments/assets/24d43725-dc19-47dd-860e-1ea05f0e5d54" />
<img width="630" height="560" alt="image" src="https://github.com/user-attachments/assets/2a70ad1d-bf21-4131-8e3b-7919d7501911" />
<img width="618" height="512" alt="image" src="https://github.com/user-attachments/assets/940b8427-9e91-4ac3-80aa-eec28db8a817" />
<img width="860" height="424" alt="image" src="https://github.com/user-attachments/assets/9c01eb0b-75a6-4a1e-8c74-50383da03293" />




---

## Conclusion

This project presents a severity-aware multi-task learning framework for plant disease classification using deep learning. By jointly predicting disease type and severity, the system provides more informative and interpretable outputs. Severity-wise evaluation exposes performance variations that are hidden by traditional metrics. The framework is lightweight, model-agnostic, and suitable for real-world agricultural applications. Overall, it improves robustness assessment and reliability of disease diagnosis systems.


```
