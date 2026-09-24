# 🩺 SAIR Regression Project 🤖

## 🇬🇧 English

### 📌 Overview

**SAIR Regression Project** is an end-to-end **Machine Learning Regression** project built using the Diabetes dataset from `scikit-learn`.

The project follows a complete machine learning workflow:

**📊 Data → 🔎 EDA → ⚙️ Preprocessing → 🤖 Model Training → 📈 Evaluation → 🎯 Hyperparameter Tuning → 🏆 Final Model → 📋 MLflow → 🌐 Streamlit → 🐙 GitHub**

The model uses **10 input features** to predict a numerical **target value related to diabetes disease progression**.

> ⚠️ **Important:** This project is for educational and machine learning demonstration purposes. It is **not a medical diagnostic system** and should not be used for clinical decision-making.

---

### 📊 Dataset

The project uses the built-in **Diabetes Dataset** provided by `scikit-learn`.

#### 🔹 Features

```text
age
sex
bmi
bp
s1
s2
s3
s4
s5
s6
```

#### 🎯 Target

The target is a continuous numerical value related to **diabetes disease progression** in the dataset.

---

### 🔬 Machine Learning Workflow

#### 1️⃣ Exploratory Data Analysis (EDA)

The notebook includes:

* 📊 Target distribution
* 📉 BMI vs. Target visualization
* 🔗 Feature-target correlation
* 📋 Sorted correlation values
* 🌡️ Correlation heatmap
* 📦 Feature distribution and outlier inspection

#### 2️⃣ Data Splitting

The dataset was divided into:

* 🏋️ Training Set
* 🔍 Validation Set
* 🧪 Test Set

The test set was kept separate until final evaluation.

#### 3️⃣ ⚙️ Preprocessing

`StandardScaler` was used for models that benefit from feature scaling.

The scaler was:

* ✅ Fitted only on the training data
* 🔄 Applied to validation and test data

Tree-based models were trained using the original feature values.

#### 4️⃣ 🤖 Models

Several regression algorithms were trained and compared:

* 📏 Linear Regression
* 🛡️ Ridge Regression
* 🌳 Random Forest Regressor
* 🚀 Gradient Boosting Regressor

#### 5️⃣ 📈 Model Evaluation

The models were evaluated using:

* **R²**
* **MAE — Mean Absolute Error**
* **RMSE — Root Mean Squared Error**

🔁 Cross-validation was also used to evaluate model performance.

#### 6️⃣ 🎯 Hyperparameter Tuning

`RandomizedSearchCV` was used to tune:

* 🌳 Random Forest
* 🚀 Gradient Boosting

The tuned models were compared using cross-validated R².

#### 7️⃣ 🏆 Final Model

The final candidate model was selected based on cross-validation performance and evaluated on the held-out test set.

Additional analysis included:

* 🎯 Actual vs. Predicted
* 📉 Residual Analysis
* ⭐ Feature Importance

The final evaluation metrics are stored in:

```text
model_card.json
```

---

### 📈 Results

The final model was evaluated on an unseen test set using:

**R² + MAE + RMSE**

The model was selected after comparing the tuned Random Forest and Gradient Boosting models using cross-validation.

📄 Detailed model information and final metrics can be found in:

```text
model_card.json
```

---

### 🌐 Streamlit Application

The project includes an interactive **Streamlit** application.

Users can enter the 10 dataset features and generate a predicted target value using the saved model.

#### ▶️ Run the Application

From the project folder:

```bash
streamlit run app.py
```

Then open the local Streamlit URL shown in the terminal, usually:

```text
http://localhost:8501
```

> ⚠️ The application uses the feature representation of the `scikit-learn` Diabetes dataset. The inputs should therefore be interpreted according to the dataset representation, not as direct real-world clinical measurements.

---

### 📋 MLflow Tracking

**MLflow** was used to track the experiment and record:

* 🤖 Model name
* 📈 Test R²
* 📉 Test MAE
* 📊 Test RMSE

The local MLflow database is stored in:

```text
mlflow.db
```

---

### 📁 Project Structure

```text
SAIR_Regression_Project/
│
├── 📱 app.py
├── 🤖 best_model.pkl
├── ⚙️ scaler.pkl
├── 📋 model_card.json
├── 📊 mlflow.db
├── 📓 regression-project.ipynb
├── 📦 requirements.txt
└── 📖 README.md
```

---

### 📂 File Description

| File                          | Description                                                                                 |
| ----------------------------- | ------------------------------------------------------------------------------------------- |
| 📓 `regression-project.ipynb` | Complete notebook containing EDA, preprocessing, training, evaluation, tuning, and analysis |
| 📱 `app.py`                   | Streamlit application for interactive predictions                                           |
| 🤖 `best_model.pkl`           | Saved final machine learning model                                                          |
| ⚙️ `scaler.pkl`               | Saved `StandardScaler` preprocessing object                                                 |
| 📋 `model_card.json`          | Model information and final evaluation metrics                                              |
| 📊 `mlflow.db`                | Local MLflow tracking database                                                              |
| 📦 `requirements.txt`         | Python dependencies required to run the project                                             |
| 📖 `README.md`                | Project documentation                                                                       |

---

### 🛠️ Installation & Usage

#### 1️⃣ Clone the repository

```bash
git clone https://github.com/alaa12-oh/SAIR_Regression_Project.git
```

#### 2️⃣ Enter the project directory

```bash
cd SAIR_Regression_Project
```

#### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

#### 4️⃣ Run the Streamlit application

```bash
streamlit run app.py
```

---

### 💻 Technologies Used

🐍 **Python**
🐼 **Pandas**
🔢 **NumPy**
📊 **Matplotlib**
🌡️ **Seaborn**
🤖 **Scikit-learn**
💾 **Joblib**
📋 **MLflow**
🌐 **Streamlit**
🐙 **Git & GitHub**

---

### 🎯 Project Goal

The goal of this project is to demonstrate a complete **Machine Learning Regression workflow**, from:

**📊 Data Exploration → ⚙️ Preprocessing → 🤖 Model Development → 📈 Evaluation → 🎯 Tuning → 💾 Model Saving → 📋 Experiment Tracking → 🌐 Deployment**

---

# 🇸🇩 العربية

## 🩺 نبذة عن المشروع

**SAIR Regression Project** هو مشروع متكامل في **Machine Learning Regression** باستخدام مجموعة بيانات **Diabetes Dataset** الموجودة داخل مكتبة `scikit-learn`.

يمر المشروع بمراحل دورة العمل الكاملة:

**📊 البيانات → 🔎 التحليل الاستكشافي → ⚙️ المعالجة → 🤖 تدريب النماذج → 📈 التقييم → 🎯 تحسين النماذج → 🏆 النموذج النهائي → 📋 MLflow → 🌐 Streamlit → 🐙 GitHub**

يستخدم النموذج **10 خصائص** كمدخلات للتنبؤ بقيمة رقمية مرتبطة بتطور مرض السكري داخل مجموعة البيانات.

> ⚠️ **مهم:** المشروع تعليمي بهدف تطبيق مفاهيم Machine Learning، وليس نظامًا للتشخيص الطبي ولا ينبغي استخدامه لاتخاذ قرارات سريرية.

---

## 📊 البيانات المستخدمة

تم استخدام **Diabetes Dataset** الجاهزة من `scikit-learn`.

### 🔹 الخصائص

```text
age
sex
bmi
bp
s1
s2
s3
s4
s5
s6
```

### 🎯 الـTarget

الـTarget عبارة عن قيمة رقمية مستمرة مرتبطة بقياس **تطور مرض السكري** داخل مجموعة البيانات.

---

## 🔬 مراحل المشروع

### 1️⃣ 🔎 التحليل الاستكشافي للبيانات — EDA

تم تنفيذ:

* 📊 تحليل توزيع الـTarget
* 📉 رسم العلاقة بين BMI والـTarget
* 🔗 حساب الارتباط بين الخصائص والـTarget
* 📋 ترتيب معاملات الارتباط
* 🌡️ Correlation Heatmap
* 📦 فحص التوزيعات والقيم الشاذة

### 2️⃣ ✂️ تقسيم البيانات

تم تقسيم البيانات إلى:

* 🏋️ Training Set
* 🔍 Validation Set
* 🧪 Test Set

وتم الاحتفاظ بالـTest Set إلى مرحلة التقييم النهائي.

### 3️⃣ ⚙️ المعالجة المسبقة

تم استخدام `StandardScaler` للنماذج التي تستفيد من Feature Scaling.

تم:

* ✅ تدريب الـScaler على بيانات التدريب فقط
* 🔄 تطبيقه على بيانات الـValidation والـTest

أما النماذج المعتمدة على الأشجار فتم تدريبها على البيانات الأصلية.

### 4️⃣ 🤖 النماذج المستخدمة

تم تدريب ومقارنة:

* 📏 Linear Regression
* 🛡️ Ridge Regression
* 🌳 Random Forest Regressor
* 🚀 Gradient Boosting Regressor

### 5️⃣ 📈 تقييم النماذج

تم استخدام:

* **R²**
* **MAE**
* **RMSE**

كما تم استخدام 🔁 **Cross-Validation** لتقييم أداء النماذج.

### 6️⃣ 🎯 تحسين النماذج

تم استخدام `RandomizedSearchCV` لتحسين:

* 🌳 Random Forest
* 🚀 Gradient Boosting

ثم تمت مقارنة النماذج المحسنة باستخدام Cross-Validation R².

### 7️⃣ 🏆 النموذج النهائي

تم اختيار النموذج المرشح النهائي بناءً على أداء الـCross-Validation، ثم تقييمه على Test Set منفصل.

كما تم تحليل:

* 🎯 Actual vs. Predicted
* 📉 Residuals
* ⭐ Feature Importance

والنتائج النهائية محفوظة في:

```text
model_card.json
```

---

## 📈 النتائج

تم تقييم النموذج النهائي على بيانات اختبار لم يتم استخدامها أثناء التدريب باستخدام:

**R² + MAE + RMSE**

وتم اختيار النموذج بعد مقارنة النماذج المحسنة باستخدام Cross-Validation.

📄 يمكن معرفة النتائج والمعلومات الخاصة بالنموذج من:

```text
model_card.json
```

---

## 🌐 تطبيق Streamlit

يحتوي المشروع على تطبيق تفاعلي باستخدام **Streamlit**.

يمكن للمستخدم إدخال الخصائص العشر والحصول على قيمة متوقعة للـTarget باستخدام النموذج المحفوظ.

### ▶️ تشغيل التطبيق

من داخل مجلد المشروع:

```bash
streamlit run app.py
```

ثم افتحي الرابط المحلي الذي يظهر في الـTerminal، وغالبًا يكون:

```text
http://localhost:8501
```

> ⚠️ التطبيق يستخدم تمثيل الخصائص كما هو موجود في Diabetes Dataset الخاصة بـ`scikit-learn`، لذلك لا ينبغي تفسير المدخلات على أنها قياسات سريرية مباشرة.

---

## 📋 MLflow

تم استخدام **MLflow** لتتبع تجربة النموذج وتسجيل:

* 🤖 اسم النموذج
* 📈 Test R²
* 📉 Test MAE
* 📊 Test RMSE

وقاعدة البيانات المحلية موجودة في:

```text
mlflow.db
```

---

## 📁 هيكل المشروع

```text
SAIR_Regression_Project/
│
├── 📱 app.py
├── 🤖 best_model.pkl
├── ⚙️ scaler.pkl
├── 📋 model_card.json
├── 📊 mlflow.db
├── 📓 regression-project.ipynb
├── 📦 requirements.txt
└── 📖 README.md
```

---

## 📂 وصف الملفات

| الملف                         | الوظيفة                                             |
| ----------------------------- | --------------------------------------------------- |
| 📓 `regression-project.ipynb` | المشروع كاملًا من EDA إلى التدريب والتقييم والتحسين |
| 📱 `app.py`                   | تطبيق Streamlit للتنبؤ التفاعلي                     |
| 🤖 `best_model.pkl`           | النموذج النهائي المحفوظ                             |
| ⚙️ `scaler.pkl`               | كائن StandardScaler المحفوظ                         |
| 📋 `model_card.json`          | معلومات النموذج والنتائج النهائية                   |
| 📊 `mlflow.db`                | قاعدة بيانات MLflow المحلية                         |
| 📦 `requirements.txt`         | المكتبات المطلوبة لتشغيل المشروع                    |
| 📖 `README.md`                | توثيق المشروع                                       |

---

## 🛠️ التثبيت والتشغيل

### 1️⃣ تحميل المشروع

```bash
git clone https://github.com/alaa12-oh/SAIR_Regression_Project.git
```

### 2️⃣ الدخول إلى مجلد المشروع

```bash
cd SAIR_Regression_Project
```

### 3️⃣ تثبيت المكتبات

```bash
pip install -r requirements.txt
```

### 4️⃣ تشغيل التطبيق

```bash
streamlit run app.py
```

---

## 💻 التقنيات المستخدمة

🐍 **Python**
🐼 **Pandas**
🔢 **NumPy**
📊 **Matplotlib**
🌡️ **Seaborn**
🤖 **Scikit-learn**
💾 **Joblib**
📋 **MLflow**
🌐 **Streamlit**
🐙 **Git & GitHub**

---

## 🎯 هدف المشروع

يهدف المشروع إلى تطبيق دورة عمل متكاملة في **Machine Learning Regression** بدايةً من:

**📊 استكشاف البيانات → ⚙️ المعالجة → 🤖 بناء النماذج → 📈 التقييم → 🎯 التحسين → 💾 حفظ النموذج → 📋 تتبع التجارب → 🌐 بناء تطبيق تفاعلي → 🐙 رفع المشروع على GitHub**

---

⭐ **Built as part of the SAIR Machine Learning learning journey.**

⭐ **تم بناء المشروع كتطبيق عملي على رحلة تعلم Machine Learning ضمن SAIR.**
