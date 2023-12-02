# Problem solving Plus Minus

**Soal :**


Selesaikan soal pada HackerRank tentang Plus-Minus **https://www.hackerrank.com/challenges/plus-minus/problem.**
Tantangan tersebut berupa membuat Codingan untuk menghitung proporsi elemen positif, negatif, nol dalam array. Cetak nilai desimal dari setiap pecahan pada baris baru minimal 6 tempat setelah nilai desimal. hasil output harus sesuai dengan sampel hasil output yg ada di link tersebut

 # Solusi

Disini saya menggunakkan bahasa Python 3, Lalu dalam kasus ini saya memanfaatkan fungsi filter dan ekspresi lambda untuk menghitung persentase bilangan positif, negatif, dan nol dalam sebuah array.
```python
n = len(arr)
    positif = len(tuple(filter(lambda x:x>0 , arr)))
    negatif = len(tuple(filter(lambda x:x<0, arr)))
    nol = len(tuple(filter(lambda x:x==0, arr)))
    print(positif/n)
    print(negatif/n)
    print(nol/n)
```
- Fungsi filter digunakan untuk memfilter elemen-elemen dalam sebuah array berdasarkan kriteria tertentu. Dalam hal ini, kriteria yang digunakan adalah nilai elemen array tersebut.
- Ekspresi lambda digunakan untuk membuat fungsi anonim dalam satu baris ekspresi. Dalam hal ini, ekspresi lambda digunakan untuk menentukan kriteria filter.
  
Berikut adalah implementasi dalam Python 3:

```python 
#!/bin/python3

import math
import os
import random
import re
import sys

def plusMinus(arr):

    n = len(arr)
    positif = len(tuple(filter(lambda x:x>0 , arr)))
    negatif = len(tuple(filter(lambda x:x<0, arr)))
    nol = len(tuple(filter(lambda x:x==0, arr)))
    print(positif/n)
    print(negatif/n)
    print(nol/n) 
    
if __name__ == '__main__':
    n = int(input().strip())

    arr = list(map(int, input().rstrip().split()))

    plusMinus(arr)
```
# Hasil
**Pertama :**

Input (stdin)
```
6
-4 3 -9 0 4 1
```
Your Output (stdout)
```
0.5
0.3333333333333333
0.16666666666666666
```
Expected Output
```
0.500000
0.333333
0.166667
```

**Kedua :**

Input (stdin)
```
8
1 2 3 -1 -2 -3 0 0
```
Your Output (stdout)
```
0.375
0.375
0.25
```
Expected Output
```
0.375000
0.375000
0.250000
```
