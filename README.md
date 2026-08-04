# Eurovision 2026 Analysis 📊🎶

This repository contains an advanced, data-driven analysis of the **Eurovision Song Contest 2026 Grand Final**. By combining official contest voting data (Jury + Televote split) with real-time digital engagement metrics from the **YouTube Data API v3**, this project explores the alignment between contest scoring, viral popularity, and audience sentiment.

---

## 🌟 Key Features & Advanced Methodology

1. **Jury vs. Televote Split**: Separates official jury scores from public televoting results to isolate expert consensus vs. viewer fanbases.
2. **Multiple Linear Regression (OLS)**: Models how jury points and televotes independently drive digital reach on YouTube ($R^2$, $p$-values, residuals).
3. **K-Means Clustering**: Segments performing acts into distinct performance archetypes based on scaled points, viewership, engagement rates, and sentiment scores.
4. **NLP Sentiment Analysis**: Uses TextBlob to process top YouTube comments and compute a **Sentiment Index** for each live performance.
5. **Engagement Metrics & Anomaly Detection**:
   - **Engagement Rate (%)**: $\frac{\text{Likes} + \text{Comments}}{\text{Views}} \times 100\%$
   - **Views-Per-Point (VPP)**: Quantifies "viral power" per contest point.
   - **Residuals Analysis**: Identifies over-performing and under-performing acts relative to theoretical expectations.

---

## 🛠️ Technical Stack

- **Language**: Python 3
- **Data Engineering & Analysis**: `pandas`, `numpy`, `scipy`, `statsmodels`, `scikit-learn`
- **Natural Language Processing (NLP)**: `textblob`
- **Visualization**: `plotly` (3D Scatter Matrices & Interactive Bar Charts)
- **API Integration**: YouTube Data API v3 (`google-api-python-client`)

---

## 📊 Summary Table of Metrics

| Metric | Definition | Practical Insight |
| :--- | :--- | :--- |
| **OLS Regression ($R^2$)** | Explanatory power of points over YouTube views. | Quantifies how much variance in viewership is driven by jury vs. televote points. |
| **K-Means Cluster** | Multi-variable grouping of acts. | Categorizes entries (e.g., *Viral Hits*, *Jury Darlings*, *Low Engagement*). |
| **Sentiment Index** | Polarity score derived from top YouTube comments. | Measures public reception beyond simple view counts. |
| **OLS Residuals** | Difference between actual and predicted views. | Highlights viral breakouts or digital reach gaps. |

---

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone [https://github.com/juliaagnieszkaguminska/Eurovision-2025---Analysis.git](https://github.com/juliaagnieszkaguminska/Eurovision-2025---Analysis.git)
