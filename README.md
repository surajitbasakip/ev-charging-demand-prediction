# User-Based Future EV Charging Demand Prediction

## Overview
This project implements a deep learning model using a three-layer Deep Neural Network (DNN) to predict the future energy demand of a user for their Electric Vehicle (EV). The model is trained on a Kaggle dataset that contains sessions from 85 EV drivers with repeat usage at 105 charging stations across 25 sites within a workplace charging program. 

The dataset is split in temporal order, allowing the model to learn from past energy consumption patterns and predict future demand. Due to the relatively small dataset, the model converges quickly.

## Dataset Preprocessing
### Cleaning Steps:
- Incorrect date formats such as `'0014-11-18'` are corrected to `'2014-11-18'`.
- Irrelevant columns like `'dollars'`, `'manager vehicle'`, etc., are dropped.
- Data is split into train-test sets in temporal order.
- Weekdays are already one-hot encoded.
- User IDs and Location IDs are embedded in dense vectors of dimension 16.

## Model Architecture
- Three-layer Deep Neural Network (DNN)
- Input features include historical charging data, user embeddings, and location embeddings
- Mean Squared Error (MSE) is used as the cost function for optimization

## Installation
To run this project, install the required dependencies:

```bash
pip install tensorflow pandas numpy matplotlib scikit-learn
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ev-charging-demand-prediction.git
   cd ev-charging-demand-prediction
   ```
2. Ensure the dataset file `ev_charging_station.txt` is placed in the correct directory.
3. Open the Jupyter Notebook `ev_charging_v2.ipynb` and run the cells to train and evaluate the model.

## Results
- The model converges quickly due to the limited dataset size.
- Evaluation is performed using MSE to measure prediction accuracy.

## Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License.

---
### Contact
For questions or collaborations, reach out at [surajitbasakip@gmail.com].
