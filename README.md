# TensorFlow-ZTM

[Project portfolio](https://fyemane.github.io/projects.html) · [About me, experience & qualifications](https://fyemane.github.io/)


My notebooks and projects from Zero to Mastery's TensorFlow Developer Certificate course, which I completed in 2023. I used TensorFlow and Keras to explore regression, classification, computer vision, transfer learning, natural language processing, and time-series forecasting.

This repository follows my progress through the course: starting with tensors and simple models, then working through pretrained image models, multi-input NLP architectures, and forecasting experiments. The notebooks include course-guided implementations, my notes, experiments, and saved outputs.

[View my course completion certificate](https://www.udemy.com/certificate/UC-755a9a4b-65ec-4741-a86a-808ef0e28191/).

## Notebook guide

The files retain their original course numbering. There is no notebook numbered `07` in this repository.

| Notebook | Focus |
| --- | --- |
| [00 — TensorFlow fundamentals](00_tensorflow_fundamentals.ipynb) | Creating and manipulating tensors, shapes and ranks, indexing, matrix operations, NumPy interoperability, and GPU checks |
| [01 — Neural network regression](01_neural_network_regression_with_tensorflow_video.ipynb) | Predicting numerical values, model experiments, MAE/MSE, preprocessing, and saving/loading models |
| [02 — Neural network classification](02_neural_network_classification_with_tensorflow.ipynb) | Classification with neural networks, including the Fashion MNIST work shown below |
| [03 — Introduction to computer vision](03_introduction_to_computer_vision_with_tensorflow_video.ipynb) | Image-based modelling with TensorFlow |
| [04 — Transfer learning: feature extraction](04_transfer_learning_in_tensorflow_part_1_feature_extraction_video.ipynb) | Using pretrained ResNet and EfficientNet features for food-image classification |
| [05 — Transfer learning: fine-tuning](05_transfer_learning_in_tensorflow_part_2_fine_tuning_video.ipynb) | Adapting pretrained image models through fine-tuning |
| [06 — Transfer learning: scaling up](06_transfer_learning_in_tensorflow_part_3_scaling_up_video.ipynb) | Extending the transfer-learning experiments to a larger problem |
| [08 — Introduction to NLP](08_introduction_to_nlp_in_tensorflow_video.ipynb) | Text modelling with TensorFlow |
| [09 — SkimLit](09_SkimLit_nlp_milestone_project_2_video.ipynb) | Classifying sentences in research abstracts using token, character, and positional information |
| [10 — Time-series forecasting](10_time_series_forecasting_with_tensorflow_video.ipynb) | Forecasting experiments, including Bitcoin price predictions |
| [11 — Skills checklist](11_tensorflow_exam_skills_checklist.ipynb) | Review notebook for TensorFlow modelling skills |

## Main projects and experiments

### Regression and classification

I started with small regression examples to understand the create → compile → fit → evaluate workflow. I compared predictions against ground truth, experimented with model complexity, and used MAE and MSE to assess error. The regression notebook also works with an insurance dataset and explores feature scaling and categorical preprocessing.

My classification work includes Fashion MNIST and experiments with the learning rate. Plotting the data, training curves, and predictions helped me connect changes in the model to its behaviour.

### Food-image classification and transfer learning

I explored using existing image representations instead of training every layer from scratch. The feature-extraction notebook compares pretrained ResNet and EfficientNet models using a ten-class food dataset subset. Later notebooks focus on fine-tuning and scaling up the experiments.

This work includes preparing image batches, attaching a classification head, tracking training with callbacks, and inspecting predictions. The gallery includes an example of food-image predictions from this part of the course.

### SkimLit: research abstract sentence classification

SkimLit was my NLP milestone project. The goal is to assign a role to each sentence in a medical research abstract so the abstract is easier to skim. It uses data from the [PubMed RCT dataset](https://github.com/Franck-Dernoncourt/pubmed-rct).

I worked through a TF-IDF/Multinomial Naive Bayes baseline and neural models using token embeddings, pretrained sentence embeddings, character representations, and combinations of those inputs. The later tribrid approach also incorporates sentence-position information. I compared models using accuracy, precision, recall, and F1, and used the Keras functional API to combine multiple inputs.

The notebook follows the course's treatment of the [PubMed 200k RCT paper](https://arxiv.org/abs/1710.06071) and its referenced architecture. This is a sentence-classification learning project; I haven't evaluated it as a clinical tool.

### Time-series forecasting

I explored time-series modelling and plotted forecasts against historical data, including Bitcoin prices. These experiments helped me practise temporal prediction and visual evaluation. The plots below are examples from my coursework, not evidence of a reliable trading model or current market predictions.

## Running the notebooks

### Google Colab

I used a notebook-based workflow, and several notebooks include Colab-specific cells and shell commands.

1. Open [Google Colab](https://colab.research.google.com/).
2. Choose **Open notebook → GitHub**, search for `fyemane/TensorFlow-ZTM`, and select a notebook. This also avoids the older embedded Colab badges that refer to the repository's previous `TensorFlow-ZTM-` name.
3. Choose a GPU runtime for the larger image/NLP experiments if one is available.
4. Review the setup and dataset-download cells, then run the notebook in order. Some cells depend on variables, files, or models created earlier.
5. Save any trained models or experiment results you want to keep before ending the session.

### Local Jupyter environment

Use an isolated Python environment with Jupyter and the dependencies required by the selected notebook. The notebooks use TensorFlow/Keras, NumPy, pandas, Matplotlib, and scikit-learn; some also use TensorFlow Hub, TensorFlow Datasets, or TensorFlow Probability. Model diagrams may need additional plotting tools.

Colab-only operations such as `google.colab` imports and notebook shell commands need adapting for a local environment. Dataset/helper-script download cells require internet access and should be reviewed before execution.

## Reproducibility and compatibility

These are my historical course notebooks, not a packaged application with a pinned environment. I haven't rerun the full collection against the latest TensorFlow, Keras, or Colab versions.

- Some imports use older API paths, including `tensorflow.keras.layers.experimental.preprocessing`. TensorFlow Hub layers, saving/loading code, and preprocessing calls may need version-specific changes.
- Several notebooks download datasets, pretrained models, or a course helper script at runtime. Those files aren't all stored in this repository, and external resources can change.
- Saved plots and outputs record earlier runs. A new run can differ with the environment, random initialization, dataset split, and hardware.
- I keep evaluation results within their notebook context rather than claiming one accuracy score for the entire repository.

## Gallery

<img width="414" alt="image" src="https://github.com/fyemane/TensorFlow-ZTM-/assets/93152842/35333e19-00e1-46ce-ae81-85d1c4762d68">

*Training data test samples with the Fashion MNIST dataset*

<img width="435" alt="image" src="https://github.com/fyemane/TensorFlow-ZTM-/assets/93152842/682b9e27-5bb0-4390-b0d6-54c6b816bd0d">

*Finding the ideal learning rate of a Keras sequential model for neural network classification*

<img width="1008" alt="image" src="https://github.com/fyemane/TensorFlow-ZTM-/assets/93152842/6ce84048-96bc-4ae5-9d80-91071bf5d592">

*Using a pretrained EfficientNet model with feature extraction and fine-tuning to predict test images of tasty food*

![image](https://github.com/fyemane/TensorFlow-ZTM-/assets/93152842/d8a96688-e395-4135-91bc-ac4edaf8bb30)

*Visually inspecting the neural network architecture of my tribrid embedding model for natural language processing*

![image](https://github.com/fyemane/TensorFlow-ZTM-/assets/93152842/798f02fe-5db9-490a-aa90-aa9f013c37de)

*Graphing a rough prediction of the future price of bitcoin using time series forecasting*

## Credits

I completed these notebooks while following the Zero to Mastery TensorFlow course. The course material and helper functions are associated with [Daniel Bourke's TensorFlow Deep Learning course repository](https://github.com/mrdbourke/tensorflow-deep-learning). Dataset and model references are retained in the notebooks. This repository records my learning and implementations of those exercises; I don't claim the course framework, datasets, or pretrained models as my own.
