# Emotion-Based Music Recommendation System

## Abstract

This project introduces an Emotion-Based Music Recommendation System designed to enhance mental well-being by recommending music based on real-time emotional analysis. The system leverages Convolutional Neural Networks (CNNs) to detect emotions from live video feeds and suggests music tailored to the user's current emotional state. Unlike traditional music recommendation systems that rely on historical data, this system focuses on real-time emotional insights.

## Introduction

### Context and Motivation

**Mental Health Statistics**: Mental health issues have significant economic and personal impacts. In India, mental health conditions contribute to a high number of disability-adjusted life years and economic losses. The prevalence of stress and anxiety is increasing, highlighting the need for effective mental health solutions.

**Music as Therapy**: Music has therapeutic benefits, including stress relief, mood enhancement, and overall well-being improvement. However, traditional music recommendation systems do not consider the user's current emotional state, which can limit their effectiveness.

### Problem Statement

**Current Limitations**: Existing music recommendation systems base their suggestions on historical data such as preferred genres and artists, without accounting for real-time emotional states.

**Objective**: Develop a system that detects the user's current emotion through live video analysis and recommends music that aligns with that emotion.

## Related Work

### Facial Expression Analysis

- **Facial Action Coding System (FACS)**: Provides a framework for analyzing facial movements associated with different emotions.
- **Previous CNN Approaches**: Research by Yu and Zhang (2015) achieved state-of-the-art results in facial emotion recognition using CNNs.
- **Automatic Face Analysis**: Techniques for analyzing both permanent and transient facial features to recognize emotions.

### Music Emotion Classification

- **Robert E. Thayer**: Classified music emotions based on energy and stress, categorizing them into types such as exuberance, anxious/frantic, and calm.

## System Design and Analysis

### Existing Music Recommendation Techniques

**Current Methods**: Platforms like Spotify and Apple Music recommend music based on user history, preferences, and surveys. These methods do not consider the user's current emotional state.

### Proposed System Design

#### Emotion Detection

- **Model Training**: A CNN is trained on a dataset of facial images to recognize emotions like angry, disgusted, fearful, happy, sad, surprised, and neutral.
- **Live Video Feed**: An application captures live video and processes it with the trained CNN to detect the user's emotion in real time.

#### Music Recommendation

- **Emotion-Based Suggestions**: Music is recommended based on the detected emotion from a predefined list or online music service.
- **User Preferences**: Users can specify language and artist preferences to refine recommendations.

### CNN Architecture

- **Layer 1**: 32 filters, size 3x3, ReLU activation.
- **Layer 2**: 64 filters, size 3x3, ReLU activation.
- **Max Pooling**: 2x2.
- **Layer 3**: 128 filters, size 3x3, ReLU activation.
- **Layer 4**: 128 filters, size 3x3, ReLU activation.
- **Dropout Layers**: To prevent overfitting.
- **Dense Layers**: Final classification with SoftMax activation.

## Implementation

### Model Training

- **Data**: A dataset of 28,000 images classified into 7 emotions was used. Images were preprocessed into batches and converted to grayscale.
- **Training Process**: Various batch sizes and epochs were tested to optimize accuracy. The CNN model was trained with adjustments to learning rates and dropout rates.
- **Results**: Achieved up to 86.06% accuracy with optimal settings.

### Live Feed Application

- **Technology**: Implemented in Python using OpenCV (CV2) for video capture and emotion detection.
- **Process**: Continuously captures video, processes frames through the CNN, and determines the dominant emotion.

### Music Recommendation

- **Integration**: Developed an algorithm to recommend music based on the detected emotion, with options for user preferences like language and artists.

## Results

- **Accuracy**: Model performance varied with different configurations:
  - Batch Size 64, Epochs 50: Highest accuracy of 86.06%.
  - Batch Size and Epochs adjustments affected accuracy, demonstrating the impact of network depth and training parameters.
- **Effect of Layers**: The removal of certain CNN layers impacted accuracy, highlighting the importance of the network's architecture.

## Conclusion and Further Scope

**Summary**: The system successfully detects emotions and provides relevant music recommendations, potentially enhancing mental well-being.

**Future Work**: Future developments could include adapting the system for movie recommendations or further improving accuracy with additional data and model adjustments.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For inquiries or contributions, please contact:

- **Praveen K**: Praveen@nitk.edu.in
- **Aditya Narayansetti**: aditya.211ai005@nitk.edu.in

---

**Acknowledgments**: This project demonstrates a novel application of CNNs for real-time emotion detection and music recommendation, addressing a gap in current systems by focusing on the user's immediate emotional state.
