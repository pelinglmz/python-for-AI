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

