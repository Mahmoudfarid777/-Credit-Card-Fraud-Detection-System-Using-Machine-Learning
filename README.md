# 💳 Credit Card Fraud Detection System

## Machine Learning كشف عمليات الاحتيال في بطاقات الائتمان باستخدام 


---

##  نبذة عن المشروع

  يهدف هذا المشروع إلى بناء نظام ذكي لاكتشاف عمليات الاحتيال في بطاقات الائتمان باستخدام تقنيات Machine Learning، من خلال تحليل بيانات المعاملات البنكية والتعرف على الأنماط المرتبطة بالعمليات الاحتيالية وتمييزها عن المعاملات السليمة.

---

##  المشكلة

تُعد عمليات الاحتيال المالي من التحديات المهمة في القطاع المصرفي، خصوصًا بسبب عدم توازن البيانات:

- إجمالي المعاملات: **284,807**
- عدد العمليات الاحتيالية: **492**
- نسبة الاحتيال: **0.17%**

لذلك تُصنف المشكلة على أنها **Imbalanced Binary Classification**، مما يتطلب تقنيات خاصة لتحسين أداء النماذج.

---

##  مجموعة البيانات (Dataset)

- المصدر: Kaggle Credit Card Fraud Detection Dataset
- عدد السجلات: 284,807 معاملة
- عدد الخصائص: 31 عمودًا
- المتغير المستهدف: Class
  - 0 → معاملة سليمة
  - 1 → معاملة احتيالية

---

##  مراحل العمل

### 1 استكشاف البيانات
- فحص البيانات والتأكد من جودتها.
- تحليل توزيع الفئات.
- التحقق من القيم المفقودة والمكررة.
- دراسة الإحصاءات الوصفية.

### 2 التحليل الاستكشافي للبيانات (EDA)
- تحليل توزيع المعاملات السليمة والاحتيالية.
- دراسة توزيع المبالغ المالية.
- تحليل العلاقات بين المتغيرات.
- إنشاء الرسوم البيانية التوضيحية.

### 3 معالجة البيانات
- تطبيق **StandardScaler** على المتغيرات المناسبة.
- تقسيم البيانات إلى تدريب واختبار بنسبة 80/20.
- استخدام **SMOTE** لمعالجة عدم توازن البيانات.

### 4 بناء النماذج
| النموذج | النوع |
|----------|----------|
| Logistic Regression | Linear Model |
| Random Forest | Ensemble Learning |
| XGBoost | Gradient Boosting |

### 5 تقييم الأداء
تم استخدام المقاييس التالية:

- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Precision-Recall Curve
- Confusion Matrix

### 6 التنبؤ بالمعاملات الجديدة
يمكن للنظام التنبؤ بما إذا كانت المعاملة:
-  سليمة
-  احتيالية

---

##  النتائج

| النموذج | ROC-AUC |
|----------|----------|
| Logistic Regression | ~0.97 |
| Random Forest | ~0.98 |
| XGBoost | **~0.98+** |

حقق نموذج **XGBoost** أفضل أداء بين النماذج المستخدمة.

---

##  هيكل المشروع

```text
credit-card-fraud-detection/
│
├── Credit_Card_Fraud_Detection.ipynb
├── creditcard.csv
├── README.md
└── requirements.txt
```

---

## التقنيات المستخدمة

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Matplotlib
- Seaborn





```bash
# تثبيت المكتبات
pip install xgboost imbalanced-learn scikit-learn pandas numpy matplotlib seaborn

# تشغيل المشروع
jupyter notebook Credit_Card_Fraud_Detection.ipynb
```




