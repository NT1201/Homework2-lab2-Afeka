# Homework2-lab2-Afeka

### Power Consumption Prediction Using RNN, LSTM, and LSTM with Attention

This project predicts household power consumption using RNN, LSTM, and LSTM with Attention models. Various experiments were conducted to evaluate model performance under different conditions: data augmentation, data reduction, and changes in data resolution.

### Assumptions

1. **Epochs**: Models were trained for 2 epochs due to limited computational resources. More epochs could improve results in a real-world scenario.

### Explanation of the Work

We utilized the "Individual household electric power consumption" dataset from the UCI Machine Learning Repository to build and evaluate three models: RNN, LSTM, and LSTM with Attention. The goal was to understand how each model performs under different data conditions and to identify which model is most robust.

### Experiments Conducted

1. **Base Performance**: Evaluated the performance of each model without any data modifications.
2. **Data Augmentation**: Added noise to up to 10% of the data and assessed the impact on model performance.
3. **Data Reduction**: Removed up to 10% of the data and analyzed the effect on each model's accuracy.
4. **Data Resolution**: Reduced the time resolution of the data by 50% and observed changes in model performance.

### Conclusions

- **Base Scenario**: LSTM with Attention performed best, leveraging the attention mechanism to capture intricate patterns in the data.
- **Noisy Data**: LSTM was the most stable, handling noise well with minimal performance drop.
- **Reduced Data**: LSTM showed robustness, maintaining performance better than RNN and significantly better than LSTM with Attention.
- **Reduced Time Resolution**: LSTM with Attention excelled, demonstrating its ability to handle lower resolution data effectively.

### Insights on Dataset Characteristics

- **Temporal Patterns**: The dataset contains strong temporal patterns, making LSTM and LSTM with Attention particularly effective due to their ability to capture sequential dependencies.
- **Noise Sensitivity**: LSTM models handle noise better, likely due to their inherent gating mechanisms that manage information flow.
- **Data Dependency**: LSTM with Attention, while powerful, shows higher sensitivity to data quantity, requiring more data to perform optimally.
- **Resolution Changes**: The ability of LSTM with Attention to maintain performance with reduced resolution indicates its strong pattern recognition capabilities, making it suitable for varied data granularity.
