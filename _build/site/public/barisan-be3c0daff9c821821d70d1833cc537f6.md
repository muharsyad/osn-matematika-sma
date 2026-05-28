# Barisan Bilangan

## Dasar-Dasar Barisan dan Notasi Sigma dan Produk

Dalam analisis matematika, barisan merupakan struktur fundamental yang merepresentasikan urutan objek matematis yang disusun berdasarkan pola tertentu. Dalam konteks matematika, pemahaman yang mendalam mengenai sifat-sifat barisan beserta teknik manipulasi notasinya merupakan prasyarat multak sebelum mempelajari teknik penyederhanaan deret, induksi matematika, dan relasi rekursif.

:::{prf:definition}
Sebuah barisan bilangan real adalah suatu fungsi $f$ yang memetakan himpunan bilangan asli $\mathbb{N}$ (atau himpunan bagian dari $\mathbb{N}$) ke himpunan bilangan real $\mathbb{R}$.\
Jika $f:\mathbb{N}\to \mathbb{R}$, maka nilai fungsi pada $n\in \mathbb{N}$ dinotasikan sebagai $a_n$ alih-alilh $f(n)$. Bilangan $a_n$ disebut sebagai suku ke-$n$ dari barisan tersebut. Secara keseluruhan, barisan bilangan dinotasikan dengan representasi $(a_n), \{a_n\}_{n=1}^\infty$, atau dijabarakan sebagai $a_1, a_2, \cdots, a_n, \cdots$
:::

### Mencari Pola Barisan

Menemukan pola adalah langkah pertama dalam analisis barisan yang tidak diketahui formulanya. Dalam level olimpiade, pola barisan jarang berupa aritmatika atau geometri sederhana. Beberapa pendekatan utama meliputi:

1. Pola Polinomial (Metode Selisih Bertingkat)\
   Jika selisih antara suku-suku yang berurutan pada barisan membentuk suatu konstant pada tingkat ke-$k$, maka suku umum $a_n$ dapat diekspresikan sebagai polinomial berderajat $k$. Dalam kurikulum sekolah standar, pencarian koefisien polinomial ini umumnya menggunakan eliminasi pada sistem persamaan linier yang sangat memakan waktu. Untuk mempercepat analisis di tingkat olimpiade, kita menggunakan pendekatan kombinatorik yang diformalkan melalu Metode Beda Hingga Newton
   ::::{prf:definition}
   Misalkan diberikan sebuah barisan bilangan real $a_1, a_2, a_3, \cdots$. Kita definisikan operator beda maju tingkat pertama, dinotasikan dengan $\Delta$, sebagai selisih antara dua suku yang berurutan:
   :::{math}
   \Delta a_n = a_{n+1}-a_n
   :::
   Secara rekursif, operator beda maju tingkat ke-$k$ (untuk $k\geq 2$) didefinisikan dari selisih barisan tingkat sebelumnya:
   :::{math}
   \Delta^ka_n = \Delta^{k-1}a_{n+1} - \Delta^{k-1}a_n
   :::
   ::::
   ::::{prf:theorem}
   Jika barisan $(a_n)$ memiliki nilai selisih yang konstan pada tingkat ke-$k$ (sehingga $\Delta^ka_n=c$ dan $\Delta^{k+1}a_n=0$), maka suku umum ke-$n$ dari barisan tersebut dapat diekspresikan sebagai kombinasi linier dari suku-suku pertama pada setiap tingkat selisihnya, yang dikalikan dengan koefisien binomial. Rumus eksaknya adalah:
   :::{math}
   a_n = a_1 \binom{n-1}{0} + \Delta a_1 \binom{n-1}{1} + \Delta^2 a_1 \binom{n-1}{2} + \dots + \Delta^k a_1 \binom{n-1}{k}
   :::
   Atau dalam notasi sigma ditulis sebagai
   :::{math}
   a_n = \sum_{k=0}^{d} \Delta^k a_n \binom{n-1}{k}
   :::
   ::::
   ::::{note}
   Bentuk $\binom{n-1}{k}$ adalah bilangan kombinasi (koefisien binomial) yang mendefinisikan banyaknya cara memilih $k$ unsur dari $n-1$ unsur, dengan definisi aljabar:
   :::{math}
   \binom{n-1}{k}=\frac{(n-1)!}{k!\cdot (n-1-k)!}
   :::
   ::::
   Dengan menggunakan Teorema Newton ini, pencarian rumus suku ke-$n$ tidak lagi memerlukan pemecahan sistem persamaan linier yang rumit. Kita hanya perlu menyusun barisan selisih bertingkatnya, mengambil angka pertama dari setiap tingkatan tersebut, dan mensubstitusikannya langsung sebagai pengali pada suku-suku koefisien binomial.
2. Pola Eksponensial / Rasio Geometri\
   Ditandai dengan rasio pembagian antara suku yang berdekatan bernilai konstan atau membentuk pola pangkat. Poal umumnya melibatkan bentuk eksponensial $C^n$.
3. Pola Alternasi (Tanda Berganti)\
   Barisan yang tandanya atau sifatnya berubah secara periodik (misal positif-negatif, atau genap-ganjil). Biasanya melibatkan komponen $(-1)^n$ atau pemisahan barisan menjadi sub-barisan untuk indeks genap $(a_{2k})$ dan ganjil $(a_{2k-1})$.
4. Pola Faktorial\
   Muncul apabila pertumbuhan nilai suku membesar dengan sangat drastis melebihi fungsi eksponensial, biasanya melibatkan bentuk perkalian menurun $n!=n\times (n-1)\times \cdot \times 1$

### Notasi Sigma

Untuk merepresentasikan penjumlahan beruntun dari suku-suku suatu barisan secara ringkas, matematika menggunakan abjad Yunani kapital Sigma $(\Sigma)$. Penggunaan notasi ini multak diperlukan untuk menyederhanakan ekspresi aljabar yang panjang dan menghindari penulisan titik-titik $\cdots$ yang ambil secara analitik.

::::{prf:definition}
Misalkan $(a_n)$ adalah sebuah barisan. Penjumlahan dari suku-suku ke-$m$ hingga suku ke-$n$ (dengan $m, n\in \mathbb{N}$, dan $m\leq n$) didefinisikan sebagai:
:::{math}
\sum_{i=m}^{n} a_i = a_m + a_{m+1} + a_{m+2} + \cdots + a_n
:::
::::

Simbol $i$ disebut sebagai indeks penjumlahan (variabel \textit{dummy}), $n$ adalah batas bawah, dan $n$ adalah batas atas. Indeks $i$ dapat diganti dengan huruf lain seperti $j, k$, atau $t$ tanpa mengubah makna matematisnya.

Sifat-Sifat Operasional Notasi Sigma
Misalkan $a_i$ dna $b_i$ adalah barisan bilangan real, dan $c$ adalah suatu konstan real. maka berlaku sifat-sifat operasional dasar berikut

1. Sifat penjumlahan konstanta\
   :::{math}
   \sum_{i=1}^{n}c= n\cdot c
   :::
2. Sifat homogenitas\
   :::{math}
   \sum_{i=m}^{n} n\cdot a_i = c\sum_{i=m}^{n} a_i
   :::
3. Sifat aditif\
   :::{math}
   \sum_{i=m}^{n} (a_i \pm b_i) = \sum_{i=m}^{n} a_i + \sum_{i=m}^{n}b_i
   :::
4. Sifat pemecahan batas\
   :::{math}
   \sum_{i=m}^{n}a_i = \sum_{i=m}^{p}a_i + \sum_{i=p+1}^{n}a_i
   :::
5. Sifat pergeseran indeks\
   :::{math}
   \sum_{i=m}^{n} a_i = \sum_{i=m}^{n+k} a_{i-k} = \sum_{i=m-k}^{n-k} a_{i+k}
   :::

### Notasi Produk

Analogi dengan notasi Sigma untuk penjumlahan berurutan, notasi huruf Yunani kapital Pi ($\Pi$) digunakan untuk menyatakan operasi perkalian beruntun dari suku-suku suatu barisan.

::::{prf:definition}
Misalkan $(a_n)$ adalah sebuah barisan bilangan real. Perkalian beruntun dari suku ke-$m$ hingga suku ke-$n$ didefinisikan secara formal sebagai
:::{math}
\prod_{i=m}^{n} a_i = a_m \cdot a_{m+1} \cdot a_{m+2} \cdot \dots \cdot a_n
:::
::::

Sebagai ilustrasi aplikatif, penulisan operasi faktorial $n!$ dapat didefinisikan secara eksak menggunakan notasi ini
:::{math}
n! = \prod_{i=1}^{n}i
:::

Sifat-sifat Operasioan Notasi Produk
Misalkan $a_i$ dan $b_i$ adalah barisan bilangan real, dan $c$ adalah konstanta real. Operasi perkalian berurutan tunduk pada hukum-hukum berikut

1. Sifat perkalian konstanta\
   :::{math}
   \prod_{i=1}^{n}c=c^n
   :::
2. Sifat Homogenitas\
   :::{math}
   \prod_{i=1}^{n} (c\cdot a_i) = c^n \cdot \prod_{i=1}^{n} a_i
   :::
3. Sifat multiplikatif\
   :::{math}
   \prod_{i=m}^{n} (a_i \cdot b_i) = \left( \prod_{i=m}^{n} a_i \right) \cdot \left( \prod_{i=m}^{n} b_i \right)
   :::
   :::{math}
   \prod_{i=m}^{n} \left(\frac{a_i}{b_i}\right) = \frac{\prod_{i=m}^{n} a_i}{\prod_{i=m}^{n} b_i}
   :::
4. Sifat pergeseran indeks\
   :::{math}
   \prod_{i=m}^{n} a_i = \prod_{i=m+k}^{n+k} a_{i-k}
   :::
5. Hubungan identitas produk dan sigma\
   :::{math}
   \ln \left( \prod_{i=m}^{n} a_i \right) = \sum_{i=m}^{n} \ln(a_i)
   :::

## Barisan dan Deret Aritmatika dan Geometri

Setelah menguasai representasi notasi operasi penjumlahan dan perkalian, analisis dilanjutnkan pada dua struktur barisan paling fundamental dalam matematika komponen diskrit, yaitu barisan aritmatika dan barisan geometri. Pada tingkat kompetisi, evaluasi terhadap kedua barisan ini tidak lagi berfokus pada visualisasi prosedural mentah, melainkan pada sifat-sifat analitik, karakteristik fungsional, perilaku limit (konvergensi), serta struktur gabungan (hibrida).

### Barisan dan Deret Aritmatika

Sebuah barisan bilangan real $(a_n)$ dikatakan sebagai barisan aritmatika jika dan hanya jika selisih antara dua suku yang berurutan selalu konstan. Nilai konstan ini disebut sebagai beda ($b$). Secara rekursif, didefinisikan $a_{n+1}-a_n=b$. Suku umum ke-$n$ dirumuskan secara eksplisit sebagai:

:::{math}
a_n = a_1 + (n-1)b
:::
Secara analitik, suku ke-$n$ dari barisan aritmatika dapat dipandang sebagai sebuah fungsi linier terhadap indeks $n$, yaitu $a_n = f(n) = bn+(a_1-b)$, di maana beda $(b)$ bertindak sebagai gradien (kemiringan) garis dan $(a_1-b)$ bertindak sebagai intersept-$y$ pada ruang kontinu.

Deret aritmatika $(S_n)$ didefinisikan sebagai jumlahan dari $n$ suku pertama barisan aritmatika. Formula baku jumlahan ini adalah:
:::{math}
S_n = \frac{n}{2}(a_1 + a_n) = \frac{n}{2}(2a_1 + (n-1)b)
:::
Jika diekspansi terhadap variabel $n$, rumus $S_n$ akan membentuk sebuah fungsi kuadrat tanpa konstanta:
:::{math}
S_n = \frac{b}{2}n^2+\left(a_1-\frac{b}{2}\right)n
:::
Karakteristik ini sangat krusial dalam identifikasi soal: jika sebuah deret $S_n$ dinyatakan dalam bentuk $An^2 + Bn$, maka deret tersebut mutlak merupakan deret aritmtaika dengan beda $b=2A$ dan suku pertama $a_1 = A+B$

Sifat-sifat Teoretis Lanjutan:
1. Sifat simteri indeks\
   Untuk sembarng indeks $i, j, k, m \in \mathbb{N}$, jika berlaku kondisi keterikatan indeks $i+j=k+m$, maka berlaku identitas penjumlahan:
   :::{math}
   a_i + a_j = a_k + a_m
   :::
2. Suku tengah\
   Jika banyaknya suku $n$ adalah bilangan ganjil, maka terdapat suku tengah eksak pada indeks $t=\frac{n+1}{2}$ yang memenuhi hubungan rataan:
   :::{math}
   a_t=\frac{a_1+a_n}{2} \implies S_n = n\cdot a_t
   :::
3. Trik representasi simetris\
   Untuk menyederhanakan perhitungan sistem persamaan aljabar yang melibatkan jumlahan suku-suku aritmtaika, pemilihan variabel sebaiknya disusun secara simetris di sekitar suku tengah
   * Untuk 3 suku: $a-b, a, a+b$
   * Untuk 4 suku: $a-3b, a-b, a+b, a+3b$

### Barisan dan Deret Geometri

Sebuah barisan bilangan real $(a_n)$ dengan unsur non-nol dikatakn sebagai barisan geometri jika dan hanya jika rasio pembagian antara dua suku yang berurutan selalu konstan. Nilia konstan ini disebut sebagai rasio ($r$). Secara rekursif, didefinisikan $\frac{a_{n+1}}{a_n}=r$. Suku umum ke-$n$ dirumuskan secara eksplisit sebagai:
:::{math}
a_n = a_1 \cdot r^{n-1}
:::
Secara analitik, suku ke-$n$ dari barisan geometri dapat dipandang sebagai fungsi eksponensial terhadap indeks $n$. Jika kita mentransformasikan barisan geometri melalui fungsi logaritma, maka barisan baru $b_n=\ln (a_n)$ secar otomatis akan membentuk barisan aritmatika dengan beda sebesar $\ln (r)$.

Jumlahan $n$ suku pertama dari barisan geometri dirumuskan secara aljabar melalui formula pecahan berikut (untuk $r\neq 1$)
:::{math}
S_n = \frac{a_1(r^n-1)}{r-1}, \text{  untuk } |r|\geq1\
S_n = \frac{a_1(1-r^n)}{1-r}, \text{  untuk } 0<|r|<1
:::

Sifat-sifat Teoretis Lanjutan
1. Sifat simetri multiplikatif indeks\
   Untuk sembarang indeks $i, j, k, m\in \mathbb{N}$, jik berlaku kondisi keterikatan indeks $i+j=k+m$, mk berlaku identitas perkalian:
   :::{math}
   a_i \cdot a_j = a_k \cdot a_m
   :::
2. Suku tengah geometri\
   Jika banyaknya suku $n$ adalah ganjil, maka kuadrat dari suku tengah $a_t$ pada indeks $t=\frac{n+1}{2}$ setara dengan hasil kali suku-ujungnya:
   :::{math}
   a_t^2 = a_1\cdot a_n = |a_t|=\sqrt{a_1\cdot a_n}
   :::
3. Trik representasi simetris\
   Jika soal olimpiade melibatkan hasil kali dari suku-suku barisan geometri, modifikasi variabel berikut sangat disarankan
   * Untuk 3 suku: $\frac{a}{r}, a, ar$

### Deret Geometri Tak Hingga dan Konvergensinya

Ketika batas atas jumlahan deret geometri diperluas hingga tak hingga $(n\to \infty)$, deret tersebtu bertransformasi menjadi deret geometri tak hingga, dinotasikan dengan 
:::{math}
S_\infty = \sum_{i=0}^{\infty} a_1 r^{i-1} = a_1 + a_1r + a_1r^2 +\cdots
:::

Perilaku dari $S_\infty$ dievaluasi berdasarkan nilai limit dari barisan jumlahan parsialnya $(S_n)$ ketika $n$ menuju tak hingga. Secara matematis, evaluasi analitik ini terbagi menjadi dua kondisi rigid:

1. Kondisi Konvergen (Memiliki Nilai Limit Tetap)\
   Deret dikatakan konvergen (memusat menju suatu nilai real tertentu) jika dan hanya jika rasio $r$ berada secara ketakt di dalam interval terbuka:
   :::{math}
   0<|r|<1
   :::
   Berdasarkan analisi limit, jika $0<|r|<1$, maka nilai $\lim_{n\to \infty} r^n=0$. Akibatnya, formula jumlahan parsial bertransformasi menjadi:
   :::{math}
   S_\infty = \lim_{n\to\infty} \frac{a_1(1-r^n)}{1-r} = \frac{a_1(1-0)}{1-r} = \frac{a_1}{1-r}
   :::
2. Kondisi Divergen (Tidak Memiliki Nilai Limit Tetap)\
   Deret dikatakan divergan (menyebar menuju tak hingga atau berosilasi) jika dan hanya jika rasio memenuhi kondisi $|r|\geq 1$
   a. Jika $r\geq 1$, nilai jumlahan akan bertumbuh tanpa batas menuju $\infty$ atau $-\infty$
   b. Jika $r\leq -1$, nilai jumlahan akan berosilasi secara ekstrem dan tidak pernah menetap pada satu titik koordinat linier.