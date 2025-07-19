🧠 Next Word Predictor using LSTM
This is a simple deep learning-based Next Word Prediction model built using TensorFlow and Keras. The model is trained on the classic novel The Blue Castle and can predict the next word in a sequence of three words.

📁 Project Structure
bash
Copy code
├── blue_castle.txt           # Training text file (novel)
├── next_word.h5              # Trained LSTM model
├── token.pkl                 # Saved tokenizer
├── plot.png                  # Model architecture visualization
├── main.py                   # Main Python file with full pipeline
└── README.md                 # Project documentation
🧪 Features
LSTM-based language model

Predicts the next word based on last 3 words

Trained on a real book dataset

Model visualization using keras.utils.plot_model

Tokenizer and model checkpointing

🛠️ Installation
Clone the repository (or download the files):

bash
Copy code
git clone https://github.com/yourusername/next-word-predictor.git
cd next-word-predictor
Install dependencies:

bash
Copy code
pip install tensorflow numpy pickle-mixin
You may also need to install pydot and graphviz if using the model plotting:

bash
Copy code
pip install pydot
▶️ How to Run
1. Train the model
Run the script to:

Clean the data

Tokenize the text

Train the LSTM model

Save the tokenizer and best model

bash
Copy code
python main.py
2. Predict next word
Once training is complete, you can interactively predict the next word by running the prediction section. Input the last three words of a sentence:

text
Copy code
Enter your line: she went to
Predicted next word: the
Enter 0 to stop the program.

🧠 Model Architecture
Embedding Layer: Converts word indices into dense vectors of fixed size.

LSTM Layers: Two stacked LSTM layers with 1000 units each.

Dense Layers: Final softmax layer outputs probability distribution over vocabulary.

Model summary is also saved as plot.png.

📊 Dataset
The training text comes from the novel:

The Blue Castle by Lucy Maud Montgomery
(Available in public domain on Project Gutenberg)

📌 Notes
Model trains on sequences of 3 words to predict the 4th.

Vocabulary size is automatically inferred from the tokenizer.

The model saves the best checkpoint using ModelCheckpoint.

🔮 Future Improvements
Use larger datasets like Wikipedia or news articles

Train with more context (5–10 words)

Add attention mechanism or transformer layers

Create a Streamlit or Tkinter GUI

🧑‍💻 Author
Vatsal Varshney

