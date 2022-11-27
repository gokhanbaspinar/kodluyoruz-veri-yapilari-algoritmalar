# Proje 1

---

### [22,27,16,2,18,6] -> Insertion Sort

---

#### 1) Yukarıda verilen dizinin sort türüne göre aşamalarını yazınız.

Diziyi küçükten büyüğe doğru sıralıyoruz.

**1. Aşama** [22,27,16,2,18,6] dizisinde en küçük eleman `2`, liste başındaki `22` ile yer değiştirir. &rArr; `[2,27,16,22,18,6]`\
**2. Aşama** [2,27,16,22,18,6] dizisinde `2`'den sonraki en küçük eleman `6`, liste başındaki `2`'den sonra gelen `27 (ikinci eleman)` ile yer değiştirir. &rArr; `[2,6,16,22,18,27]`\
**3. Aşama** [2,6,16,22,18,27] dizisinde `6`'dan sonraki en küçük eleman `16`'nın sıralaması doğru olduğu için sıralaması değişmez.\
**4. Aşama** [2,6,16,22,18,27] dizisinde `16`'dan sonraki en küçük eleman `18`, kendinden önce gelen `22 (dördüncü eleman)` ile yer değiştirir. &rArr; `[2,6,16,18,22,27]`\
**5. Aşama** `[2,6,16,18,22,27]` dizisinde bütün sayıların yeri doğrudur. İşlem yapılmaz.

---

#### 2) Big-O gösterimini yazınız.

`n` elemanlı bir dizi olduğunu varsayalım.
Insertion sort yönteminde bu dizideki ilk aşamada `n` tane eleman kontrol edilir, işlem yapılır.\
2. aşamada `n-1` işlem (kotrol-yer değiştirme),\
3. aşamada `n-2` işlem (kotrol-yer değiştirme) yapılır.\
4. Aşamalar en sonda `1` eleman ve `1` işlem kalana kadar devam eder.

- Algoritmada `n+(n-1)+(n-2)+...+2+1` kadar işlem yapılmış olur.
- Formül sadeleşince: `n+(n-1)+(n-2)+...+2+1` &rArr; `[n(n+1)]/2` &rArr; `(n²+n)/2`

Big-O notationda domine eden değer alınır. Bu durumda `n²` değeri alınır. Insertion sort Worst Case senaryoda `Big-O = O(n²)`'dir.

---

#### 3) Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız

Dizinin sıralanmış hali: `[2,6,16,18,22,27]`

`18` dizinin ortasındadır ve `Average case: Aradığımız sayının ortada olması` kapsamındadır.

---

### [7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.

**1-** `2` en küçük olduğu için `7` ile yer değiştirir. &rArr; [``2``,3,5,8,7,9,4,15,6]\
**2-** İkinci sırada `3` doğru yerdedir. &rArr; [2,``3``,5,8,7,9,4,15,6]\
**3-** Üçüncü sırada `4`, `5` ile yer değiştirir. &rArr; [2,3,``4``,8,7,9,5,15,6]\
**4-** Dördüncü sırada `5`, `8`' ile yer' değiştirir. &rArr; [2,3,4,``5``,7,9,8,15,6]
