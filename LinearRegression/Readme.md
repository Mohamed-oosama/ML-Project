# 📊 Linear Regression Guide

هذا الملف يحتوي على شرح شامل لمفهوم **Linear Regression** في تعلم الآلة، مع توضيح أهم المفاهيم المرتبطة به.

---

## 1️⃣ ما هو Linear Regression

**Linear Regression** هو نموذج إحصائي يهدف لإيجاد علاقة خطية بين المتغيرات.  
الفكرة الأساسية: إيجاد أفضل خط مستقيم يمر بين النقاط بحيث يقلل الفرق بين:

- القيم الحقيقية
- القيم المتوقعة من النموذج

المعادلة الأساسية للخط:

<img width="688" height="49" alt="image" src="https://github.com/user-attachments/assets/66a5ef0e-bad0-4835-81c8-4c2b483f7519" />


| الرمز | المعنى |
|-------|--------|
| y     | القيمة المتوقعة |
| x     | المتغير (Feature) |
| m     | الميل (Slope) |
| b     | نقطة التقاطع مع محور y (Intercept) |

---

## 2️⃣ فكرة عمل النموذج

نحاول إيجاد خط يقلل الفرق بين القيمة الحقيقية \(y\) والقيمة المتوقعة \(\hat{y}\).

<img width="674" height="59" alt="image" src="https://github.com/user-attachments/assets/5580c504-1d87-4e97-a973-98bab67921ab" />


---

## 3️⃣ حساب الميل (Slope) ونقطة التقاطع

**الميل:**

<img width="445" height="186" alt="image" src="https://github.com/user-attachments/assets/2aaff2e3-d3fd-4fab-a1ca-052b9db78c6e" />


حيث:

| الرمز | المعنى |
|-------|--------|
| \(x_i\) | قيمة المتغير |
| \(y_i\) | القيمة الحقيقية |
| \(\bar{x}\) | متوسط x |
| \(\bar{y}\) | متوسط y |

---

## 4️⃣ Multiple Linear Regression

عندما يكون لدينا أكثر من Feature:


<img width="337" height="44" alt="image" src="https://github.com/user-attachments/assets/1bda9b1f-b556-4ae4-9ce5-2d01d854a7d7" />


**مثال:** التنبؤ بسعر منزل باستخدام:

- المساحة
- عدد الغرف
- الموقع

---

## 5️⃣ قياس جودة النموذج

<img width="475" height="363" alt="image" src="https://github.com/user-attachments/assets/5e50abb2-8b53-4efa-b736-f68afcd601e8" />


## 6️⃣ مشاكل شائعة

- **Outliers**: Linear Regression حساس للقيم الشاذة  
- **Overfitting**: عند التعقيد الكبير للنموذج  
- **Multicollinearity**: وجود تداخل بين Features  
- **Non-linear relationships**: عند عدم خطية العلاقة

---
<img width="555" height="613" alt="image" src="https://github.com/user-attachments/assets/c78e0f5b-e00f-4990-9a20-dde96c31e5e4" />

## 🔟 مقارنة سريعة للنماذج

| النموذج | الاستخدام |
|---------|-----------|
| Linear Regression | علاقة خطية بسيطة |
| Multiple Linear | أكثر من Feature |
| Ridge | تقليل معاملات لتجنب Overfitting |
| Lasso | اختيار Features مهمه |
| Polynomial | علاقة غير خطية |

---

## 1️⃣1️⃣ أهم المشاكل في Linear Regression

- Overfitting  
- Outliers  
- Multicollinearity  
- Non-linear relationships

---
from sklearn.linear_model import LinearRegression
import numpy as np
import matplotlib.pyplot as plt

# بيانات بسيطة
X = np.array([[1], [2], [3], [4], [5]]) \
y = np.array([2, 4, 6, 8, 10]) 

# تدريب النموذج
model = LinearRegression() \
model.fit(X, y) 

print("Slope (m):", model.coef_) \
print("Intercept (b):", model.intercept_)

# توقعات
y_pred = model.predict(X)

# رسم النتائج
plt.scatter(X, y, color='blue', label='Actual') \
plt.plot(X, y_pred, color='red', label='Predicted') \
plt.xlabel('X') \
plt.ylabel('y') \
plt.title('Linear Regression Example') \
plt.legend() \
plt.show() 

## 📚 المصادر

- [Scikit-Learn Linear Regression](https://scikit-learn.org/stable/modules/linear_model.html)  
- [Machine Learning Mastery](https://machinelearningmastery.com/linear-regression-for-machine-learning/)  
- [Towards Data Science](https://towardsdatascience.com/linear-regression-detailed-view-5a6c1c3a8b59)
