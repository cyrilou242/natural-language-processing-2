# Natural Language Processing 2
My seconde iteration of works for "Natural Language Processing" Coursera course.

## Week1
Predict tag of Stackoverflow with linear model. (multi-tag)
Used GridSearch CV for optimisation on tfidf model.

Accuracy:  0.3631 (low because multi-tag)  
F1-score micro: :  0.6752548016404758  
F1-score macro: :  0.5062362622222868  
F1-score weighted: :  0.6540253209151559  
Precision micro: :  0.4810782509911088  
Precision macro: :  0.3396351761816072  
Precision weighted: :  0.5102553014775187  

## Week2
Named entity recognition with LSTMs.  

TODO

## Week3
Find duplicate questions by their embedding in word2vec.
TODO

## Week4
Seq2Seq model, encoder-decoder to learn to addition and substraction.
Model could be used for other tasks.
TODO

## Week5
TODO


# Natural Language Processing course resources
https://www.coursera.org/learn/language-processing

## Running on Google Colab
Google has released its own flavour of Jupyter called Colab, which has free GPUs!

Here's how you can use it:
1. Open https://colab.research.google.com, click **Sign in** in the upper right corner, use your Google credentials to sign in.
2. Click **GITHUB** tab, paste https://github.com/hse-aml/natural-language-processing and press Enter
3. Choose the notebook you want to open, e.g. week1/week1-MultilabelClassification.ipynb
4. Click **File -> Save a copy in Drive...** to save your progress in Google Drive
5. _If you need a GPU_, click **Runtime -> Change runtime type** and select **GPU** in Hardware accelerator box
6. **Execute** the following code in the first cell that downloads dependencies (change for your week number):
```python
! wget https://raw.githubusercontent.com/hse-aml/natural-language-processing/master/setup_google_colab.py -O setup_google_colab.py
import setup_google_colab
# please, uncomment the week you're working on
# setup_google_colab.setup_week1()  
# setup_google_colab.setup_week2()
# setup_google_colab.setup_week3()
# setup_google_colab.setup_week4()
# setup_google_colab.setup_project()
# setup_google_colab.setup_honor()
```
7. If you run many notebooks on Colab, they can continue to eat up memory,
you can kill them with `! pkill -9 python3` and check with `! nvidia-smi` that GPU memory is freed.

**Known issues:**
* No support for `ipywidgets`, so we cannot use fancy `tqdm` progress bars.
For now, we use a simplified version of a progress bar suitable for Colab.
* Blinking animation with `IPython.display.clear_output()`.
It's usable, but still looking for a workaround.

## Running elsewhere

[AWS](AWS-tutorial.md)

[Docker](Docker-tutorial.md)
