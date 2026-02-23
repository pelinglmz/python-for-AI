VERİ TİPLERİ

Programlama şu soruyla başlar:

> “Bilgiyi bilgisayara nasıl saklarız?”

Python’da bilgi saklamanın farklı yolları var. Bunlara **veri tipi (data type)** denir.

---

# 🟢 1) SAYILAR

Python’da 3 temel sayı türü var:

## 🔹 Integer (Tam sayı)

```python
a = 10
```

Ne oldu burada?

* `a` bir değişken.
* 10 değerini tutuyor.
* Türü: integer (int)

Kontrol edelim:

```python
print(type(a))
```

Çıktı:

```
<class 'int'>
```

---

## 🔹 Float (Ondalıklı sayı)

```python
b = 3.14
print(type(b))
```

Çıktı:

```
<class 'float'>
```

Float = decimal sayı.

---

## 🔹 Complex (Karmaşık sayı)

```python
c = 2 + 3j
print(type(c))
```

AI’da genelde kullanılmaz ama matematikte vardır.

---

# 🟢 Matematik İşlemleri

Python hesap makinesi gibi çalışır.

```python
a = 10
b = 3
```

### ➕ Toplama

```python
print(a + b)
```

Çıktı:

```
13
```

### ✖ Çarpma

```python
print(a * b)
```

Çıktı:

```
30
```

### ➗ Bölme

```python
print(a / b)
```

Çıktı:

```
3.3333...
```

Dikkat: Sonuç float olur.

---

### 🔹 // → Tam sayı bölme

```python
print(a // b)
```

Çıktı:

```
3
```

Yani virgülden sonrasını atar.

---

### 🔹 ** → Üs alma

```python
print(a ** 2)
```

Çıktı:

```
100
```

---

### 🔥 Gerçek Hayat Örneği

AI’da kayıp fonksiyonu hesaplıyorsun diyelim:

```python
error = (5 - 3) ** 2
print(error)
```

Bu ne yaptı?

(5 - 3)² hesapladı.

---

# 🟢 2) STRING (METİN)

String = yazı.

```python
text = "Artificial Intelligence"
```

---

## 🔹 Büyük harf

```python
print(text.upper())
```

Çıktı:

```
ARTIFICIAL INTELLIGENCE
```

---

## 🔹 Küçük harf

```python
print(text.lower())
```

---

## 🔹 Uzunluk

```python
print(len(text))
```

Kaç karakter var onu verir.

---

## 🔹 Kelimelere ayırma

```python
print(text.split())
```

Çıktı:

```
['Artificial', 'Intelligence']
```

AI’da metin işleme (NLP) için bu çok önemli.

---

## Örnek

```python
sentence = "I love AI"
words = sentence.split()

print(words[0])
```

Çıktı:

```
I
```

Yani string’i listeye çevirdi.

---

# 🟢 3) LIST (DEĞİŞTİRİLEBİLİR)

Liste = birden fazla şeyi saklama yöntemi.

```python
numbers = [1, 2, 3]
```

---

## 🔹 Eleman ekleme

```python
numbers.append(4)
print(numbers)
```

Çıktı:

```
[1, 2, 3, 4]
```

---

## 🔹 İlk eleman

```python
print(numbers[0])
```

Çıktı:

```
1
```

Python 0’dan başlar.

---

## 🔹 Son eleman

```python
print(numbers[-1])
```

Çıktı:

```
4
```

---

## 🔹 Slicing

```python
print(numbers[1:3])
```

Çıktı:

```
[2, 3]
```

Mantık:

```
[start : stop]
```

Stop dahil değil.

---

## AI Örneği

Bir veri seti düşün:

```python
scores = [85, 90, 78, 92, 88]
```

İlk 3 öğrenciyi al:

```python
print(scores[:3])
```

---

# 🟢 4) TUPLE (DEĞİŞTİRİLEMEZ)

Liste gibi ama değişmez.

```python
coordinates = (10, 20)
```

Bunu değiştiremezsin:

```python
coordinates[0] = 5
```

Hata verir.

---

### Ne zaman kullanılır?

Değişmemesi gereken verilerde.

Örneğin:

```python
rgb = (255, 0, 0)
```

---

# 🟢 5) DICTIONARY

Anahtar-değer sistemi.

```python
person = {
    "name": "Alice",
    "age": 25
}
```

---

## 🔹 Değer alma

```python
print(person["name"])
```

Çıktı:

```
Alice
```

---

## 🔹 Yeni veri ekleme

```python
person["city"] = "Istanbul"
print(person)
```

---

## AI Örneği

Bir öğrenci kaydı:

```python
student = {
    "math": 85,
    "physics": 90
}

average = (student["math"] + student["physics"]) / 2
print(average)
```

---

# KONTROL YAPILARI

Programın karar verme mekanizması.

---

# IF-ELSE

```python
score = 85

if score >= 90:
    print("A")
elif score >= 80:
    print("B")
else:
    print("F")
```

Mantık:

* Eğer doğruysa çalışır.
* Değilse diğerine geçer.

---

## AI Örneği

```python
prediction = 0.8

if prediction > 0.5:
    print("Class 1")
else:
    print("Class 0")
```

Bu classification mantığıdır.

---

# FOR LOOP

Tekrar yapma.

```python
for i in range(5):
    print(i)
```

Çıktı:

```
0
1
2
3
4
```

---

## Liste üzerinde dönme

```python
numbers = [10, 20, 30]

for num in numbers:
    print(num * 2)
```

---

# WHILE LOOP

Koşul doğru olduğu sürece çalışır.

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

Dikkat: Sonsuz döngü yapma.

---

# LIST COMPREHENSION (ÇOK ÖNEMLİ)

Normal yöntem:

```python
squares = []

for x in range(5):
    squares.append(x**2)
```

Kısa hali:

```python
squares = [x**2 for x in range(5)]
```

Çıktı:

```
[0, 1, 4, 9, 16]
```

---

## Koşullu

```python
even_squares = [x**2 for x in range(10) if x % 2 == 0]
```

Bu AI’da veri filtrelemede çok kullanılır.

---

# FONKSİYONLAR

Fonksiyon = tekrar kullanılabilir kod.

---

## 🔹 Basit Fonksiyon

```python
def greet(name):
    return "Hello " + name
```

Kullanım:

```python
print(greet("Ahmet"))
```

---

## 🔹 Default Parametre

```python
def power(base, exponent=2):
    return base ** exponent
```

```python
print(power(5))     # 25
print(power(5,3))   # 125
```

---

## 🔹 Lambda

```python
square = lambda x: x**2
print(square(5))
```

---

# 🔹 MAP

```python
numbers = [1,2,3]

squared = list(map(lambda x: x**2, numbers))
print(squared)
```

Tüm elemanlara uygular.

---

# 🔹 FILTER

```python
numbers = [1,2,3,4,5]

evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)
```

Sadece şartı sağlayanları alır.

---

OBJECT ORIENTED PROGRAMMING (OOP)

Gerçek AI projelerinde class yapısı kullanılır.

Model yazarken, veri loader yazarken, custom layer yazarken class gerekir.

Class Nedir?

Class = bir şablon (template).

class Student:
    pass

Bu sadece boş bir class.

init Nedir?

Constructor (başlatıcı fonksiyon).

Class oluşturulurken otomatik çalışır.

class Student:

    def __init__(self, name, score):
        self.name = name
        self.score = score

Burada:

self → objenin kendisini temsil eder

name → parametre

self.name → objeye ait özellik

Obje Oluşturma
s1 = Student("Ahmet", 85)

print(s1.name)
print(s1.score)
Method (Fonksiyon Eklemek)
class Student:

    def __init__(self, name, score):
        self.name = name
        self.score = score

    def is_passed(self):
        return self.score > 80

Kullanım:

s1 = Student("Ahmet", 85)
print(s1.is_passed())
AI Bağlantısı

Gerçek hayatta model şöyle yazılır:

class LinearModel:

    def __init__(self, weight):
        self.weight = weight

    def predict(self, x):
        return self.weight * x

Neural network’lerin temeli budur.

---

# NUMPY NEDİR?

NumPy = Numerical Python

Şu problemi çözer:

Python listeleri matematik için yavaştır.

Örnek:

```python
a = [1, 2, 3]
b = [4, 5, 6]

print(a + b)
```

Çıktı:

```
[1, 2, 3, 4, 5, 6]
```

Toplama yapmadı. Birleştirdi!

Ama NumPy:

```python
import numpy as np

a = np.array([1,2,3])
b = np.array([4,5,6])

print(a + b)
```

Çıktı:

```
[5 7 9]
```

Gerçek matematik yaptı.

İşte bu yüzden AI’da NumPy kullanılır.

---

# ARRAY OLUŞTURMA

NumPy’nin temel veri tipi: **array**

---

## 1D Array (Vektör)

```python
import numpy as np

arr = np.array([1,2,3])
print(arr)
```

Bu ne?

Bir vektör.

Matematikte:

```
[1 2 3]
```

---

## 2D Array (Matrix)

```python
matrix = np.array([[1,2],[3,4]])
print(matrix)
```

Bu ne?

```
1  2
3  4
```

AI’da:

* Görüntüler → matrix
* Veri setleri → matrix
* Neural network ağırlıkları → matrix

---

# ÖZEL MATRİSLER

---

## np.zeros

Sıfırlardan oluşan matrix.

```python
z = np.zeros((2,3))
print(z)
```

Çıktı:

```
[[0. 0. 0.]
 [0. 0. 0.]]
```

Ne işe yarar?

* Model başlatırken
* Boş veri oluştururken

---

## np.ones

```python
o = np.ones((2,2))
print(o)
```

---

## np.eye (Identity Matrix)

```python
i = np.eye(3)
print(i)
```

Çıktı:

```
[[1 0 0]
 [0 1 0]
 [0 0 1]]
```

Bu neden önemli?

Lineer cebirin temelidir.
Neural network’te kullanılır.

---

## np.random.rand

Rastgele sayılar üretir.

```python
r = np.random.rand(2,3)
print(r)
```

Ne işe yarar?

Model ağırlıkları random başlatılır.

RANDOM SEED

Random demek tamamen rastgele değildir.

Aynı sonucu tekrar üretmek için seed kullanılır.

import numpy as np

np.random.seed(42)

print(np.random.rand(3))

Her çalıştırmada aynı sonuç gelir.

AI’da Önemi

Deney tekrar edilebilir olmalı.

Makale yazarken seed belirtilir.

---

# ARRAY ÖZELLİKLERİ

Bir matrix hakkında bilgi almak için:

```python
matrix = np.array([[1,2,3],[4,5,6]])
```

---

## 🔹 .shape

```python
print(matrix.shape)
```

Çıktı:

```
(2,3)
```

Yani:
2 satır
3 sütun

AI’da çok önemli!

---

## 🔹 .size

Toplam eleman sayısı

```python
print(matrix.size)
```

Çıktı:

```
6
```

---

## 🔹 .ndim

Kaç boyutlu?

```python
print(matrix.ndim)
```

Çıktı:

```
2
```

---

## 🔹 .dtype

Veri tipi

```python
print(matrix.dtype)
```

Genelde:

```
int64
float64
```

---

# ARRAY İŞLEMLERİ

---

## Element Bazlı İşlem

```python
a = np.array([1,2,3])
b = np.array([4,5,6])

print(a + b)
```

Çıktı:

```
[5 7 9]
```

Mantık:
1+4
2+5
3+6

---

## Çarpma

```python
print(a * b)
```

Çıktı:

```
[4 10 18]
```

Element bazlıdır.

---

# Matrix Çarpımı (ÖNEMLİ)

```python
A = np.array([[1,2],[3,4]])
B = np.array([[5,6],[7,8]])

print(A @ B)
```

Çıktı:

```
[[19 22]
 [43 50]]
```

Bu neden önemli?

Neural network’te:

```
Output = Weights @ Input
```

Her şey matrix çarpımıdır.

---

# İSTATİSTİKSEL İŞLEMLER

```python
data = np.array([1,2,3,4,5])
```

---

## 🔹 Mean

```python
print(np.mean(data))
```

Ortalama.

---

## 🔹 Median

Ortadaki değer.

---

## 🔹 Std

Standart sapma.

AI’da veri dağılımını anlamak için kullanılır.

---

## 🔹 Min / Max

```python
print(np.min(data))
print(np.max(data))
```

---

## 🔹 Sum

Toplam.

---

# INDEXING

---

## 1D

```python
arr = np.array([10,20,30,40])

print(arr[2])
```

Çıktı:

```
30
```

---

## 2D

```python
matrix = np.array([[1,2,3],[4,5,6]])
```

---

Satır 1 sütun 2:

```python
print(matrix[1,2])
```

Çıktı:

```
6
```

---

## Satır alma

```python
print(matrix[0,:])
```

İlk satır.

---

## Sütun alma

```python
print(matrix[:,1])
```

İkinci sütun.

---

# BOOLEAN INDEXING (AI’da çok kritik)

```python
arr = np.array([1,2,3,4,5,6])
```

3’ten büyükleri al:

```python
print(arr[arr > 3])
```

Çıktı:

```
[4 5 6]
```

Bu ne yaptı?

Önce şunu oluşturdu:

```
[False False False True True True]
```

Sonra True olanları aldı.

AI’da:

* Filtreleme
* Outlier temizleme
* Veri seçme

hep bu yöntemle yapılır.

---

# BROADCASTING

NumPy’nin en güçlü özelliği.

Farklı boyuttaki array’ler birlikte çalışır.

---

## Tüm matrise 10 eklemek

```python
arr = np.array([[1,2],[3,4]])

print(arr + 10)
```

Çıktı:

```
[[11 12]
 [13 14]]
```

10’u her elemana yaydı.

---

## Satır vektörüyle çarpma

```python
arr = np.array([[1,2,3],
                [4,5,6]])

vector = np.array([1,2,3])

print(arr * vector)
```

Çıktı:

```
[[ 1  4  9]
 [ 4 10 18]]
```

Her satır vector ile çarpıldı.

---

## Sütun vektörü

```python
col = np.array([[10],[20]])

print(arr + col)
```

Çıktı:

```
[[11 12 13]
 [24 25 26]]
```

---

# AI BAĞLANTISI

Neural network’te:

```
z = W @ X + b
```

* W = matrix
* X = vector
* b = bias (broadcasting ile eklenir)

Broadcasting olmazsa neural network olmaz.

---

# PANDAS NEDİR?

Pandas = tablo şeklindeki verileri yönetmek için kullanılır.

Excel gibi düşün.

Ama kodla kontrol ediyorsun.

---

# SERIES

Series = tek boyutlu veri.

Bir sütun gibi düşün.

---

## Series Oluşturma

```python
import pandas as pd

s = pd.Series([10, 20, 30, 40])
print(s)
```

Çıktı:

```
0    10
1    20
2    30
3    40
dtype: int64
```

Sol taraf → index
Sağ taraf → değer

---

## Özel index ile

```python
s = pd.Series([85, 90, 78], index=["Ali", "Ayşe", "Mehmet"])
print(s)
```

Çıktı:

```
Ali       85
Ayşe      90
Mehmet    78
```

Veriye isim verdik.

---

## 🔹 Değer çekme

```python
print(s["Ali"])
```

---

### AI bağlantısı

Bir modelin çıktıları:

```python
probabilities = pd.Series([0.1, 0.7, 0.2], index=["Cat", "Dog", "Bird"])
```

En yüksek ihtimali bulabilirsin.

---

# DATAFRAME

DataFrame = tablo.

Excel tablosu gibi.

---

## Dictionary’den oluşturma

```python
data = {
    "Name": ["Ali", "Ayşe", "Mehmet"],
    "Age": [25, 30, 22],
    "Score": [85, 90, 78]
}

df = pd.DataFrame(data)
print(df)
```

Çıktı:

```
     Name  Age  Score
0     Ali   25     85
1    Ayşe   30     90
2  Mehmet   22     78
```

Sütunlu veri.

---

## NumPy array’den oluşturma

```python
import numpy as np

arr = np.array([[1,2],[3,4],[5,6]])

df = pd.DataFrame(arr, columns=["A","B"])
print(df)
```

---

# VERİ SEÇME

---

## Tek sütun seçme

```python
print(df["Name"])
```

Bir Series döner.

---

## Birden fazla sütun

```python
print(df[["Name","Age"]])
```

DataFrame döner.

---

## İlk 5 satır

```python
print(df.head())
```

İlk 5 satırı gösterir.

İlk 3 satır:

```python
print(df.head(3))
```

---

# KOŞULLU FİLTRELEME (ÇOK ÖNEMLİ)

```python
print(df[df["Age"] > 25])
```

Ne oldu burada?

1️⃣ df["Age"] > 25 → True/False listesi üretir
2️⃣ True olan satırları alır

Bu Boolean indexing’dir (NumPy mantığı burada da var).

---

## Birden fazla koşul

```python
print(df[(df["Age"] > 20) & (df["Score"] > 80)])
```

& = ve
| = veya

---

### AI bağlantısı

Örneğin:

* Yaşı 30’dan büyük
* Geliri yüksek

olan müşterileri filtrelemek.

Model eğitmeden önce veri seçimi yapılır.

---

# YENİ SÜTUN EKLEME

```python
df["Bonus"] = df["Score"] * 0.1
print(df)
```

Ne yaptı?

Score sütununu %10 ile çarptı ve yeni sütun yaptı.

---

## Daha gelişmiş örnek

```python
df["Passed"] = df["Score"] > 80
```

Yeni sütun True/False olur.

---

AI’da:
Feature engineering böyle yapılır.

Yeni özellikler oluşturulur.

---

# 🔵 GROUPBY (ÇOK ÖNEMLİ)

Verileri grupla ve analiz et.

---

## Örnek veri

```python
data = {
    "Name": ["Ali","Ayşe","Mehmet","Zeynep"],
    "Department": ["AI","ML","AI","ML"],
    "Salary": [7000,8000,7500,9000]
}

df = pd.DataFrame(data)
```

---

## Departmana göre ortalama maaş

```python
print(df.groupby("Department")["Salary"].mean())
```

Ne yaptı?

1️⃣ AI grubunu aldı
2️⃣ ML grubunu aldı
3️⃣ Her grubun ortalamasını hesapladı

Çıktı:

```
AI    7250
ML    8500
```

---

AI’da:

* Sınıflara göre ortalama
* Departmana göre analiz
* Ülkeye göre satış

hep groupby ile yapılır.

---

CSV DOSYASI OKUMA

Gerçek AI projelerinde veri genelde CSV dosyasındadır.

CSV Okuma
import pandas as pd

df = pd.read_csv("data.csv")
print(df.head())
CSV Kaydetme
df.to_csv("cleaned_data.csv", index=False)
Excel Okuma
df = pd.read_excel("data.xlsx")
AI Süreci

1️⃣ CSV yüklenir
2️⃣ Temizlik yapılır
3️⃣ Yeni feature oluşturulur
4️⃣ Model eğitilir

---

# DATA CLEANING

Gerçek veri asla temiz değildir.

Eksik veri vardır.

Yanlış veri vardır.

Model eğitmeden önce temizlenir.

---

# Eksik Veri (NaN)

NaN = Not a Number

```python
import numpy as np

df = pd.DataFrame({
    "A": [1,2,np.nan,4],
    "B": [5,np.nan,7,8]
})

print(df)
```

---

## 🔹 Eksik veri kontrolü

```python
print(df.isnull())
```

True/False verir.

---

## 🔹 Kaç tane eksik var?

```python
print(df.isnull().sum())
```

Her sütundaki eksik sayısı.

---

# 🔵 dropna()

Eksik olan satırları siler.

```python
print(df.dropna())
```

NaN olan satır gider.

---

# 🔵 fillna()

Eksik veriyi doldurur.

---

## 0 ile doldur

```python
print(df.fillna(0))
```

---

## Ortalama ile doldur

```python
print(df.fillna(df.mean()))
```

Bu çok kullanılır.

AI’da genelde:

* Mean
* Median

ile doldurulur.

---

# 🔥 GERÇEK HAYAT AI SÜRECİ

1️⃣ CSV dosyası yüklenir
2️⃣ df.head() ile bakılır
3️⃣ df.isnull().sum() ile eksik kontrol edilir
4️⃣ fillna yapılır
5️⃣ Gereksiz sütunlar silinir
6️⃣ Yeni feature oluşturulur
7️⃣ Model eğitilir

---

TRAIN – TEST SPLIT

Modeli test etmeden eğitmek hatadır.

Veri ikiye bölünür:

Train (öğrenme)

Test (değerlendirme)

from sklearn.model_selection import train_test_split

X = df[["Age", "Score"]]
y = df["Passed"]

X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.2,
    random_state=42
)
Parametreler

test_size=0.2 → %20 test

random_state=42 → her seferinde aynı bölme

AI Bağlantısı

Model:

model.fit(X_train, y_train)
model.score(X_test, y_test)

Test set olmadan model değerlendirilmez.

---

SCALING / NORMALIZATION
➜ NEREYE EKLEMELİSİN?

👉 Train-Test Split bölümünden hemen sonra

🟢 FEATURE SCALING

AI modelleri büyük sayılardan etkilenir.

Örnek:

Maaş: 100000

Yaş: 25

Maaş modeli domine eder.

Çözüm: Scaling

StandardScaler
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
Neden transform ayrı?

Test verisi öğrenmez.

Sadece train üzerinden öğrenilen ortalama ve std kullanılır.

AI’da Neden Önemli?

Logistic regression

Neural network

KNN

SVM

Scaling olmadan kötü sonuç verir.

---

# MATPLOTLIB

Python’da grafik çizme kütüphanesi.

Genelde şöyle import edilir:

```python
import matplotlib.pyplot as plt
import numpy as np
```

`plt` = plot demek.

---

# 1️⃣ LINE PLOT (Çizgi Grafiği)

En temel grafik türü.

### Basit örnek:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.show()
```

### Bu ne yaptı?

* x ekseni → 1,2,3,4
* y ekseni → 10,20,25,30
* Noktaları birleştirdi

📌 `plt.show()` grafiği ekrana bastırır.

---

## Sinüs Grafiği (Çok klasik örnek)

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 2*np.pi, 100)
y = np.sin(x)

plt.plot(x, y)
plt.show()
```

### Burada ne oldu?

`np.linspace(0, 2*np.pi, 100)`
→ 0 ile 2π arasında 100 sayı üretir.

`np.sin(x)`
→ her x için sinüs değeri hesapladı.

Bu grafik:
📈 dalgalı sinüs eğrisi çizdi.

AI’da nerede kullanılır?

* Loss grafiği
* Accuracy grafiği
* Zaman serileri

---

## Grafik güzelleştirme

```python
plt.plot(x, y)
plt.title("Sinus Graph")
plt.xlabel("X Axis")
plt.ylabel("Sin(X)")
plt.grid()
plt.show()
```

* title → başlık
* xlabel → x ekseni adı
* ylabel → y ekseni adı
* grid → arka plan çizgileri

---

# 2️⃣ SCATTER PLOT (Nokta Grafiği)

Noktaları birleştirmez.

Veri dağılımını gösterir.

```python
x = np.random.rand(50)
y = np.random.rand(50)

plt.scatter(x, y)
plt.show()
```

### Ne oldu?

* 50 rastgele x
* 50 rastgele y
* Grafikte 50 nokta

📌 AI’da ÇOK önemli:

* Veri dağılımı
* Sınıflar arası ayrım
* Outlier (aykırı değer) görme

---

## Renkli Scatter

```python
colors = np.random.rand(50)

plt.scatter(x, y, c=colors)
plt.show()
```

`c=` → renklendirme.

---

# 3️⃣ HISTOGRAM

Dağılım grafiği.

"Veriler hangi aralıkta yoğun?"

```python
data = np.random.randn(1000)

plt.hist(data, bins=30)
plt.show()
```

### Açıklama:

* 1000 rastgele normal dağılım sayı
* bins=30 → 30 bölme

Ne görürüz?
🔔 Çan eğrisi

AI’da:

* Veri normal mi?
* Aykırı değer var mı?
* Feature scaling gerekli mi?

---

# 4️⃣ BAR PLOT (Sütun Grafiği)

Kategorik veri için.

```python
categories = ["A", "B", "C"]
values = [10, 20, 15]

plt.bar(categories, values)
plt.show()
```

Ne oldu?

* A → 10
* B → 20
* C → 15

Sütun grafik oluştu.

---

## Örnek: Öğrenci notları

```python
students = ["Ali", "Ayşe", "Mehmet"]
grades = [85, 90, 78]

plt.bar(students, grades)
plt.title("Student Grades")
plt.show()
```

AI’da:

* Sınıf bazlı ortalama
* Model performans karşılaştırma
* Kategori sayıları

---

# AI İçin Kritik Kullanım

En çok göreceğin grafik:

## 📉 Loss Grafiği

```python
epochs = [1,2,3,4,5]
loss = [0.9, 0.7, 0.5, 0.4, 0.3]

plt.plot(epochs, loss)
plt.title("Training Loss")
plt.show()
```

Bu grafik şunu gösterir:
Model öğreniyor mu?

Azalıyorsa → iyi.
Artıyorsa → problem var.

---

# 🧠 Mantık Özeti

| Grafik Türü | Ne Gösterir            | AI'da Kullanımı |
| ----------- | ---------------------- | --------------- |
| Line Plot   | Zamanla değişim        | Loss, accuracy  |
| Scatter     | Nokta dağılımı         | Veri analizi    |
| Histogram   | Dağılım                | Normal mi?      |
| Bar         | Kategori karşılaştırma | Model kıyaslama |

---

# 🔥 En Önemli Kavram

Matplotlib mantığı:

```
1) Veriyi hazırla
2) plt.xxx ile grafiği çiz
3) plt.show()
```


EXCEPTION HANDLING (HATA YAKALAMA)

Program hata verirse durur.

Ama biz hatayı yakalayabiliriz.

try – except
try:
    x = int(input("Sayı gir: "))
    print(x)
except ValueError:
    print("Geçerli bir sayı gir.")

Ne oldu?

Hata oluşursa program çökmedi

except bloğu çalıştı

Birden Fazla Exception
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Sıfıra bölünemez.")
finally

Her durumda çalışır.

try:
    x = int("10")
except:
    print("Hata var")
finally:
    print("Bu her zaman çalışır")
AI Bağlantısı

Dosya okurken:

try:
    df = pd.read_csv("data.csv")
except FileNotFoundError:
    print("Dosya bulunamadı")

Profesyonel projelerde zorunludur.


# Troubleshooting (Hata Çözme Mantığı)

Programlama = %40 yazmak, %60 hata çözmek.

Önemli olan hata görünce paniklememek.

---

## 1️⃣ ImportError

### Hata:

```python
ImportError: No module named 'numpy'
```

### Ne demek?

Python diyor ki:

> Bu kütüphane bilgisayarında kurulu değil.

### Çözüm:

Terminal aç:

```bash
pip install numpy
```

Eğer Jupyter kullanıyorsan hücreye yazabilirsin:

```python
!pip install numpy
```

---

### Neden olur?

* Sanal ortam farklıdır
* Python sürümleri karışıktır
* Kütüphane hiç yüklenmemiştir

---

### Profesyonel İpucu

Aktif Python sürümünü kontrol et:

```bash
where python   # Windows
which python   # Mac/Linux
```

Çünkü bazen pip başka yere kurar.

---

## 2️⃣ Jupyter Çalışmıyor

### Hata:

```bash
'jupyter' is not recognized
```

Çözüm:

```bash
pip install jupyter
```

Sonra:

```bash
jupyter notebook
```

---

### Kernel Sorunu

Kod çalışmıyorsa:

* Sağ üstte Kernel seçili mi?
* Restart Kernel yap

Çoğu problem buradan çıkar.

---

## 3️⃣ Plot Görünmüyor

Kod:

```python
plt.plot(x,y)
```

Ama grafik çıkmıyor.

### Sebep:

`plt.show()` yok.

Çözüm:

```python
plt.plot(x,y)
plt.show()
```

---

### Jupyter’da Bazen Şu Gerekir:

```python
%matplotlib inline
```

---

# Hata Okuma Sanatı

Önemli kural:

Hatanın EN ALT SATIRINI oku.

Örnek:

```python
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

Bu ne demek?

Sayı + string toplamaya çalıştın.

---

## Örnek Hata

```python
x = 5
y = "10"
print(x + y)
```

Çözüm:

```python
print(x + int(y))
```

---

## Shape Hatası (AI’da çok olur)

```python
ValueError: shapes (3,2) and (3,2) not aligned
```

Matrix çarpımı için:

(A m×n) @ (B n×p)

Ortadaki boyut eşit olmalı.

---

# 🧠 Troubleshooting Mantık Formülü

1. Hata mesajını oku
2. Hangi satırda?
3. Veri tipi nedir?
4. .shape nedir?
5. print() ile debug yap

---

---

# Best Practices (Profesyonel Kod Yazma)

Bu kısım seni öğrenci seviyesinden geliştirici seviyesine çıkarır.

---

## 1️⃣ Açık Değişken İsimleri

❌ Kötü:

```python
a = 90
b = 85
c = (a+b)/2
```

✔ İyi:

```python
math_score = 90
physics_score = 85
average_score = (math_score + physics_score) / 2
```

Kod okunur hale geldi.

---

## 2️⃣ Docstring Yaz

Fonksiyonun ne yaptığını açıkla.

```python
def calculate_average(scores):
    """
    Takes a list of scores
    Returns their average
    """
    return sum(scores)/len(scores)
```

Profesyonel projelerde zorunludur.

---

## 3️⃣ NumPy Kullan (List Yerine)

❌ Kötü:

```python
numbers = [1,2,3,4]

squared = []
for n in numbers:
    squared.append(n**2)
```

✔ İyi:

```python
numbers = np.array([1,2,3,4])
squared = numbers ** 2
```

Daha kısa.
Daha hızlı.
Daha temiz.

---

## 4️⃣ Döngü Yerine Vectorization Kullan

AI’da performans her şeydir.

---

### Karşılaştırma

```python
import numpy as np
import time

arr = np.random.rand(1000000)

# Loop
start = time.time()
result = []
for x in arr:
    result.append(x**2)
print("Loop time:", time.time() - start)

# Vectorized
start = time.time()
result = arr**2
print("Vectorized time:", time.time() - start)
```

Vectorization 50-100 kat hızlı olabilir.

---

## Neden?

Çünkü NumPy:

* C dilinde yazılmıştır
* Bellek bloklarıyla çalışır
* Python loop’tan kaçınır
