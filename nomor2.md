# Tugas 2

**menghitung jarak**

**Mencari jarak dengan methode Euclidia Distance**



### **EICLIDEAN DISTANCE**

<P ALIGN = JUSTIFY>Jarak yang paling terkenal yang digunakan untuk data numerik adalah jarak Euclidean. Ini adalah kasus khusus dari jarak Minkowski ketika m = 2. Jarak Euclidean berkinerja baik ketika digunakan untuk kumpulan data cluster kompak atau terisolasi . Meskipun jarak Euclidean sangat umum dalam pengelompokan, ia memiliki kelemahan: jika dua vektor data tidak memiliki nilai atribut yang sama, kemungkin memiliki jarak yang lebih kecil daripada pasangan vektor data lainnya yang mengandung nilai atribut yang sama. Masalah lain dengan jarak Euclidean sebagai fitur skala terbesar akan mendominasi yang lain. Normalisasi fitur kontinu adalah solusi untuk mengatasi kelemahan ini.</P>
```python
import  pandas as pd
pd.read_csv("dataset.csv")
import math
```

```python
def Euclidean(i,j):
    hasil = 0
    for k in range(len(df)-1):
        rumus = (i[k]-j[k])**2
        hasil = hasil + rumus
    return math.sqrt(hasil)
print("M=2")
print("jarak kedua fitur :",Euclidean(df['hr'],df['weekday']))
```

***Output*** :

```python
jarak kedua objek adalah : 1473.2039913060241
```



### MANHATTAN DISTANCE

<P ALIGN="JUSTIFY">Manhattan distance adalah kasus khsusu dari jarak Minkowski distance pada m = 1. Seperti Minkowski Distance, Manhattan distance sensitif terhadap outlier. BIla ukuran ini digunakan dalam algoritma clustering , bentuk cluster adalah hyper-rectangular. Ukuran ini didefinisikan dengan</P>
```python
import  pandas as pd
pd.read_csv("dataset.csv")
import math
```


```python
def Manahattan(i,j):
    hasil = 0
    for k in range(len(df)-1):
        rumus = i[k]-j[k]
        hasil = hasil + rumus
    return hasil
print("jarak kedua fitur :",Manahattan(df['casual'],df['registered']))
```
***Output*** :

```python
jarak kedua objek adalah : -2052620
```

