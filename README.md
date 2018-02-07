## Beginning Machine Learning with Keras & Core ML

[出處](https://www.raywenderlich.com/181760/beginning-machine-learning-keras-core-ml)，這篇文章內容完全剛好是我之前正想要學習的部分，因此根據文章內容實作一遍後，整理出自己的心得筆記。

### [Why Use Keras?](#1)
### Getting Started
> [Setting Up Docker](#2)
> 
> [ML in a Nutshell](#3)
> 
> > Weights & Threshold
> > 
> > Training an ML Model
> > 
> > Stochastic Gradient Descent
> > 
> > Optimizers

### Keras Code Time!
> [Import Utilities & Dependencies]()
> 
> [Load & Pre-Process Data]()
> >
> > [Training & Validation Data Sets]()
> > 
> > [Set Input & Output Dimensions]()
> > 
> > [Reshape x Data & Set Input Shape]()
> > 
> > [Inspect Reshaped x Data]()
> > 
> > [Convert Data Type & Normalize Values]()
> > 
> > [Inspect Normalized x Data]()
> > 
> > [Reformat y Data]()
> > 
> > [Inspect Reformatted y Data]()

### [Define Model Architecture]()
> [Malireddi’s Architecture]()
> 
> [Chollet’s Architecture]()
> 
> [Model Summaries]()

### [Train the Model]()
> [Define Callbacks List]()
> 
> [Compile & Fit Model]()

### [Convolutional Neural Network: Explanations]()
> [Sample Model]()
> 
> [Sequential]()
> 
> [Conv2D]()
> 
> [MaxPooling2D]()
>
> [Dropout]()
> 
> [Flatten]()
> 
> [Dense]()
> 
> [Compile]()
> 
> [Fit]()

### [Results]()

### [Convert to Core ML Model]()
> [Inspect Core ML model]()
> 
> [Add Metadata for Xcode]()
> 
> [Save the Core ML Model]()

### [Use Model in iOS App]()
> [Step 1. Drag the model into the app:]()
> 
> [Step 2. Import the CoreML and Vision frameworks:]()
> 
> [Step 3. Create VNCoreMLModel and VNCoreMLRequest objects:]()
> 
> [Step 4. Create and run a VNImageRequestHandler:]()

---

<h3 id="1">Why Use Keras?</h3>

> 兩個原因:
> > 1. Keras提供簡易好用的API(easy-to-use)，就是將TensorFlow在封裝一層，當然缺點就是使用上的靈活性也下降了。
> > 2. 就是apple所提供coremltools有支援Keras converter，尚未有TensorFlow converter。

<h3 id="2">Setting Up Docker?</h3>

> 這篇文章，介紹如何利用docker進行相關環境的安裝(ML resources)，但我這裡是用更無腦的anaconda。
> > 1. [安裝anaconda](https://www.anaconda.com/download/#macos)
> > 2. [安裝keras](https://anaconda.org/conda-forge/keras)
> > 3. [安裝CoreML tools](https://pypi.python.org/pypi/coremltools)

<h3 id="3">ML in a Nutshell?</h3>

> ML的超級基礎入門
>
>  1. ML的定義:  
> > “the field of study that gives computers the ability to learn without being explicitly programmed”。
> 
> 2. ML的分類:
> > supervised learning, Unsupervised learning
> 
> 3. Weights & Threshold
> > 舉了選餐廳的例子，要如何選擇一家好的餐廳可能有很多影響因子(價格，距離，服務..)，替每個因子都給予量化(1~5顆星)，並替每個因子都給予一個權重值(Weight)，將所有的因子跟權重值的乘積相加後，就是我們量化選擇餐廳的分數，當這個分數高過一個門檻(Threshold)，我們就可以將此餐廳列入選擇之一。
> 
> 4. Training an ML Model
> > 如何替每個因子設定適當的權重，這就是機器的學習目標。
> > 
> > * 隨機量化權重值
> > * 給予trainig data進行訓練，利用與實際結果的誤差來更新權重。
> > * overfitting問題，weight沒有一般化，導致測試結果比訓練結果差很多。
> 
> 5. Stochastic Gradient Descent
> > 找到最佳權重值的方法。
> 
> 6. 

