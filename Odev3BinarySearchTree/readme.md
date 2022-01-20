# Proje 3 : Binary Search Tree Projesi

[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree aşamalarını yazınız.

---
İlgili sayı dizisinin sırayla geldiğini varsayalım. <br>
Dolayısıyla root : 7<br>
- 5 değerini algoritma 7 değerinden küçük olduğu için soluna yerleştirir. Dolayısıyla 7'nin solunda 5 vardır.
- 1 değerini algoritma 5'ten küçük olduğu için 5'in soluna yerleştirir. Dolayısıyla 5'in solunda 1 vardır.
- 8 değerini algoritma 7'nin sağına yerleştirir. Dolayısıyla 7'nin sağında 8 vardır.
- 3 değerini algoritma 1'in sağına yerleştirir. Dolayısıyla 1'in sağında 3 vardır.
- 6 değerini algoritma 5'in sağına yerleştirir. Dolayısıyla 5'in sağında 6 vardır.
- 0 değerini algoritma 1'in soluna yerleştirir. Dolayısıyla 1'in solunda 0 vardır.
- 9 değerini algoritma 8'in sağına yerleştirir. Dolayısıyla 8'in sağında 9 vardır.
- 4 değerini algoritma 3'ün sağına yerleştirir. Dolayısıyla 3'ün sağında 4 vardır.
- Son olarak 2 değerini algoritma 3'ün soluna yerleştirir. Dolayısıyla 3'ün solunda 2 vardır.

Algoritmanın çalışmasının tamamlanmasının ardından binary tree aşağıdaki gibi görünür.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;&nbsp;\\<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;8<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;&nbsp;\\ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\\<br>
&nbsp;&nbsp;&nbsp;1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;9<br>
&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;\\<br>
0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;\\<br>
&nbsp;&nbsp;&nbsp;2 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4

---
## Big-o gösterimi;
- Average Case : O(logn)
- Worst Case : O(n)
- Insertion : O(logn)