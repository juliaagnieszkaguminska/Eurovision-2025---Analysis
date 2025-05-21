# Eurovision 2025 Analysis 

I am a Eurovision fan, thus I created this project.
This repository contains a comprehensive data-driven Eurovision Song Contest 2025 Grand Final analysis. Using official jury and public voting results alongside real-time YouTube view counts, we explore the relationship between contest performance and audience engagement.

## Key Components

1. **Data Collection**
   - **Points**: Official Grand Final scores (Jury + Televote).
   - **YouTube Views**: Real-time view counts from the Eurovision channel for each live performance video.
   - (Optional) **Spotify Streams**: Proxy for longer-term streaming popularity.

2. **Metrics & Methodology**
   - **Pearson Correlation (r)**: Measures linear association between contest points and YouTube view counts.
   - **Linear Regression & R²**: Quantifies how well points predict viewership; slope indicates average views gained per point.
   - **Views-Per-Point (VPP) Index**: A single KPI that normalizes view counts by score to flag over- and under-performing acts.
   - **Outlier Detection**: Identifies acts that significantly over- or under-performed relative to their jury/public score.

3. **Technical Stack**
   - **Python**: Pandas for data wrangling, Plotly for interactive visualizations.
   - **YouTube Data API v3**: Automated retrieval of view counts (requires API key).
   - **Google Colab**: Reproducible notebook environment.

## Insights & Highlights

- **Strong but Incomplete Alignment**: Pearson r ≈ 0.77 highlights a robust correlation—higher-scoring acts generally attract more views, but ~40% of viewership variance lies outside of vote totals.
- **Predictive Power**: Linear regression reveals that each additional contest point corresponds to ~14 k extra YouTube views on average (R² ≈ 0.59).
- **Viral Champions & Gaps**:
  - 🇦🇹 *Austria* over-delivered by +2 200 views/pt (highest VPP).
  - 🇮🇹 *Italy* under-performed by –10 000 views/pt, suggesting a “digital reach gap.
  - <h3>Practical Metric Breakdown</h3>

<table>
  <thead>
    <tr>
      <th><strong>Metric</strong></th>
      <th><strong>What It Means</strong></th>
      <th><strong>Why It Matters</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Pearson Correlation (r)</strong></td>
      <td>Shows how closely contest points align with YouTube views.</td>
      <td>High r (e.g., 0.77) means performances that score well also draw strong online interest.</td>
    </tr>
    <tr>
      <td><strong>Linear Regression & R²</strong></td>
      <td>Estimates how many views each point brings; R² shows prediction accuracy.</td>
      <td>Each point ≈ 14k extra views; R² = 0.59 means points explain 59% of view count variance.</td>
    </tr>
    <tr>
      <td><strong>Views-Per-Point (VPP)</strong></td>
      <td>Normalizes view count by score to show “viral power”.</td>
      <td>High VPP = underrated but viral; low VPP = scored well but lacked digital traction.</td>
    </tr>
    <tr>
      <td><strong>Outlier Detection</strong></td>
      <td>Flags acts whose views diverge sharply from their scores.</td>
      <td>Helps spot hidden hits or acts that didn’t resonate despite scoring high.</td>
    </tr>
  </tbody>
</table>

    **Actionable Roadmap**:
  1. **Enrich the Model**: Incorporate artist Spotify followers, social media buzz, and TikTok activity to improve explanatory power.
  2. **Real-Time Tracking**: Schedule automated API pulls to capture view spikes and engagement surges.
  3. **Embed VPP KPI**: Use the Views-Per-Point index as a standard metric for future contests and marketing strategies.


**Author:** Julia Agnieszka G
**Date:** May 2025

*Transforming contest data into strategic audience insights.*
