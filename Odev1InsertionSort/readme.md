# Proje 1 (Insertion Sort)

Elimizde [22,27,16,2,18,6] şeklinde 6 elemanlı bir dizi var ve bu diziyi insertion sort 
yöntemi ile sıralamak istiyoruz.

## Yukarıda verilen dizinin insertion sort yöntemi ile aşamaları

- Insertion sort yönteminde dizinin ilk elemanı atlanır. Çünkü ilk elemanı karşılaştırabileceğimiz bir başka önceki eleman yoktur. Atlanılan bu eleman, sayı grubunun (bizim örneğimizde dizinin) sorted kısmında olduğu varsayılır. 

Yani yukarıdaki örnek ele alındığında:
[22|27,16,2,18,6] şeklinde bir başlangıç yapılır. Dik çizgi sorted ve unsorted kısımların ayrımını göstermek amacıyla kullanılır.

- Ardından kendini yineleyen iteratif işlemlere geçilir. Genellikle programlamada bu kısımda iç içe geçmiş iki adet while döngüsü kullanırız. Burada aşamalar şu şekilde ilerler;

 Unsorted kısımdaki ilk elemanı al, sorted alandaki son elemandan başlayarak karşılaştır. Karşılaştırma, daha küçük bir eleman bulunamayıncaya kadar devam eder. Bu süreçte kaydırma işlemi uygulanır.
- Örneğin unsorted alanda bulunan 27 sayısı için.
- [22|27,16,2,18,6] (Unsorted alandaki ilk eleman 27 alınır.)
- [22,27|16,2,18,6] (Kendisinden daha küçük elemanın zaten sağında. İşlemden çıkılır.)
- Örneğin devamında unsorted alanda bulunan 16 sayısı için:
- [22,27|16,2,18,6] (Unsorted alandaki ilk eleman 16 alınır.)
- [22,27,16|2,18,6] (Sorted alandaki ilk eleman 27 ile kıyaslanır. ve yerleri değiştirilir. Çünkü 16 daha küçüktür. 27 sayısının soluna kaydırılır.)
- [22,16,27|2,18,6] (Tekrar soldaki elemanla kıyaslanır. 22den küçük olduğu için yine yer değiştirme uygulanır. 16 sayısı 22 sayısının soluna kaydırılır.)
- [16,22,27|2,18,6] (Kendinden küçük eleman kalmadığı için döngü biter. Bir sonraki unsorted eleman için işlemler başlar.)

İteratif adımlar bu şekilde kendini tekrar eder ve unsorted alanda eleman kalmayınca iteratif adımlardan çıkılır. Artık elimizde sıralanmış bir dizi vardır.


## Big-Oh Gösterimi 

Big-O gösterimlerinde worst case analiz edilir. Worst case analizinde ise input(girdi) n kabul edilerek gösterilir. 

- Worst Case : Dizinin tersten sıralanmış olarak verilmesi durumudur.

Worst Case durumunda dizimiz [27,22,18,16,6,2] şeklinde verilmiş olurdu. Bu durumda en küçük sayı en başa getirilene kadar işlem yapılacak dolayısıyla (n.(n+1))/2 

Dolayısıyla  O(n^2)

## Time Complexity

Bu kısımda sorunun soruluş biçimi hatalı. Biz search değil sort işlemi yapıyoruz. Sayı aramıyoruz. Dolayısıyla Insertion sort hesaplamasında aradığımız bir sayı yok, ortada başta olması durumu da yok.

- Best Case : Dizinin zaten küçükten büyüğe sıralı verilmesi. Böyle bir durumda yapılacak tek şey sıralı çubuğunu sola kaydırmak. N tane sayı üzerinden geçeriz. O(n)
- Worst Case : Dizinin Büyükten küçüğe sıralı verilmesi. O(n^2)
- Average Case : Best case ile worst case'in ortalamasıdır. = (n+n^2)/2 = (n.(n+1))/2 = O(n^2)



## Java üzerinde kod gösterimi

```

 int i = 1,j,swap;
        while(i< array.length){
            j=i;
            while ( (j>0) && (array[j-1]>array[j]) ) {
           
                swap = array[j-1];
                array[j-1] = array[j];
                array[j] = swap;
                j--;  }
            i++; }
       

```

## 4. Soru : Dizi sıralandıktan sonra 18 sayısı hangi case'e girer ? 

Cevap : 18 sayısı herhangi bir case'e girmez, çünkü arama algoritması çözmüyoruz. 
