# Pengantar dan Ketaksamaan

## Sistem Bilangan Real

Sebelum kita memanipulasi berbagai bentuk ketaksamaan, kita perlu menetapkan batasan atau semesta pembicaraan kita. Dalam aljabar tingkat lanjut, hampir semua operasi dilakukan dalam himpunan bilangan real. Sistem bilangan real tidak muncul begitu saja, melainkan merupakan hasil evolusi dari kebutuhan manusia untuk merepresentasikan dunia nyata secara matematis:

1. **Bilangan Asli ($\mathbb{N}$ - *Natural Numbers*)**: Ini adalah bilangan pertama yang digunakan manusia. Konteksnya lahir dari kebutuhan menghitung objek fisik, seperti jumlah ternak atau hasil panen.
$$ 
\mathbb{N} = \{1, 2, 3, \cdots\}
$$
2. **Bilangan Cacah ($\mathbb{W}$ - *Whole Numbers*)**: Berkembang ketika peradaban mulai memahami konsep "ketiadaan". Angka nol (0) ditambahkan ke dalam sistem untuk mewakili ketiadaan objek.
:::{math}
    \mathbb{W}=\{0, 1, 2, \cdots\}
:::
3. **Bilangan Bulat ($\mathbb{Z}$ - *Zahlen*)**:Lahir dari konsep perdangan, utang piutang, dan arah. Jika kita bisa memiliki 3 ekor domba, bagaimana kita mencatat bahwa kita \textit{berutang} 3 ekor domba? Di sinilah bilangan negatif muncul.
:::{math}
    \{\cdots, -2, -1, 0, 1, 2, \cdots\}
:::
4. **Bilangan Rasional ($\mathbb{Q}$ - *Quotient*)**: Konteksnya berasal dari pengukuran dan pembagian harta atau lahan. Kata rasional merujuk pada "rasio" (perbandingan). Bilangan ini adalah semua bilangan yang dapat dinyatakan dalam bentuk $\frac{a}{b}$ dengan $a,b\in \mathbb{Z}$, dan $b\neq 0$.
5. **Bilangan Irasional**: Ditemukan pertama kali oleh murid Pythagoras ketika mencoba mengukur panjang sisi miring segitiga siku-siku sama kaki dengan sisi 1 satuan. hasilnya $\sqrt{2}$, sebuah panjang yang tidak akan pernah bisa dinyatakan sebagai rasio dua bilangan bulat. Bilangan ini tidak memiliki pola berulang pada desimalnya (contoh: $\pi, \epsilon, \sqrt{2}, \sqrt{3}$).
6. **Bilangan Real ($\mathbb{R}$)**: Ini adalah gabungan dari semua bilangan rasional dan irasional. Secara visual, bilangan real merepresentasikan setiap titik yang mungkin ada pada sebuah garis lurus tak hingga (garis bilangan).

Untuk memudahkan pemahaman, berikut adalah struktur hierarki sistem bilangan dari yang paling luas hingga yang paling spesifik.

Misalkan $\mathbb{N, Z, Q}$ dan $\mathbb{R}$ berturut-turut menyatakan himpunan bilangan asli, himpunan bilangan bulat, himpunan bilangan rasional, dan himpunan bilangan real. Masing-masing himpunan ini dilengkapi dengan operasi tambah, dan operasi kali yang disebut sebagai sistem bilangan.

Sistem ini biasa ditulis dengan notasi himpunan beserta operasi. Sebagai contoh, sistem bilangan real ditulis ($\mathbb{R}, +, \times$). Selanjutnya, untuk kepraktisan, cukup ditulis notasi himpunannya saja, yaitu $\mathbb{R}$.

Berikut akan dibahas dua aksioma mendasar yang berlaku pada sistem bilangan real, yang menjadi tulang punggung dari seluruh teknik ketaksamaan yang akan kita pelajari: Aksioma Lapangan dan Aksioma Urutan.

### Aksioma Lapangan
Aksima lapangan mendefinisikan aturan main dasar dari operasi penjumlahan dan perkalian pada bilangan real.

:::{prf:axiom} Aksioma Lapangan
:label:ax-lapangan
Untuk setiap $a, b, c \in \mathbb{R}$, berlaku:
1. Sifat Tertutup
\begin{equation}
a+b\in \mathbb{R} \text{ dan } a\times b\in \mathbb{R} 
\label{eq:tertutup} % Menambahkan label di sini
\end{equation}
2. Sifat Asosiatif\
   a. $(a+b)+c = a+(b+c)$\
   b. $(a\times b)\times c=a\times (b\times c)$
3. Sifat Komutatif\
   a. $a+b=b+a$\
   b. $a\times b=b\times a$
4. Terdapat Unsur Identitas\
   a. Terdapat $0\in \mathbb{R}$ untuk semua $a\in \mathbb{R}$ yang memenuhi
    \begin{equation}
    a+0=0+a=a \label{eq:identitas_tambah}
    \end{equation}
   b. Terdapat $1\in \mathbb{R}$ untuk semua $a\in \mathbb{R}$ yang memenuhi
    \begin{equation}
    a\times 1 = 1\times a = a \label{eq:identitas_kali}
    \end{equation}
5. Terdapat Unsur Invers\
   a. Untuk setiap $a \in \mathbb{R}$ terdapat $-a\in \mathbb{R}$ sehingga 
    \begin{equation}
        a+(-a)=(-a)+a=0
        \label{eq:invers_tambah}
    \end{equation}
   b. Untuk setiap $a\in \mathbb{R}$ dengan $a\neq 0$ terdapat $a^{-1} \in \mathbb{R}$ sehingga 
    \begin{equation}
        a\times a^{-1}=a^{-1}\times a=1
        \label{eq:invers_kali}
    \end{equation}
6. Sifat Distributif\
   a. $a\times (b+c)=a\times b + a\times c$\
   b. $(a+b)\times c = a\times c + b\times c$
:::

Berdasarkan penjabaran aksioma \ref{axi:lapangan} diturunkan sejumlah sifat berikut yang dianggap sebagai teorema.

:::{prf:theorem} Konsekuensi Aksioma Lapangan
:label: thm-konsekuensi-axi-lapangan
1. $-a$ dan $a^{-1}$ yang memenuhi sifat \ref{eq:invers_tambah} dan \ref{eq:invers_kali} di atas adalah tunggal
2. $0a=0$, untuk setiap $a\in \mathbb{R}$
3. $(-1)a=-a$, untuk setiap $a\in \mathbb{R}$
4. $-(-a)=a$, untuk setiap $a\in\mathbb{R}$
5. $(-a)(-b)=ab$, untuk setiap $a, b\in \mathbb{R}$
6. $(a^{-1})^{-1}=a$, untuk setiap $a\in \mathbb{R}$ yang tidak nol.
:::

Berikut adalah pembuktian untuk masing-masing bagian pada {prf:ref}`thm-konsekuensi-axi-lapangan`

::::{prf:proof} {prf:ref}`thm-konsekuensi-axi-lapangan`
:class: dropdown
1. Ketunggal Invers
    * Invers Penjumlahan: Misalkan $x$ dan $y$ adalah invers penjumlahan dari $a$, maka $a+x=0$ dan $a+y=0$.
    :::{math}
    x &= x + 0 && \text{(sifat identitas penjumlahan)} \\
    &= x + (a + y) && \text{(sifat invers penjumlahan untuk $y$)} \\
    &= (x + a) + y && \text{(sifat asosiatif penjumlahan)} \\
    &= (a + x) + y && \text{(sifat komutatif penjumlahan)} \\
    &= 0 + y && \text{(sifat invers penjumlahan untuk $x$)} \\
    &= y && \text{(sifat identitas penjumlahan)}
    :::
    Jadi, invers penjumlahan bersifat tunggal (unik).

    * Invers Perkalian: Misalkan $x$ dan $y$ adalah invers perkalian dari $a$ (dengan $a \neq 0$), maka $a \cdot x = 1$ dan $a \cdot y = 1$.
    :::{math}
    x &= x \cdot 1 && \text{(sifat identitas perkalian)} \\
    &= x \cdot (a \cdot y) && \text{(sifat invers perkalian untuk $y$)} \\
    &= (x \cdot a) \cdot y && \text{(sifat asosiatif perkalian)} \\
    &= (a \cdot x) \cdot y && \text{(sifat komutatif perkalian)} \\
    &= 1 \cdot y && \text{(sifat invers perkalian untuk $x$)} \\
    &= y && \text{(sifat identitas perkalian)}
    :::
    Jadi, invers perkalian bersifat tunggal (unik). 
2. Ambil sembarang $a\in \mathbb{R}$
    :::{math}
    0a &= 0 + 0a && \text{(sifat identitas penjumlahan)} \\
    &= (-0a + 0a) + 0a && \text{(sifat invers penjumlahan)} \\
    &= -0a + (0a + 0a) && \text{(sifat asosiatif penjumlahan)} \\
    &= -0a + (0 + 0)a && \text{(sifat distributif)} \\
    &= -0a + 0a && \text{(sifat identitas penjumlahan untuk $0+0$)} \\
    &= 0 && \text{(sifat invers penjumlahan)}
    :::
    Jadi terbukti untuk setiap $a\in \mathbb{R}$ berlaku $0a=0$
3. Ambil sembarang $a\in\mathbb{R}$
   :::{math}
   (-1)a &= 0 + (-1)a && \text{(sifat identitas penjumlahan)} \\
    &= (-a+a)+(-1)a && \text{(sifat invers penjumlahan)} \\
    &= -a + (a+(-1)a) && \text{(sifat asosiatif penjumlahan)} \\
    &= -a + (1a+(-1)a) && \text{(sifat identitas perkalian)} \\
    &= -a + (1+(-1))a && \text{(sifat distributif)} \\
    &= -a + (0a) && \text{(sifat invers penjumlahan)} \\
    &= -a+0 && \text{(berdasarkan Sifat 2: $0a=0$)} \\
    &= -a && \text{(sifat identitas penjumlahan)}
   :::
   Jadi terbukti untuk setiap $a\in \mathbb{R}$ berlaku $(-1)a=-a$
4. Ambil sembarang $a\in \mathbb{R}$
    :::{math}
    -(-a) &= 0 + -(-a) && \text{(sifat identitas penjumlahan)} \\
    &= (a + (-a)) + -(-a) && \text{(sifat invers penjumlahan dari $a$)} \\
    &= a + ((-a) + -(-a)) && \text{(sifat asosiatif penjumlahan)} \\
    &= a + 0 && \text{(sifat invers penjumlahan dari $-a$)} \\
    &= a && \text{(sifat identitas penjumlahan)}
    :::
   Jadi terbukti untuk setiap $a\in \mathbb{R}$ berlaku $-(-a)=a$
5. Ambil sembarang $a, b\in \mathbb{R}$
    :::{math}
    (-a)(-b) &= (-a)(-b) + 0 && \text{(sifat identitas penjumlahan)} \\
    &= (-a)(-b) + 0b && \text{(berdasarkan bagian 2)} \\
    &= (-a)(-b) + (a + (-a))b && \text{(sifat invers penjumlahan)} \\
    &= (-a)(-b) + (ab + (-a)b) && \text{(sifat distributif)} \\
    &= [(-a)(-b) + (-a)b] + ab && \text{(sifat asosiatif penjumlahan)} \\
    &= (-a)(-b + b) + ab && \text{(sifat distributif)} \\
    &= (-a)0 + ab && \text{(sifat invers penjumlahan)} \\
    &= 0 + ab && \text{(berdasarkan bagian 2)} \\
    &= ab && \text{(sifat identitas penjumlahan)}
    :::
    Jadi terbukti untuk setiap $a, b\in \mathbb{R}$ berlaku $(-a)(-b)=ab$
6. Ambil sembarang $a \in \mathbb{R}$
    :::{math}
    (a^{-1})^{-1} &= 1 \cdot (a^{-1})^{-1} && \text{(sifat identitas perkalian)} \\
    &= (a \cdot a^{-1}) \cdot (a^{-1})^{-1} && \text{(sifat invers perkalian dari $a$)} \\
    &= a \cdot (a^{-1} \cdot (a^{-1})^{-1}) && \text{(sifat asosiatif perkalian)} \\
    &= a \cdot 1 && \text{(sifat invers perkalian dari $a^{-1}$)} \\
    &= a && \text{(sifat identitas perkalian)}    
    :::
    Jadi terbukti untuk setiap $a\in \mathbb{R}$ berlaku $(a^{-1})^{-1}=a$

$\blacksquare$
::::

### Aksioma Urutan
Aksioma inilah yang melahirkan konsep "ketaksamaan" (lebih besar, lebih kecil). Terdapat sebuah himpunan bagian dari $\mathbb{R}$ yang disebut sebagai himpunan bilangan real positif, dinotasikan dengan $\mathbb{R}^+$, yang memenuhi sifat-sifat berikut:

:::{prf:axiom} Aksioma Urutan
:label: axi-urutan
1. Sifat Ketertutupan\
   a. Jika $a, b \in \mathbb{R}^+$, maka $a+b\in \mathbb{R}^+$\
   b. Jika $a, b \in \mathbb{R}^+$, maka $a\times b \in \mathbb{R}^+$
2. Sifat Trikotomi
   Untuk setiap $a\in \mathbb{R}^+$, pasti dan hanya akan memenuhi tepat satu dari ketiga kemungkinan berikut:
   a. $a\in \mathbb{R}^+$ (artinya $a>0$),
   b. $a=0$, atau
   c. $a\in \mathbb{R}^-$ (artinya $a<0$)
:::

Definisi untuk relasi "lebih besar dari" dan lebih kecil dari" pada dua bilangan real dapat disusun berdasarkan selisihnya. Kita katakan $x>y$ jika hasil dari $x-y>0$, dan $y<x$ jika $y-x<0$. Kedua notasi ini saling berkaitan karena $x>y$ memiliki makna yang sama dengan $y<x$. Adapun simbol $x\geq y$ dipakai untuk menyatakan situasi di mana $x$ lebih besar dari atau sama dengan $y$.

Dari aksioma \ref{axi:urutan} ini, kita dapat menurunkan sifat-sifat operasional ketaksamaan baku (dapat dianggap sebagai teorema).

:::{prf:theorem} Konsekuensi Aksioma Urutan
:label: thm-konsekuensi-axi-urutan
1. Untuk setiap pasang bilangan real $a$ dan $b$ pasti berlaku salah satu dari $a<b$, atau $a=b$, atau $a>b$
2. Jika $a<b$ dan $b<c$, maka $a<c$
3. Jika $a<b$, maka $a+c<b+c$
4. Jika $a<b$ dan $c>0$, maka $ac<bc$
5. Jika $a>0$ dan $b>0$, maka $ab>0$
6. Jika $a<b$ dan $c<0$, maka $ac>bc$
7. Untuk setiap $a\in \mathbb{R}$ berlaku $a^2\geq 0$. Selanjutnya, $a^2=0$ jika dan hanya jika $a=0$
8. Jika $a>b>0$, maka $\frac{1}{a}<\frac{1}{b}$
9. Jika $a>b>0$ dan $c>d>0$, maka $ac>bd$ dan $\frac{a}{d}>\frac{b}{c}$
10. Jika $a>b$, maka $a^n > b^n$ untuk $n$ bilangan asli ganjil
11. Jika $a>b>0$, maka $a^n > b^n$ untuk $n$ bilangan asli
:::

Berikut adalah pembuktian untuk masing-masing bagian pada {prf:ref}`thm-konsekuensi-axi-urutan`

::::{prf:proof} {prf:ref}`thm-konsekuensi-axi-urutan`
:class: dropdown
1. Ambil sembarang bilangan real $a$ dan $b$. Berdasarkan sifat ketertutupan pada bilangan real, nilai $a - b$ juga merupakan bilangan real. Berdasarkan Aksioma Trikotomi pada himpunan bilangan real positif ($\mathbb{R}^+$), untuk bilangan $a - b \in \mathbb{R}$, pasti memenuhi tepat satu dari tiga kemungkinan berikut:
    * $a - b \in \mathbb{R}^+$, yang ekuivalen dengan $a > b$,
    * $a - b = 0$, yang ekuivalen dengan $a = b$, atau
    * $-(a - b) \in \mathbb{R}^+ \implies b - a \in \mathbb{R}^+$, yang ekuivalen dengan $a < b$.
Jadi, terbukti bahwa selalu berlaku salah satu dari $a < b$, $a = b$, atau $a > b$.

2. Berdasarkan definisi ketaksamaan, karena $a < b$, maka $b - a \in \mathbb{R}^+$. Demikian pula karena $b < c$, maka $c - b \in \mathbb{R}^+$. Karena himpunan bilangan real positif ($\mathbb{R}^+$) bersifat tertutup terhadap operasi penjumlahan, maka jumlah dari kedua elemen tersebut juga berada di $\mathbb{R}^+$, sehingga diperoleh:
:::{math}
(b - a) + (c - b) &\in \mathbb{R}^+ \\
c - a &\in \mathbb{R}^+.
:::
Pernyataan $c - a \in \mathbb{R}^+$ ekuivalen dengan $a < c$. Jadi, terbukti bahwa $a < c$.

3. Berdasarkan definisi, karena $a < b$, maka $b - a \in \mathbb{R}^+$. Untuk membuktikan bahwa $a + c < b + c$, kita harus menunjukkan bahwa $(b + c) - (a + c) \in \mathbb{R}^+$. Perhatikan operasi aljabar berikut:
:::{math}
(b + c) - (a + c) &= b + c - a - c \\
&= b - a + (c - c) \\
&= b - a + 0 \\
&= b - a.
:::
Karena telah diketahui bahwa $b - a \in \mathbb{R}^+$, maka $(b + c) - (a + c)$ juga merupakan elemen dari $\mathbb{R}^+$. Dengan demikian, terbukti bahwa $a + c < b + c$.

4. Karena $a < b$, maka $b - a \in \mathbb{R}^+$. Selanjutnya, karena $c > 0$, maka $c \in \mathbb{R}^+$. Berdasarkan Aksioma Urutan, $\mathbb{R}^+$ bersifat tertutup terhadap operasi perkalian, sehingga hasil kali kedua elemen tersebut juga berada di dalam $\mathbb{R}^+$:
:::{math}
(b - a)c &\in \mathbb{R}^+.
:::
Dengan menerapkan sifat distributif, ekspresi di atas dapat dijabarkan menjadi $bc - ac \in \mathbb{R}^+$. Pernyataan ini ekuivalen dengan $ac < bc$. Jadi, pembuktian selesai.

5. Berdasarkan definisi, $a > 0$ berarti $a \in \mathbb{R}^+$, dan $b > 0$ berarti $b \in \mathbb{R}^+$. Karena $\mathbb{R}^+$ tertutup terhadap perkalian, maka hasil kalinya yaitu $ab$ juga harus merupakan elemen dari $\mathbb{R}^+$. Pernyataan $ab \in \mathbb{R}^+$ memiliki makna yang sama dengan $ab > 0$. Jadi, terbukti bahwa $ab > 0$.

6. Karena $a < b$, maka $b - a \in \mathbb{R}^+$. Di sisi lain, karena $c < 0$, maka berdasarkan definisi nilai negatif, invers penjumlahannya haruslah positif, yaitu $-c \in \mathbb{R}^+$. Karena $\mathbb{R}^+$ tertutup terhadap perkalian, maka:
:::{math}
(b - a)(-c) &\in \mathbb{R}^+ \\
-bc + ac &\in \mathbb{R}^+ \\
ac - bc &\in \mathbb{R}^+.
:::
Pernyataan $ac - bc \in \mathbb{R}^+$ ekuivalen dengan $ac > bc$. Jadi, terbukti bahwa arah ketaksamaan berbalik ketika dikalikan bilangan negatif.

7. Berdasarkan Aksioma Trikotomi, terdapat tiga kemungkinan untuk bilangan $a$, yaitu $a \in \mathbb{R}^+$, $a = 0$, atau $-a \in \mathbb{R}^+$.
    * Kasus 1: Jika $a \in \mathbb{R}^+$, karena $\mathbb{R}^+$ tertutup terhadap perkalian, maka $a \cdot a \in \mathbb{R}^+$. Artinya $a^2 > 0$.
    * Kasus 2: Jika $a = 0$, maka berdasarkan sifat perkalian dengan nol, $a^2 = 0 \cdot 0 = 0$.
    * Kasus 3: Jika $-a \in \mathbb{R}^+$, karena $\mathbb{R}^+$ tertutup terhadap perkalian, maka $(-a)(-a) \in \mathbb{R}^+$. Berdasarkan sifat bilangan real, $(-a)(-a) = a^2$, sehingga $a^2 \in \mathbb{R}^+$, yang berarti $a^2 > 0$.
Dari ketiga kasus di atas, nilai $a^2$ hanya mungkin positif atau nol, sehingga disimpulkan $a^2 \geq 0$. Selanjutnya, dari kasus-kasus tersebut terlihat jelas bahwa nilai $a^2 = 0$ hanya terjadi secara eksklusif pada Kasus 2, yaitu ketika $a = 0$.

8. Pertama, karena $a > 0$, maka invers perkaliannya juga positif, yaitu $\frac{1}{a} > 0$. (Jika sebaliknya $\frac{1}{a} \leq 0$, maka saat dikalikan $a > 0$ akan menghasilkan $1 \leq 0$, yang mana kontradiksi karena $1 = 1^2 > 0$). Dengan alasan yang sama, $\frac{1}{b} > 0$.\
Karena $a > 0$ dan $b > 0$, berdasarkan Bagian 5, $ab > 0$. Akibatnya, invers perkalian dari $ab$ juga positif, yaitu $\frac{1}{ab} > 0$.\
Selanjutnya, kita mulai dari ketaksamaan yang diketahui yaitu $a > b$. Kalikan kedua ruas dengan $\frac{1}{ab}$, yang merupakan bilangan positif. Berdasarkan Bagian 4, tanda ketaksamaan tidak berubah, sehingga diperoleh:
:::{math}
a \left(\frac{1}{ab}\right) &> b \left(\frac{1}{ab}\right) \\
\frac{1}{b} &> \frac{1}{a}.
:::
Pernyataan $\frac{1}{b} > \frac{1}{a}$ ekuivalen dengan $\frac{1}{a} < \frac{1}{b}$. Jadi, terbukti.

9.  Karena $a > b$ dan $c > 0$, berdasarkan Bagian 4 berlaku $ac > bc$. Selanjutnya, karena $c > d$ dan diketahui $b > 0$, kalikan kedua ruas dengan $b$ sehingga diperoleh $bc > bd$. Berdasarkan sifat transitif ketaksamaan (Bagian 2), dari $ac > bc$ dan $bc > bd$ dapat disimpulkan bahwa $ac > bd$.\
Berdasarkan Bagian 8, karena $c > d > 0$, maka berlaku $\frac{1}{c} < \frac{1}{d}$, yang dapat ditulis sebagai $\frac{1}{d} > \frac{1}{c} > 0$.\
Kita mulai dari $a > b > 0$. Kalikan kedua ruas dengan $\frac{1}{d} > 0$, sehingga diperoleh $\frac{a}{d} > \frac{b}{d}$.\
Selanjutnya, karena $\frac{1}{d} > \frac{1}{c}$ dan $b > 0$, kalikan kedua ruas dengan $b$ sehingga diperoleh $\frac{b}{d} > \frac{b}{c}$.\
Dengan menggunakan sifat transitif kembali, dari $\frac{a}{d} > \frac{b}{d}$ dan $\frac{b}{d} > \frac{b}{c}$ disimpulkan secara mutlak bahwa $\frac{a}{d} > \frac{b}{c}$.

10.  Kita dapat membagi pembuktian ini ke dalam tiga kasus yang saling lepas berdasarkan tanda dari $a$ dan $b$:
    * Kasus 1 ($a > b \geq 0$):
        Jika keduanya bernilai non-negatif, maka pembuktiannya akan merujuk langsung pada Bagian 11 (dibuktikan di bawah), di mana $a^n > b^n$ berlaku untuk seluruh bilangan asli $n$, termasuk $n$ ganjil.
    * Kasus 2 ($a > 0 > b$)
        Karena $a$ positif, maka $a^n > 0$. Karena $b$ negatif dan $n$ merupakan bilangan ganjil, maka pangkat ganjil dari bilangan negatif akan tetap negatif, sehingga $b^n < 0$. Karena bilangan positif selalu lebih besar dari bilangan negatif, jelas terbukti bahwa $a^n > b^n$.
    * Kasus 3 ($0 \geq a > b$):
        Misalkan $x = -b$ dan $y = -a$. Karena $0 \geq a > b$, maka $x > y \geq 0$. Berdasarkan Bagian 11, berlaku $x^n > y^n$, yang berarti $(-b)^n > (-a)^n$. Karena $n$ ganjil, bentuk tersebut ekuivalen dengan $-b^n > -a^n$. Tambahkan $(a^n + b^n)$ ke kedua ruas, sehingga diperoleh $a^n > b^n$.

Karena ketiga kasus bernilai benar, terbukti bahwa $a^n > b^n$ untuk $n$ ganjil.

11. Untuk membuktikan hal ini tanpa menggunakan induksi, kita dapat memanfaatkan sifat pemfaktoran aljabar bentuk selisih pangkat $n$. Ingat kembali identitas aljabar berikut yang berlaku untuk sembarang bilangan asli $n$:
:::{math}
a^n - b^n = (a - b)(a^{n-1} + a^{n-2}b + a^{n-3}b^2 + \dots + ab^{n-2} + b^{n-1})
:::
Mari kita analisis elemen-elemen dari masing-masing faktor di ruas kanan:
    * *Faktor pertama*: Karena diketahui $a > b$, maka berdasarkan definisi ketaksamaan, diperoleh $(a - b) \in \mathbb{R}^+$.
    * *Faktor kedua*: Karena diketahui $a > 0$ dan $b > 0$, maka setiap suku tunggal pada faktor kedua (yaitu $a^{n-1}$, $a^{n-2}b$, dan seterusnya hingga $b^{n-1}$) murni merupakan hasil kali bilangan-bilangan positif. Mengingat $\mathbb{R}^+$ bersifat tertutup terhadap operasi perkalian dan penjumlahan, maka keseluruhan panjang faktor kedua ini juga pasti bernilai positif, atau elemen dari $\mathbb{R}^+$.

Berdasarkan Aksioma Urutan, karena $\mathbb{R}^+$ tertutup terhadap perkalian, maka hasil kali dari faktor pertama dan faktor kedua juga harus berada di dalam $\mathbb{R}^+$. Akibatnya diperoleh:
:::{math}
a^n - b^n \in \mathbb{R}^+
:::
Pernyataan $a^n - b^n \in \mathbb{R}^+$ memiliki makna yang ekuivalen dengan $a^n > b^n$. Jadi, terbukti secara aljabar bahwa untuk setiap bilangan asli $n$, berlaku $a^n > b^n$.
$\blacksquare$
::::

## Ketaksamaan

### Kuadrat Bilangan Ral Selalu Non-Negatif
Pada Teorema \ref{thm:konsekuensi_axi_urutan} poin ke-7, kita telah melihat sebuah sifat yang sangat istimewa:

:::{prf:theorem}
Misalkan $x\in \mathbb{R}$, maka
\begin{equation}
    x^2 \geq 0
\end{equation}
dengan kesamaan terjadi jika dan hanya jika $x=0$
:::

:::{prf:proof}
:class: dropdown
Berdasarkan Sifat Trikotomi, untuk setiap $a\in \mathbb{R}$, hanya ada tiga kemungkinan:
1. Jika $a=0$, maka $a^2=0\times 0=0$. (Memenuhi $a^2\geq 0$)
2. Jika $a>0$ (atau $a\in \mathbb{R}^+$), maka berdasarkan sifat ketertutupan perkalian bilangan positif, $a\times a \in \mathbb{R}^+$. Artinya $a^2>0$.
3. Jika $a<0$, maka $-a>0$. Berdasarkan sifat ketertutupan perkalian bilangan positif, $(-a)\times (-a)\in \mathbb{R}^+$. Karena $(-a)\times (-a)=a^2$, maka $a^2>0$

Dari ketiga kasus di atas, terbukti bahwa untuk setiap $a\in \mathbb{R}$, nilai $a^2$ selalu lebih besar dari atau sama dengan nol. $\blacksquare$
:::

Sifat ini tampaknya sederhana, namun di dalam olimpiade matematika, fakta bahwa "kuadrat bilangan real tidak pernah negatif" adalah pondasi dasar dari hampir semua teknik pembuktian ketaksamaan.

Dari bentuk tunggal di atas, kita dapat memperluas menjadi penjumlahan beberapa bentuk kuadrat.

:::{prf:theorem}
Misalkan $x_1, x_2, x_3, \cdots, x_n \in \mathbb{R}$, maka
\begin{equation}
    x_1^2 + x_2^2 + x_3^2 + \cdots + x_n^2 \geq 0
\end{equation}
dengan kesamaan terjadi jika dan hanya jika $x_1 = x_2 = x_3 =\cdots = x_n = 0$
:::

Pembuktian Teorema 1.4 ini dapat dibagi menjadi dua tahapan utama yaitu membuktikan ketaksamaan dasar dan membuktikan syarat kesamaannya.
::::{prf:proof}
:class: dropdown
**Tahap 1: $x_1^2 + x_2^2 + \dots + x_n^2 \ge 0$**

Berdasarkan Teorema {prf:ref}`thm-konsekuensi-axi-urutan` kita telah mengetahui baha kuadrat dari sembarang bilangan real selalu bernilai non-negatif. Dengan kata lain, untuk setiap $x_i \in \mathbb{R}$ dengan $i = 1, 2, \dots, n$, berlaku:
:::{math}
x_1^2 &\ge 0 \\
x_2^2 &\ge 0 \\
&\vdots \\
x_n^2 &\ge 0
:::
Karena himpunan bilangan real positif dan nol bersifat tertutup terhadap operasi penjumlahan, maka jumlah dari sekumpulan bilangan yang masing-masing non-negatif tersebut juga pasti bernilai non-negatif. Dengan menjumlahkan seluruh pertidaksamaan di atas, kita peroleh:
:::{math}
x_1^2 + x_2^2 + x_3^2 + \dots + x_n^2 \ge 0
:::
Tahap pertama terbukti.

**Tahap 2**
::::

Sifat ini memungkinkan kita untuk membangun ketaksamaan-ketaksamaan baru yang sangat berguna. Salah satu bentuk turunan adalah sebagai berikut:

:::{prf:theorem}
Untuk setiap bilangan real $x$ dan $y$, berlaku:
\begin{equation}
    x^2+y^2 \geq 2xy
\end{equation}
Kesamaan terjadi jika dan hanya jika $x=y$
:::

:::{prf:proof}
:class: dropdown
Kita mulai dari fakta fundamental bahwa kudrat dari bilangan real $(x-y)$ tidak mungkin negatif:
$$ 
(x-y)^2 \geq 0
$$
Bila kita jabarkan bentuk di ruas kiri, kita peroleh
$$ 
x^2-2xy+y^2 \geq 0
$$
Tambahkan $2xy$ pada kedua ruas (berdasarkan Teorema \ref{thm:konsekuensi_axi_urutan}) poin ke-3, sehingga diperoleh:
$$ 
x^2+y^2\geq 2xy
$$
Kesamaan terjadi apabila $(x-y)^2=0$, yang berakibat $x-y=0$, atau $x=y$. $\blacksquare$
:::

:::::{prf:example}
:label: contoh-1.1
Buktikan bahwa untuk setiap bilangan real positif $a$, berlaku $a+\frac{1}{a} \geq 2$. Kapan kesamaan tersebut terjadi?
::::{solution} contoh-1.1
:class: dropdown
Diketahui bahwa $a$ bilangan real positif sehingga $\sqrt{a}$ terdefinisi. Oleh karena itu, dengan menggunakan teorema kuadrat bilangan real tak negatif, diperoleh
:::{math}
\begin{aligned}
    \left(\sqrt{a}+\frac{1}{\sqrt{a}}\right)^2 \geq 0\\
    \sqrt{a}^2-2\sqrt{a}\cdot\frac{1}{\sqrt{a}}+\left(\frac{1}{\sqrt{a}}\right)^2 \geq 0\\
    a - 2 + \frac{1}{a} \geq 0
\end{aligned}
:::
dengan menambahkan 2 pada kedua ruas, diperoleh
:::{math}
\begin{aligned}
    a - 2 + \frac{1}{a} + 2\geq 0+2\\
    a + \frac{1}{a} \geq 2
\end{aligned}
:::
Jadi terbukti bahwa $a + \frac{1}{a}\geq 2$. Kemudian, kesamaan terjadi jika dan hanya jika
:::{math}
\begin{aligned}
    \left(\sqrt{a}-\frac{1}{\sqrt{a}}\right)=0\\
    \sqrt{a}=\frac{1}{\sqrt{a}}
\end{aligned}
:::
Kalikan kedua ruas dengan $\sqrt{a}$
:::{math}
\begin{aligned}
    \sqrt{a}\cdot \sqrt{a} = \frac{1}{\sqrt{a}}\cdot \sqrt{a}\\
    a=1
\end{aligned}
:::
::::
:::::

:::::{prf:example}
:label: contoh-1.2
Buktikan bahwa untuk setiap bilangan real $x$ dan $y$, berlaku $x^2+4y^2 \geq 4xy$. Tentukan kondisi kesamaannya.
::::{solution} contoh-1.2
:class: dropdown
Diketahui bahwa $x$ dan $y$ bilangan real, sehingga dengan menggunakan teorema kuadrat real tak negatif, diperoleh
:::{math}
:::{math}
    (x-2y)^2\geq 0\\
    x^2 - 4xy + 4y^2 \geq 0
:::
:::
Tambahkan kedua ruas dengan $4xy$
:::{math}
:::{math}
    x^2-4xy+4y^2+4xy \geq 0 +4xy\\
    x^2 + 4y^2 \geq 4xy
:::
:::
Jadi terbukti bahwa $x^2 + 4y^2 \geq 4xy$. Kemudian kesamaan terjadi jika dan hanya jika
:::{math}
:::{math}
    (x-2y)=0 \implies x=2y
:::
:::
::::
:::::

:::{exercise}
:label: exe-1.1
Diberikan bilangan real $a, b, c$. Buktikan ketaksamaan $a^2 + b^2 + c^2 \geq ab+bc+ca$ dengan memanipulasi ekspresi $(a-b)^2+(b-c)^2+(c-a)^2\geq 0$
:::

::::{exercise}
:label: exe-1.2
Diberikan bilangan real positif $a, b, c$. Dengan mengeksploitasi bentuk kuadrat, buktikan bahwa
:::{math}
    \frac{a^2}{b}+\frac{b^2}{c}+\frac{c^2}{a} \geq a+b+c
:::
Petunjuk: Tinjau bentuk $\frac{a^2}{b}+b\geq 2a$ yang diturunkan dari $(a-b)^2\geq 0$
::::

:::{exercise}
:label: exe-1.3
Diberikan bilangan real $x$ dan $y$. Jabarkan dna gunakan sifat kuadrat non-negatif untuk membuktikan bahwa $2x^2+2y^2\geq (x+y)^2$
:::

### Nilai Ekstrim dan Sifat Definit Fungsi Kuadrat

Sebagai konsekuensi lanjutan dari sifat kuadrat bilangan real yang tak negatif, kita dapat menganalisis nilai ekstrim (maksimum atau minimum) dari sebuah fungsi kuadrat. Konsep ini sangat berguna ketika kita diminta mencari batas bawah atau batas atas dari sebuah ekspresi aljabar di dalam soal ketaksamaan.

Mari kita tinjau fungsi kuadrat umum $f(x)=ax^2+bx+c$. Dengan teknik melengkapkan kuadrat sempurna, fungsi tersebut selalu dapat diubah menjadi bentuk 
$$ 
f(x) = a\left(x+\frac{b}{2a}\right)^2 - \frac{D}{4a}
$$
di mana $D=b^2-4ac$ adalah diskriminan.

Karena kita tahu bahwa bentuk kuadrat $\left(x+\frac{b}{2a}\right)^2$ nilai selalu lebih besar atau sama dengan nol, kita bisa menyimpulkan teorema berikut.

:::{prf:theorem}
Misalkan $a, b, c, x \in \mathbb{R}, a\neq 0, D=b^2-4ac$, dan $f(x)=ax^2+bx+c$
1. (Nilai maksimum)  Jika $a>0$, maka $f(x)\geq -\frac{D}{4a}$
2. (Nilai minimum) Jika $a<0$, maka $f(x)\leq -\frac{D}{4a}$ 

Kesamaan terjadi (fungsi mencapai nilai maksimum/minimum tersebut) jika dan hanya jika bagian kuadratnya bernilai nol, yaitu saat $x=-\frac{b}{2a}$
:::

Dari pemahaman tentang nilai minimum dan maksimum di atas, kita juga bisa mendeduksikan sebuah fakta penting lainnya tentang kondisi di mana fungsi kuadrat tidak pernah menyentuh atau memotong sumbu-$x$ sama sekali. Kondisi ini melahirkan teorema definit:

:::{prf:theorem}
Misalkan $a, b, c, x \in \mathbb{R}, a\neq 0, D=b^2-4ac$ dan $f(x)=ax^2+bx+c$.
1. (Definit Positif) $f(x)>0$ untuk setiap $x\in \mathbb{R}$ jika dan hanya jika $a>0$ dan $D<0$
2. (Definit Negatif) $f(x)<0$ untuk setiap $x\in \mathbb{R}$ jika dan hanya jika $a<0$ dan $D<0$
:::

:::::{prf:example}
:label: contoh-1.3
Tentukan syarat batas nilai $m$ agar fungsi kuadrat $f(x)=x^2-mx+9$ bernilai definit positif untuk semua $x\in \mathbb{R}$
::::{solution} contoh-1.3
:class: dropdown
Suatu fungsi kuadrat $f(x) = ax^2 + bx + c$ dikatakan \textbf{definit positif} (selalu bernilai positif atau berada di atas sumbu-$x$ untuk setiap nilai $x \in \mathbb{R}$) jika memenuhi dua syarat utama, yaitu:
1. Parabola terbuka ke atas, yang berarti nilai koefisien $a > 0$
2. Parabola tidak memotong sumbu-$x$, yang berarti nilai diskriminan $D < 0$.

Dari fungsi $f(x) = x^2 - mx + 9$, kita peroleh informasi nilai koefisien sebagai berikut:
:::{math}
a = 1, \quad b = -m, \quad \text{dan} \quad c = 9
:::
Mari kita periksa kedua syarat tersebut:
* Syarat 1 ($a > 0$):\
Karena $a = 1$, maka syarat $1 > 0$ sudah terpenuhi secara mutlak. Artinya, kurva fungsi ini dipastikan terbuka ke atas.
* Syarat 2 ($D < 0$):\
Kita substitusikan nilai $a, b,$ dan $c$ ke dalam rumus diskriminan $D = b^2 - 4ac$:
:::{math}
b^2 - 4ac &< 0 \\
(-m)^2 - 4(1)(9) &< 0 \\
m^2 - 36 &< 0
:::
Untuk menyelesaikan pertidaksamaan kuadrat di atas, langkah pertama adalah memfaktorkan bentuk aljabarnya untuk mencari nilai pembuat nol:
:::{math}
(m - 6)(m + 6) < 0
:::

Dari pemfaktoran tersebut, diperoleh akar-akar pembuat nol, yaitu $m = 6$ dan $m = -6$. Selanjutnya, kita tentukan tanda pada interval garis bilangan. Jika kita mengambil titik uji di antara $-6$ dan $6$ (misalnya $m = 0$) dan mensubstitusikannya ke $m^2 - 36$, hasilnya adalah $0^2 - 36 = -36$ (bernilai negatif). 

Karena pertidaksamaan yang diminta adalah kurang dari nol ($< 0$), maka daerah penyelesaiannya adalah daerah yang bernilai negatif, yaitu interval yang berada di antara kedua titik pembuat nol tersebut.

Jadi, batas nilai $m$ agar fungsi kuadrat $f(x) = x^2 - mx + 9$ bernilai definit positif adalah:
:::{math}
-6 < m < 6
:::
::::
:::::

:::{exercise}
:label: exe-1.4
Buktikan bahwa ekspresi $x^2-6x+10$ tidak pernah bernilai negatif untuk sembarang bilangan real $x$.
:::

:::{exercise}
:laebl: exe-1.5
Tentukan batas nilai $k$ sehingga grafik fungsi $y=-x^2+4x-k$ selalu berada di abwah sumbu-$x$ (definiti negatif).
:::

### Pengantar Membuktikan Ketaksamaan
Sebelum kita mempelajari berbagai teorema ketaksamaan tingkat lanjut seperti Rataan, Cauchy-Schwarz, dan lain-lain, kita perlu menyamakan sudut pandang tentang apa yang dimaksud dengan soal ketaksamaan pada OSN Matematika.

Di Sekolah, anda mungkin terbiasa dengan soal "mencari himpunan penyelesaian", misalnya: \textit{Tentukan nilai $x$ yang memenuhi $x^2 - 5x+6 <0$}. Jawaban dari soal ini adalah sebuah interval nilai $x$.

Namun, di dalam olimpiade matematika, perintah yang paling sering muncul adalah "\textbf{Buktikan bahwa ...}". Anda tidak diminta mencari rentang nilai variabel, melainkan diminta membuktikan bahwa sebuah ekspresi aljabar \textit{selalu} lebih besar atau lebih kecil dari ekspresi lainnya, untuk sembarang nilai variabel yang diberikan pada soal.

Dalam membuktikan ketaksamaan, ada dua hal penting yang harus selalu dievaluasi:

1. **Arah Ketaksamaan**: Apakah kita harus membuktikan ruas kiri lebih besar dari ruas kanan, atau sebaliknya? kita dapat menggunakan manipulasi aljabar, memfaktorkan, atau menggunakan teorema-teorema yang sudah terbukti benar.
2. **Kondisi Kesamaan**: Pada ketaksamaan yang memuat $\geq$ atau $\leq$, sangat penting untuk selalu menyebutkan kapan ruas kiri benar-benar bernilai \textit{sama dengan} ruas kanan. Kondisi ini sering kali menjadi  kunci untuk memecahkan soal tingkat lanjut.

## Ketaksamaan Rataan (QM-AM-GM-HM)

Di sekolah, saat kita mendengar kata "rata-rata", yang terlintas di pikiran kita adalah menjumlahkan semua data lalu membaginya dengan banyaknya data. Dalam matematika tingkat lanjut, rata-rata jenis ini hanyalah satu dari beberapa jenis rataan yang ada.

Dalam olimpiade matematika, kita mengenal empat jenis rataan utama. Untuk setiap $n$ buah bilangan real positif $a_1, a_2, a_3, \cdots, a_n$, kita mendefinisikan empat rataan berikut:

1. **Rataan Aritmatika (AM - *Arithmetic Mean*)**\
   Ini adalah rata-rata yang biasa kita kenal di sekolah
    \begin{equation}
        AM = \frac{a_1 + a_2 + a_3 +\cdots + a_n}{n}
    \end{equation}
2. **Rataan Geometri (GM - *Geometric Mean*)**\
   Rataan ini diperoleh dengan mengalikan semua bilangan, lalu diakar pangkat $n$
    \begin{equation}
        GM = \sqrt[n]{a_1 \times a_2 \times a_3 \times \cdots \times a_n}
    \end{equation}
3. **Rataan Harmonik (HM - *Harmonic Mean*)**\
   Rataan ini adalah kebalikan dari rataan aritmatika dari kebalikan bilangan-bilangannya.
    \begin{equation}
        HM = \frac{n}{\frac{1}{a_1}+\frac{1}{a_2}+\frac{1}{a_3}+\cdots +\frac{1}{a_n}}
    \end{equation}
4. **Rataan Kuadratik (QM - *Quadratic Mean*)**\
   Sering juga disebut \textit{Root Mean Square (RMS)}. Rataan ini sangat berguna jika kita berhadapan dengan bentuk kuadrat.
    \begin{equation}
        QM = \sqrt{\frac{a_1^2 + a_2^2 + a_3^2 + \cdots + a_n^2}{n}}
    \end{equation}

:::{prf:theorem}
Jika $QM, AM, GM$, dan $HM$ berturut-turut menyatakan rataan kuadrat, rataan aritmatika, rataan geometri, dan rataan harmonik dari bilangan real positif $a_1, a_2, a_3, \cdots, a_n$, maka 
\begin{equation}
    QM \geq AM \geq GM \geq HM
\end{equation}
Selanjutnya, kesamaan terjadi jika dan hanya jika $a_1 = a_2 = a_3 =\cdots = a_n$
:::

Untuk setiap bilangan real positif $a$ dan $b$, kita akan membuktikan rantai ketaksamaan $QM \geq AM \geq GM \geq HM$. Mari kita pecah pembuktiannya menjadi tiga bagian yang lebih sederhana.

1. Pembuktian $AM \geq GM$
   :::{prf:proof}
   Karena $a$ dan $b$ adalah bilangan positif, maka $\sqrt{a}$ dan $\sqrt{b}$ adalah bilangan real yang terdefinisi. Kuadrat dari sebuah bilangan real selalu tak negatif.
   $$ 
   (\sqrt{a}-\sqrt{b})\geq 0
   $$
   Jabarkan bentuk kuadrat di ruas kiri
   $$ 
   (\sqrt{a})^2-2\sqrt{a}\sqrt{b}+(\sqrt{b})^2\geq 0\\
   a-2\sqrt{ab}+b\geq 0
   $$
   Tambahkan $-2\sqrt{ab}$ pada kedua ruas
   $$ 
   a+b\geq 2\sqrt{ab}
   $$
   Bagi kedua ruas dengan 2
   $$ 
   \frac{a+b}{2}\geq \sqrt{ab}
   $$
   Kesamaan terjadi jika dan hanya jika $(\sqrt{a}-\sqrt{b})^2 \implies \sqrt{a}=\sqrt{b} \implies a=b$
   :::
2. Pembuktian $QM \geq AM$
   :::{prf:proof}
   Kedua ruas bernilai positif, kita diperbolehkan mengkuadratkan kedua ruas tanpa mengubah arah ketaksamaan
    :::{math}
        \sqrt{\frac{a^2+b^2}{2}}^2 \geq \left(\frac{a+b}{2}\right)^2\\
        \frac{a^2+b^2}{2} \geq \frac{a^2+2ab+b^2}{4}
    :::
    Kalikan kedua ruas dengan 4 untuk menghilangkan pecahan
    :::{math}
        2(a^2+b^2) \geq a^2+2ab+b^2\\
        2a^2+2b^2 \geq a^2+2ab+b^2
    :::
    Kurangkan kedua ruas dengan $a^2+2ab+b^2$
    :::{math}
        2a^2+2b^2 - (a^2+2ab+b^2) \geq 0\\
        (2a^2-a^2) + (2b^2-b^2) - 2ab \geq 0\\
        a^2 + b^2 - 2ab \geq 0\\
        (a-b)^2 \geq 0
    :::
    Karena kuadrat bilangan real selalu lebih besar atau sama dengan nol, maka baris terakhir ini bernilai benar. Karena langkah-langkah kita bisa dibalik, maka ketaksamaan awal juga terbukti benar.\
    Kesamaan terjadi jika dan hanya jika $(a-b)^2=0 \implies a=b$
   :::
3. Pembuktian $GM \geq HM$
   :::{prf:proof}
   Pertama kita sederhanakan bentuk $HM$ di ruas kanan
    :::{math}
        HM = \frac{2}{\frac{1}{a}+\frac{1}{b}}=\frac{2}{\frac{b+a}{ab}}=\frac{2ab}{a+b}
    :::
    Sehingga, ketaksamaan yang ingin kita buktikan menjadi
    :::{math}
        \sqrt{ab}\geq \frac{2ab}{a+b}
    :::
    Karena $a, b\geq 0$, maka $\sqrt{ab}\geq 0$. Kita bisa membagi kedua ruas dengan $\sqrt{ab}$
    :::{math}
        1\geq \frac{\frac{2ab}{a+b}}{\sqrt{ab}}\\
        1\geq \frac{\frac{2ab}{a+b}}{\sqrt{ab}}\cdot \frac{\sqrt{ab}}{\sqrt{ab}}\\
        1 \geq \frac{2\sqrt{ab}}{a+b}
    :::
    Kalikan kedua ruas dengan $(a+b)$ yang bernilai positif
    :::{math}
        a+b \geq 2\sqrt{ab}
    :::
    Bagi kedua ruas dengan 2
    :::{math}
        \frac{a+b}{2}\geq\sqrt{ab}
    :::
    Perhatikan bahwa baris terakhir ini tidak lain adalah ketaksamaan $AM\geq GM$ yang sudah kita buktikan kebenarannya. Oleh karena itu, $GM \geq HM$ juga terbukti benar.\
    Kesamaan terjadi jika dan hanya jika $a=b$.
   :::

Dari ketiga bukti di atas, kita secara sah dapat menggabungkannya menjadi satu rantai ketaksamaan yang solid untuk dua variabel
:::{math}
    \sqrt{\frac{a^2+b^2}{2}}\geq \frac{a+b}{2}\geq \sqrt{ab}\geq \frac{2}{\frac{1}{a}+\frac{1}{b}}
:::
atau 
:::{math}
    QM \geq AM \geq GM \geq GM
:::

:::{note}
Untuk pembuktian $n$ variabel yang lebih banyak, matematikawan hebat Augustin-Louis Cauchy menggunakan sebuah metode brilian yang disebut Induksi Maju-Mundur atau Cauchy's Forward-Backward Induction. Namun, untuk aplikasi praktis menyelesaikan soal OSN, menguasai bukti dan aplikasi untuk 2 atau 3 variabel biasanya sudah sangat memadai.
:::

:::::{prf:example}
:label: contoh-1.4
Gunakan ketaksamaan GM-HM untuk menentukan batas nilai dari $\frac{1}{x}+\frac{1}{y}$ jika diketahui $x,y>0$ dan $xy=25$.
::::{solution} contoh-1.4
:class: dropdown
ini bagian solusi
::::
:::::

:::::{prf:example} 
:label: contoh-1.5
Diberikan $a, b, c, d>0$. Buktikan bahwa $(a+b)(c+d)\geq 4\sqrt{abcd}$
::::{solution} contoh-1.5
:class: dropdown
ini bagian solusi
::::
:::::

:::::{prf:example} 
:label: contoh-1.6
Tentukan nilai minimum dari fungsi objektif $\frac{x}{y}+\frac{y}{z}+\frac{z}{x}$ untuk setiap bilangan real positif $x, y$, dan $z$.
::::{solution} contoh-1.6
:class: dropdown
ini bagian solusi
::::
:::::

:::::{prf:example} 
:label: contoh-1.7
Diberikan $a, b, c>0$. Buktikan bahwa $(a+b+c)(a^2+b^2+c^2)\geq 9abc$
::::{solution} contoh-1.7
:class: dropdown
ini bagian solusi
::::
:::::

:::::{prf:example} 
:label: contoh-1.8
Buktikan Ketaksamaan Nesbitt berikut untuk setiap bilangan real positif $a, b, c$
:::{math}
\frac{a}{b+c}+\frac{b}{c+a}+\frac{c}{a+b}\geq \frac{3}{2}
:::
::::{solution} contoh-1.8
:class: dropdown
ini bagian solusi
::::
:::::

::::{exercise}
:label: exe-1.6
Diketahui $a, b, c>0$ dan $abc=8$. Tentukan nilai minimum dari ekspresi $a+b+c$
::::

:::{exercise}
:label: exe-1.7
Diketahui $a>0$. Tentukan nilai minimum dari ekspresi $3a+\frac{12}{a}$.
:::

:::{exercise}
:label: exe-1.8
Diketahui $a, b, c$ adalah bilangan real positif yang memenuhi $a+b+c=1$. Dengan menggunakan ketaksamaan $AM-HM$, tentukan nilai minimum dari $\frac{1}{a}+\frac{1}{b}+\frac{1}{c}$.
:::

:::{exercise}
:label: exe-1.9
Diketahui bilangan real positif $x$ dan $y$ yang memenuhi $x^3+y^3=2$. Buktikan bahwa $x+y\leq 2$
:::

:::{exercise}
:label: exe-1.10
lorem ipsum
:::


## Ketaksamaan Cauchy-Schwarz
Setelah mengkaji rantai ketaksamaan rataan, kita melangkah ke salah satu teorema pembuktian paling kuat, fundamental, dan universal dalam aljabar: Ketaksamaan Cauchy-Schwarz. Teorema ini sangat esensial karena aplikasinya tidak hanya mendominasi soal-soal olimpiade aljabar tingkat lanjut, tetapi juga menjadi basis bagi geometri analitik dan aljabar linier.

Secara formal, ketaksamaan ini menyatakan batasan hasil kali dari dua barisan bilangan real.

::::{prf:theorem} Ketaksamaan Cauchy-Schwarz
Misalkan $a_1, a_2, a_3, \cdots, a_n$ dan $b_1, b_2, b_3, \cdots, b_n$ adalah dua barisan bilangan real sembarang. Maka selalu berlaku hubungan 
:::{math}
(a_1^2+a_2^2+a_3^2\cdots +a_n^2)(b_1^2+b_2^2+b_3^2+\cdots +b_n^2) \geq (a_1b_1 + a_2b_2 + a_3b_3 + \cdots + a_nb_n)^2
:::
Atau sering dituliskan dalam notasi sigma
:::{math}
\left(\sum_{i=1}^{n}a_i^2\right)\left(\sum_{i=1}^{n}b_i^2\right) \geq \left(\sum_{i=1}^{n}a_ib_i\right)^2
:::
Kesamaan terjadi jika dan hanya kedua barisan tersebut sebanding. Artinya, terdapat suatu konstanta real $k$ sedemikian sehingga $a_i=k\cdot b_i$ untuk setiap $i=1, 2, 3, \cdots, n$
::::

Terdapat beberapa cara untuk membuktikan Ketaksamaan Cauchy-Schwarz. Namun, salah satu pembuktian paling elegan dan logis bersumber langsung dari Sifat Definit Fungsi Kuadrat yang telah dibahas pada subbab sebelumnya.

::::{prf:proof}
:class: dropdown
Bentuklah sebuah fungsi kuadrat baru $f(x)$ dalam variabel real $x$, yang dikonstruksikan dari jumlah kuadrat binomial berikut.
:::{math}
    f(x)=(a_1x-b_1)^2+(a_2x-b_2)^2+\cdots + (a_nx-b_n)^2
:::
Karena fungsi $f(x)$ merupakan penjumlahan dari bentuk-bentuk kuadrat, maka berdasarkan sifat fundamental bilangan real, nilai $f(x)$ tidak mungkin bernilai negatif. Dengan kata lain
:::{math}
    f(x)\geq 0 \text{ untuk setiap } x \in \mathbb{R}
:::
Mari kita jabarkan setiap suku pada fungsi $f(x)$ tersebut
:::{math}
    f(x)=(a_1^2x^2-2a_1b_1x+b_1^2)+(a_2^2x^2-2a_2b_2x+b_2^2)+\cdots + (a_n^2x^2-2a_nb_nx+b_n^2)
:::
Kelompokkan suku-suku tersebut berdasarkan derajat variabel $x$
:::{math}
    f(x)=(a_1^2+a_2^2+\cdots + a_n^2)x^2 - 2(a_1b_1 + a_2b_2 + \cdots +a_nb_n)x + (b_1^2+b_2^2+\cdots +b_n^2)
:::
Agar penulisan menjadi lebih ringkas dan memudahkan analisis, kita misalkan
:::{math}
    A &= a_1^2 + a_2^2 + \cdots + a_n^2\\
    B &= a_1b_1 + a_2b_2 + \cdots + a_nb_n\\
    C &= b_1^2 + b_2^2 + \cdots + b_n^2
:::
Sehingga fungsi kuadrat di atas dapat direduksi menjadi bentuk standar
:::{math}
    f(x) = Ax^2-2Bx + C
:::
Kita kembali merujuk pada konsep bahwa $f(x)\geq 0$ untuk setiap nilai $x$. Ini berarti grafik fungsi kuadrat tersebut selalu berada di atas atau menyinggung sumbu-$x$ (definit positif). Syarat mutlak agar suatu fungsi kuadrat $Ax^2 - 2Bx + C\geq 0$ terpenuhi adalah nilai diskriminannya $(D)$ harus lebih kecil atau sama dengan nol ($D\leq 0$).

Kita asumsikan $A>0$. Jika $A=0$, maka seluruh $a_i=0$, sehingga ketaksamaan menjadi $0\geq 0$ yang mana secara trivial benar.

Hitung nilai diskriminannya
:::{math}
    D&\leq 0\\
    (-2B)^2 - 4(A)(C)&\leq 0\\
    4B^2 - 4AC&\leq 0\\
    4B^2 &\leq 4AC\\
    B^2 &\leq AC
:::
Substitusi kembali persamaan $A, B, C$ ke bentuk terkahir
:::{math}
    (a_1^2+a_2^2+a_3^2\cdots +a_n^2)(b_1^2+b_2^2+b_3^2+\cdots +b_n^2) \geq (a_1b_1 + a_2b_2 + a_3b_3 + \cdots + a_nb_n)^2
:::
$\blacksquare$
::::

Pembuktian ini juga secara simultan menjelaskan mengapa kesamaan terjadi. Nilai ruas kiri sama dengan ruas kanan jika dan hanya jika diskriminan bernilai nol ($D=0$). Hal ini ekuivalen dengan fungsi $f(x)$ menyentuh sumbu-$x$ tepat di satu titik, yang berarti setiap suku kuadrat $(a_ix-b_i)^2=0$. Akibatnya $a_ix=b_i$ atau $x=\frac{b_i}{a_i}$ untuk setiap $i$. ini membuktikan bahwa barisan $a_i$ dan $b_i$ harus memiliki rasio kesebandingan yang konstan $x$.

Dalam menyelesaikan soal-soal OSN, sering kali kita berhadapan dengan ketaksamaan yang memuat bentuk pecahan (rasional). Terdapat sebuah turunan langsung dari Ketaksamaan Cauchy-Schwarz yang didesain khusus untuk melibas soal-soal pecahan dengan sangat cepat. Bentuk ini dikenal dengan nama Bentuk Engel atau Lemma Titu.

::::{prf:lemma} Titu
Untuk setiap barisan bilangan real $x_1, x_2, \cdots, x_n$ dan barisan bilangan real positif $y_1, y_2, \cdots, y_n$, berlaku
:::{math}
    \frac{x_1^2}{y_1}+\frac{x_2^2}{y_2}+\cdots +\frac{x_n^2}{y_n}\geq \frac{(x_1+x_2+\cdots+x_n)^2}{y_1+y_2+\cdots+y_n}
:::
Kesamaan terjadi jika dan hanya jika $\frac{x_1}{y_1}=\frac{x_2}{y_2}=\cdots=\frac{x_n}{y_n}$. 
::::

Pembuktian bentuk ini dapat dengan mudah dijabarkan menggunakan Cauchy-Schwarz standar dengan mensubstitusikan $a_i=\frac{x_i}{\sqrt{y_i}}$ dan $b_i=\sqrt{y_i}$.

::::{prf:proof}
:class: dropdown
Lema Titu ini merupakan akibat langsung (korolari) dari Ketaksamaan Cauchy-Schwarz. Ingat kembali bentuk umum Ketaksamaan Cauchy-Schwarz untuk dua barisan bilangan real $a_1, a_2, \dots, a_n$ dan $b_1, b_2, \dots, b_n$:
:::{math}
:label: eq-cs
(a_1^2 + a_2^2 + \dots + a_n^2)(b_1^2 + b_2^2 + \dots + b_n^2) \ge (a_1b_1 + a_2b_2 + \dots + a_nb_n)^2
:::
Berdasarkan hipotesis, diketahui $y_i$ adalah barisan bilangan real positif (sehingga $y_i > 0$). Hal ini memungkinkan kita untuk menarik akar kuadrat dan menjadikannya sebagai penyebut tanpa melanggar aturan aljabar. Kita definisikan nilai $a_i$ dan $b_i$ sebagai berikut:
:::{math}
a_i = \frac{x_i}{\sqrt{y_i}} \quad \text{dan} \quad b_i = \sqrt{y_i}
:::
untuk setiap $i = 1, 2, \dots, n$.

Selanjutnya, substitusikan pemisalan tersebut ke dalam bentuk Ketaksamaan Cauchy-Schwarz pada persamaan {eq}`eq-cs`
:::{math}
\left( \left(\frac{x_1}{\sqrt{y_1}}\right)^2 + \dots + \left(\frac{x_n}{\sqrt{y_n}}\right)^2 \right) \left( (\sqrt{y_1})^2 + \dots + (\sqrt{y_n})^2 \right) &\ge \left( \frac{x_1}{\sqrt{y_1}}\sqrt{y_1} + \dots + \frac{x_n}{\sqrt{y_n}}\sqrt{y_n} \right)^2 \\
\left( \frac{x_1^2}{y_1} + \frac{x_2^2}{y_2} + \dots + \frac{x_n^2}{y_n} \right) (y_1 + y_2 + \dots + y_n) &\ge (x_1 + x_2 + \dots + x_n)^2
:::
Karena $y_1, y_2, \dots, y_n$ semuanya bernilai positif, maka hasil penjumlahannya, yaitu $(y_1 + y_2 + \dots + y_n)$, juga dipastikan bernilai positif. Oleh karena itu, kita dapat membagi kedua ruas ketaksamaan dengan $(y_1 + y_2 + \dots + y_n)$ tanpa mengubah tanda ketaksamaan, sehingga diperoleh:
:::{math}
\frac{x_1^2}{y_1} + \frac{x_2^2}{y_2} + \dots + \frac{x_n^2}{y_n} \ge \frac{(x_1 + x_2 + \dots + x_n)^2}{y_1 + y_2 + \dots + y_n}
:::
Ketaksamaan Lema Titu terbukti.

Berdasarkan sifat Ketaksamaan Cauchy-Schwarz, kesamaan (ruas kiri sama dengan ruas kanan) terjadi jika dan hanya jika barisan $a_i$ dan $b_i$ sebanding. Artinya, rasio antara suku-suku yang bersesuaian adalah konstan:
:::{math}
\frac{a_1}{b_1} = \frac{a_2}{b_2} = \dots = \frac{a_n}{b_n}
:::
Dengan mensubstitusikan kembali pemisalan kita sebelumnya, kondisi kesamaan ini dapat dituliskan sebagai:
:::{math}
\frac{\frac{x_1}{\sqrt{y_1}}}{\sqrt{y_1}} &= \frac{\frac{x_2}{\sqrt{y_2}}}{\sqrt{y_2}} = \dots = \frac{\frac{x_n}{\sqrt{y_n}}}{\sqrt{y_n}}
:::
Dengan menyederhanakan bentuk pecahan bertumpuk di atas (mengalikan pembilang dan penyebut dengan $\sqrt{y_i}$), kita memperoleh syarat kesamaan akhir:
:::{math}
\frac{x_1}{y_1} = \frac{x_2}{y_2} = \dots = \frac{x_n}{y_n}
:::
Jadi, Lema Titu terbukti secara keseluruhan.
::::

:::::{prf:example}
:label: contoh-1.9
Jika $x, y, z$ adalah bilangan real dengan $x+y+z=12$, gunakan ketaksamaan Cauchy-Schwarz untuk mencari nilai minimum dari $x^2+y^2+z^2$.
::::{solution} contoh-1.9
:class: dropdown
ini bagian solusi
:::::

:::::{prf:example}
:label: contoh-1.10
Diberikan $x, y>0$ dan $x+y=5$. Tentukan nilai minimum dari $\frac{x^2}{2}+\frac{y^2}{3}$ menggunakan Lema Titu.
::::{solution} contoh-1.10
:class: dropdown
ini bagian solusi
:::::

:::::{prf:example}
:label: contoh-1.11
Gunakan Lema Titu untuk mencari nilai minimum dari $\frac{a^2}{x}+\frac{b^2}{y}+\frac{c^2}{z}$ apabila diketahui $x, y, z>0$ dan $x+y+z=1$, di mana $a, b, c$ adalah konstanta real positif.
::::{solution} contoh-1.11
:class: dropdown
ini bagian solusi
:::::

:::::{prf:example}
:label: contoh-1.12
Diberikan $x, y, z>0$ dan $x+y+z=1$. Buktikan bahwa
:::{math}
\frac{x}{1-x}+\frac{y}{1-y}+\frac{z}{1-z} \geq \frac{3}{2}
:::
::::{solution} contoh-1.12
:class: dropdown
ini bagian solusi
:::::

:::::{prf:example}
:label: contoh-1.13
Buktikan bahwa untuk setiap bilangan real positif $a, b, c$ dengan $a+b+c=1$, berlaku $\frac{a^2}{3a+1}+\frac{b^2}{3b+1}+\frac{c^2}{3c+1}\geq \frac{1}{6}$
::::{solution} contoh-1.13
:class: dropdown
ini bagian solusi
:::::

::::{exercise}
:label: exe-1.11
Tentukan nilai maksimum dari $2x-y+2z$ jika diketahui $x, y, z\in \mathbb{R}$ dan $x^2+y^2+z^2=9$.
::::

::::{exercise}
:label: exe-1.12
Diberikan persamaan $4a^2+9b^2=36$ dengan $a, b\in \mathbb{R}$. Tentukan nilai maksimum yang mungkin untuk $2a+3b$.
::::

::::{exercise}
:label: exe-1.13
Tentukan nilai minimum dari $\frac{2}{x}+\frac{9}{y}+\frac{8}{z}$ jika diketahui $x, y, z$ adalah bilangan real positif dan $x+y+z=1$.
::::

::::{exercise}
:label: exe-1.14
Diketahui $a, b, c, d$ adalah bilangan asli. Gunakan ketaksamaan Cauchy-Schwarz untuk membuktikan bahwa $\frac{1}{a}+\frac{1}{b}+\frac{1}{c}+\frac{1}{d}\geq \frac{16}{a+b+c+d}$
::::

::::{exercise}
:label: exe-1.15
Misalkan $a, b, c$ adalah bilangan real positif. Buktikan ketaksamaan berikut menggunakan Lemma Titu
:::{math}
\frac{a^2}{(a+b)(a+c)}+\frac{b^2}{(b+c)(b+a)}+\frac{c^2}{(c+a)(c+b)}\geq \frac{3}{4}
:::
::::

## Ketaksamaan Jensen
Dalam analisis matematis, Ketaksamaan Jensen memberikan batasan nilai fungsi konveks  atau konkaf terhadap kombinasi linier dari titik-titik pada domainnya. Sebelum merumuskan ketaksamaan ini, definisi fungsi konveks perlu dirumuskan secara formal.

::::{prf:definition}
Misalkan $I\subseteq \mathbb{R}$ adalah sebuah inteval. Sebuah fungsi $f:I\to \mathbb{R}$ dikatakan konveks pada inverval $I$ jika untuk untuk setiap $x_1, x_2 \in I$ dan untuk setiap bilangan real $t\in [0,1]$, berlaku ketaksamaan berikut
:::{math}
    f(tx_1+(t-1)x_2) \leq tf(x_1)+(1-t)f(x_2)
:::
Fungsi $f$ dikatakan konkaf pada $I$ jika ketaksamaan pada definisi di atas dibalik arahnya, yakni
:::{math}
    f(tx_1+(1-t)x_2) \geq tf(x_1)+(1-t)f(x_2)
:::
::::

Sebagai kriteria operasional analitik yang praktis untuk fungsi yang dapat diturunkan, kita dapat menggunakan uji turunan kedua.

:::{prf:theorem}
Misalkan $f$ adalah fungsi yang memiliki turunan kedua yang terdefinisi pada interval terbuka $I$.
1. Fungsi $f$ konveks pada $I$ jika dan hanya jika $f"(x)\geq 0$ untuk setiap $x\in I$
2. Fungsi $f$ konkaf pada $I$ jika dan hanya jika $f"(x)\leq 0$ untuk setiap $x\in I$
:::

Melalui pendefinisian di atas, kita dapat memperluas sifat konveksitas dari dua variabel ke dalam $n$ variabel menggunakan pembobot, yang melahirkan teorema Ketaksamaan Jensen.

::::{prf:theorem}
Misalkan $I$ adalah sebuah interval, dan $f:I\to \mathbb{R}$ adalah fungsi yang konveks pada $I$. Jika $x_1, x_2, \cdots, x_n$ adalah bilangan-bilangan di dalam interval $I$, dan $w_1, w_2, \cdots, w_n$ adalah bobot non-negatif sedemikian sehingga $\sum_{i=1}^{n} w_i=1$, maka berlaku
:::{math}
    f\left(\sum_{i=1}^{n}w_i x_i\right) \leq \sum_{i=1}^{n} w_i f(x_i)
:::
::::

:::{note}
Jika $f$ adalah fungsi konkaf, maka tanda $\leq$ pada ketaksamaan di atas berubah menjadi $\geq$
:::

Dalam konteks penyelesaian masalah aljabar, kasus yang paling umum ditemui adalah ketika semua variabel memiliki pembobot yang seragam, yaitu $w_i=\frac{1}{n}$ untuk setia $i=1, 2, \cdots, n$. Substitusi bobot ini menghasilkan bentuk Ketaksamaan Jensen Khusus Rataan.

1. Untuk Fungsi Konveks
   :::{math}
        f\left(\frac{x_1+x_2+\cdots +x_n}{n}\right) \leq \frac{f(x_1)+f(x_2)+\cdots +f(x_n)}{n}
    :::
2. Untuk Fungsi Konkaf
   :::{math}
        f\left(\frac{x_1+x_2+\cdots +x_n}{n}\right) \geq \frac{f(x_1)+f(x_2)+\cdots +f(x_n)}{n}
    :::

Kondisi kesamaan terjadi jika dan hanya jika $x_1 = x_2 = \cdots = x_n$, atau jika $f(x)$ merupakan fungsi linier pada interval pembicaraan.

:::::{prf:example}
:label: contoh-1.14
Dengan menggunakan uji turunan kedua, tentukan apakah fungsi $f(x)=x^4-2x^3+5x$ merupakan fungsi konveks atau konkaf pada interval $[2, \infty)$
::::{solution} contoh-1.14
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.15
Jika $x, y, z\in \mathbb{R}$, buktikan bahwa $x^2+y^2+z^2 \geq \frac{(x+y+z)^2}{3}$
::::{solution} contoh-1.15
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.16
Diberikan $a, b, c>0$ dan $a+b+c=3$. Tentukan nilai minimum dari $a^3+b^3+c^3$
::::{solution} contoh-1.16
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.17
Diberikan bilangan real positif $x_1, x_2, \cdots, x_n$ sedemikian sehingga $\sum_{i=1}^{n} x_i = 1$. Buktikan bahwa
:::{math}
\sum_{i=1}^{n} \frac{x_i}{2-x_i} \geq \frac{n}{2n-1}
:::
dengan mendefinisikan fungsi $f(t)=\frac{t}{2-t}$
::::{solution} contoh-1.17
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.18
Jika $x_1, x_2, x_3, x_4$ adalah bilangan positif sedemikian sehingga $x_1+x_2+x_3+x_4=1$, tentukan nilai maksimum dari $\sqrt{x_1}+\sqrt{x_2}+\sqrt{x_3}+\sqrt{x_4}$.
::::{solution} contoh-1.18
:class: dropdown
ini solusi
::::
:::::

::::{exercise}
:label: exe-1.16
Tentukan interval di mana fungsi $f(x)=x^3-6x^2+9x$ bersifat konkaf.
::::

::::{exercise}
:label: exe-1.17
Diberikan $a, b>0$. Buktikan bahwa $(a+b)^4 \leq 8(a^4+b^4).$
::::

::::{exercise}
:label: exe-1.18
Diberikan $x, y>0$. Gunakan ketaksamaan Jensen dengan pembobot $w_1=\frac{1}{3}$ dan $w_2=\frac{2}{3}$ pada fungsi konveks $f(t)=t^3$ untuk membuktikan $\frac{x^3+2y^3}{3} \geq \left(\frac{x+2y}{3}\right)^3$.
::::

::::{exercise}
:label: exe-1.19
Diberikan fungsi $f(x)=\sqrt{x^2+1}$. Tujukkan bahwa $f(x)$ konveks, lalu gunakan fakta tersebut untuk membuktikan bahwa
:::{math}
\sqrt{a^2+1}+\sqrt{b^1+1} \geq 2\sqrt{\left(\frac{a+b}{2}\right)^2+1}
:::
::::

::::{exercise}
:label: exe-1.20
(Ketaksamaan Young) Diberikan bilangan real $p, q>1$ sedemikian sehingga $\frac{1}{p}+\frac{1}{q}=1$. Gunakan konveksitas dari fungsi eksponensial $f(x)=e^x$ dan ketaksamaan Jensen berbobot untuk membuktikan bahwa untuk setiap $a, b>0$ berlaku $ab\leq \frac{a^p}{p}+\frac{b^q}{q}$
::::

## Ketaksamaan Rearrangment
Dalam eksplorasi optimasi aljabar, Ketaksamaan Rearrangement memberikan landasan yang kuat mengenai bagaimana mengatur pasangan perkalian dari dua himpunan bilangan agar menghasilkan nilai total yang maksimum atau minimum. Secara intuitif, jumlah perkalian maksimum dicapai ketika bilangan terbesar dipasangkan dengan bilangan terbesar lainnya, sedangkan jumlah minimum dicapai saat bilangan terbesar dipasangkan dengan bilangan terkecil.

::::{prf:definition}
Misalkan terdapat dua barisan bilangan real berukuran $n$ yang masing-masing telah diurutkan secara monoton naik (tidak turun)
:::{math}
    a_1\leq a_2\leq \cdots \leq a_n\\
    b_1\leq b_2\leq \cdots \leq b_n
:::
Misalkan pula $c_1, c_2, \cdots, c_n$ adalah sembarang permutasi dari elemen-elemen pada barisan $b_1, b_2, \cdots, b_n$.
::::

::::{prf:theorem}
Berdasarkan barisan yang telah didefinisikan di atas, hasil kali berpasangan antara barisan $a$ dan permutasi $c$ akan selalu memenuhi rantai ketaksamaan berikut
:::{math}
    a_1b_n + a_2b_{n-1}+\cdots +a_nb_1 \leq a_1c_1 + a_2c_2 +\cdots +a_nc_n \leq a_1b_1+a_2b_2+\cdots+a_nb_n
:::
Dalam notasi sigma, teorema ini secara ekuivalen dapat dituliskan sebagai
:::{math}
    \sum_{i=1}^{n} a_ib_{n-i+1} \leq \sum_{i=1}^{n} a_ic_i \leq \sum_{i=1}^{n}a_ib_i
:::
::::

Konsekuensi analitik dari teorema ini dapat dijabarkan ke dalam tiga prinsip utama pengelompokan batas

1. Batas Atas (Maksimum): Penjumlahan hasil kali akan mencapai nilai maksimum jika kedua barisan dipasangkan secara searah (elemen terkecil dikalikan dengan elemen terkecil, dan elemen terbesar dikalikan dengan elemen terbesar).
2. Batas Bawah (Minimum): Penjumlahan hasil kali akan mencapai nilai minimum jika kedua barisan dipasangkan secara berlawanan arah (elemen terkecil dikalikan dengan elemen terbesar dan sebalikanya berlanjut hingga ke tengah barisan).
3. Susunan Acak: Kombinasi perkalian dengan susunan permutasi sembarang akan selalu menghasilkan nilai di antara batas bawah dan batas atas tersebut.

:::::{prf:example}
:label: contoh-1.19
Diberikan dua himpunan bilangan $A=\{2, 4, 7\}$ dan $B=\{1, 3, 5\}$. Jika elemen-elemen $A$ dan $B$ dipasangkan satu per satu lalu dikalikan, tentukan jumlah hasil kali maksimum yang mungkin diperoleh.
::::{solution} contoh-1.19
:class: dropdown
::::
:::::

:::::{prf:example}
:label: contoh-1.20
Diberikan barisan $\{1, 2, 3, 4\}$ dan $\{1, 4, 9, 16\}$. Tentuka nilai terkecil dari penjumlahan $a_1b_1 + a_2b_2 + a_3b_3 + a_4b_4$ jika $a_i$ dan $b_i$ diambil dari masing-masing himpunan.
::::{solution} contoh-1.20
:class: dropdown
::::
:::::

:::::{prf:example}
:label: contoh-1.21
Diberikan $x, y>0$. Buktikan bahwa $\frac{x^2}{y^2} + \frac{y^2}{x^2}\geq \frac{x}{y}+\frac{y}{x}$.
::::{solution} contoh-1.21
:class: dropdown
::::
:::::

:::::{prf:example}
:label: contoh-1.22
Diberikan bilangan real $x\in (0, \frac{\pi}{2})$. Tentukan batas bawah (nilai minimum) dari ekspresi $\frac{\sin^3 x}{\cos x}+\frac{\cos^3 x}{\sin x}$.
::::{solution} contoh-1.22
:class: dropdown
::::
:::::

:::::{prf:example}
:label: contoh-1.23
Misalkan $a, b, c$ adalah bilangan real positif. Tinjau semua kemungkinan semua kemungkinan permutasi derejat pangkat. Buktikan secara ketat bahwa
:::{math}
a^5 b^2 c+b^5 c^ 2 a+ c^5 a^2 b \leq a^8 + b^8 + c^8
:::
::::{solution} contoh-1.23
:class: dropdown
::::
:::::

::::{exercise}
:label: exe-1.21
Diberikan dua himpunan bilangan $A=\{2, 4, 7\}$ dan $B=\{1, 3, 5\}$. Jika elemene-elemen $A$ dan $B$ dipasangkan satu per satu lalu dikalikan, tentukan jumlah hasil kali minimum yang mungkin diperoleh.
::::

::::{exercise}
:label: exe-1.22
Buktikan bahwa untuk setiap bilangan real positif $x, y, z$, berlaku $x^4+y^4+z^4 \geq x^3y + y^3z + z^3x$.
::::

::::{exercise}
:label: exe-1.23
Diberikan bilangan real positif $a, b, c$. Buktikan bahwa $a^2b^2+b^2c^2+c^2a^2 \geq abc(a+b+c)$. 
::::

::::{exercise}
:label: exe-1.24
Diberikan bilangan real positif $a, b, c$. Buktikan ketaksamaan
:::{math}
\frac{a^3}{b^2} + \frac{b^3}{c^2} + \frac{c^3}{a^2} \geq \frac{a^2}{b} + \frac{b^2}{c} + \frac{c^2}{a}
:::
::::

::::{exercise}
:label: exe-1.25
Diberikan bilangan real positif $a, b, c$. Gunakan ketaksamaan Rearrangement untuk memberikan bukti alternatif dari ketaksamaan berikut
:::{math}
\frac{a^3}{a^2+ab+b^2} + \frac{b^3}{b^2+bc+c^2} + \frac{c^3}{c^2+ca+a^2} \geq \frac{a+b+c}{3}
:::
::::

## Identitas Dasar dan Teknik Substitusi Aljabar dalam Ketaksamaan

Dalam memecahkan masalah ketaksamaan tingkat olimpiade, sebuah ekspresi aljabar sering kali tampak terlalu kompleks atau terikat pada kondisi tertentu yang menghalanig aplikasi langsung dari teorema ketaksamaan. Manipulasi aljabar melalui pemfaktoran identitas khusus dan teknik substitusi variabel menjadi instrumen esensial untuk mentransformasikan ketaksamaan bersyarat menjadi ketaksamaan tak bersyarat, atau mereduksi derajat kerumitan sebuah polinomial.

### Identitas Aljabar Fundamental

Penguasaan terhadap pemfaktoran identitas mutlak diperlukan untuk membongkar struktur aljabar pada soal. Berikut adalah daftar identitas esensial yang wajib dikuasai.

1. Identitas Euler (Pemfaktoran Tiga Variabel)\
   Identitas ini merupakan salah satu alat paling kuat dalam aljabar untuk menghubungkan jumlahan pangkat tiga dengan perkalian tiga variabel
    :::{math}
        a^3+b^3+c^3-3abc=(a+b+c)(a^2+b^2+c^2-ab-bc-ca)
    :::
    Ekspresi pada faktor kedua dapat diekspansi menjadi jumlahan kuadrat sempurna, sehingga menghasilkan bentuk ekuivalen yang secara ketat menunjukkan sifat tak negatifnya
    :::{math}
        a^3+b^3+c^3-3abc=\frac{1}{2}(a+b+c)((a-b)^2+(b-c)^2+(c-a)^2)
    :::

    :::{prf:corollary}
    Jika $a, b, c$ adalah bilangan real positif, maka secara otomatis berlaku ketaksamaan $a^3+b^3+c^3\geq 3abc$, yang mana merupakan bentuk $AM-GM$ untuk tiga variabel
    :::
2. Identitas Lagrange\
   Identitas ini adalah basis struktural dari Ketaksamaan Cauchy-Schwarz. Identitas Lagrange mendefinisikan secara presisi selisih antara ruas kiri dan ruas kanan pada Cauchy-Schwarz sebagai jumlahan kuadrat
    :::{math}
        \left(\sum_{i=1}^{n}a_i^2\right)\left(\sum_{i=1}^{n}b_i^2\right) - \left(\sum_{i=1}^{n}a_i b_i\right)^2 = \sum_{1\leq i<j\leq n} (a_i b_j - a_j b_i)^2
    :::
    Karena ruas kanan adalah jumlah kuadrat (yang selalu lebih besar atau sama dengan nol), identitas ini secara langsung membuktikan ketaksamaan Cauchy-Schwarz, serta menunjukkan bahwa kesamaan terjadi jika dan hanya jika $a_ib_j=a_jb_i$ untuk setiap pasangan $i$ dan $j$.
3. Identitas Brahmagupta-Fibonacci\
   Sering digunakan dalam teori bilangan dan ketaksamaan bentuk kuadrat, identitas ini menunjukkan bahwa hasil kali dua jumlahan kuadrat juga dapat dinyatakan sebagai jumlahan kudrat
    :::{math}
        (a^2+b^2)(c^2+d^2)=(ac+bd)^2+(ad-bc)^2=(ac-bd)^2+(ad+bc)^2
    :::
4. Identitas Sophie Germain\
   Idenititas ini digunakan untuk memfaktorkan bentuk polinomial berderajat empat yang sekilas tidak memiliki faktor rill. Sangat bermanfaat untuk proses eliminasi suku dalam deret teleskopik atau pecahan aljabar.
    :::{math}
        a^4+4b^2=(a62+2ab+2b^2)(a^2-2ab+2b^2)
    :::
5. Faktorisasi Pangkat $n$ (Bentuk Selisih dan Jumlah)\
   Manipulasi batas bawah atau atas sering kali memerlukan pemfaktoran selisih pangkat berderajat $n$.
    :::{math}
        a^n-b^n = (a-b)(a^{n-1}+a^{n-2}b+a^{n-3}b^2+\cdots+ab^{n-2}+b^{n-1})
    :::
    Untuk bilangan asli $n$ ganjil, berlaku juga pemfaktoran untuk jumlahan
    :::{math}
        a^n+b^n = (a+b)(a^{n-1}-a^{n-2}b+a^{n-3}b^2-\cdots-ab^{n-2}+b^{n-1})
    :::

### Teknik Substitusi
Substitusi aljabar merupakan metode penggantian parameter yang dirancang untuk meleburkan batasa syarat yang diberikan pada soal ke dalam variabel baru, sehingga variabel tersebut menjadi bebas tanpa syarat.

1. Substitusi Simetris Dasar\
   Jika ketaksamaan melibatkan tiga variabel $a, b, c$ yang berifat simetri (struktunya tidak berubah jika variabelnya ditukar letaknya), pendefinisian variabel baru yang merepresentasikan akar-akar polinomial sering kali menyederhanakan perhitungan
    :::{math}
        p=a+b+c\\
        q=ab+bc+ca\\
        r=abc
    :::
    Penerapan substitusi ini mampu mentransformasikan polinomial simteri tingkat tinggi ke dalam sistem variabel bebasnya
    :::{math}
        a^2+b^2+c^2 = p^2-2q\\
        a^3+b^3+c^3=p^3-3pq+3r\\
        a^2b^2+b^2c^2+c^2a^2 = q^2-2pr
    :::
2. Substitusi Ravi\
   Persoalan aljabar sering kali menyertakan syarat "$a, b, c$ adalah panjang sisi-sisi dari sebuah segitiga". Berdasarkan ketaksamaan segitiga, harus berlaku mutlak bahwa jumlah dua sisi selalu lebih panjang dari sisi ketiga ($a+b>c, b+c>a, c+a>b$). Untuk mentransformasikan batasan geometri ini ke dalam wilayah aljabar murni yang tak bersyarat, kita melakukan substitusi Ravi menggunakan tiga bilangan real positif sembarang $x, y$ dan $z$
    :::{math}
        a=x+y\\
        b=y+z\\
        c=z+x
    :::
    Dengan pemisalan ini, ketiga syarat segitiga terpenuhi secara absolut, dan variabel $x, y, z>0$ dapat dioperasikan secara bebas.
3. Substitusi Kondisional Multiplikatif\
   Apabila soal memberikan batasan perkalian konstan, contohnya $abc=1$ dengan $a, b, c>0$, maka variabel tersebut dapat direpresentasikan sebagai pecahan siklis yang saling menghilangkan dari sekumpulan bilangan positif baru $x, y, z>0$
    :::{math}
        a=\frac{x}{y}, \text{   } b=\frac{y}{z}, \text{   } c=\frac{z}{x}
    :::
    Bentuk struktural substitusi ini didesain agar sangat kompatibel dengan Lemma Titu atau dalam menyamakan penyebut pada ketaksamaan aljabar.
4. Substitusi Trigonometri Lanjutan\
   Berbagai bentuk konstrain aljabar memiliki kesepadanan (ekuivalensi) identik dengan sifat-sifat identitas trigonometri. Pemetaan ke dalam ruang trigonometri mampu membatasi domain fungsi tanpa mengurangi keumuman (umumnya pada interval sudut segitiga $0<\theta<\pi$)
   * Syarat $ab+bc+ca=1$: Ekuivalen dengan relasi tangen setengah sudut segitiga. Substitusinya adalah $a=\tan\left(\frac{A}{2}\right), b=\tan\left(\frac{B}{2}\right), c=\tan\left(\frac{C}{2}\right)$, di mana $A+B+C=\pi$
    * Syarat $a+b+c=abc$: Ekuivalen dengan tangen sudut internal segitiga tak-siku. Substitusinya adalah $a=\tan A, b=\tan B, c=\tan C$
    * Syarat $x^2+y^2=1$: Merupakan persamaan lingkaran satuan. Kita dapat mensubstitusikannya secara langsung dengan $x=\cos \theta$ dan $y=\sin \theta$
    * Syarat $a^2+b^2+c^2+2abc=1$ (dengan $a, b, c>0$): Sangat sering muncul pada soal $OSN$ tingkat lanjut. Substitusi analitik yang tepat adalah $a=\cos A, b=\cos B, c=\cos C$, di mana $A, B, C$ adalah sudut-sudut lancip dari suatu segitiga.
5. Teknik Homogenisasi\
   Fungsi polinomial dikatakan homogen berderajat $k$ apabila total pangkat pada setiap sukunya bernilai sama. Jika sebuah ketaksamaan bersifat tak-homogen (misalnya membandingkan derajat tiga dengan derajat dua) dan memiliki batasan konstan seperti $a+b+c=1$, maka kita wajib melakukan homogenisasi dengan menyisipkan pengali ($a+b+c$) pada suku yang kekurangan derajat. Misalnya disyaratkan $a+b+c=1$, buktikan $a^2+b^2+c^2\geq a^3+b^3+c^3$. Ruas kiri dikalikan dengan faktor $(a+b+c)$ agar berderajat tiga
    :::{math}
        (a^2+b^2+c^3)(a+b+c) \geq a^3+b^3+c^3
    :::
    Setelah diekspansi, ketaksamana tersebut akan siap diselesaikan karena telah setara secara struktural
6. Teknik Normalisasi (Scaling)\
   Ini adalah operasi kebalikan dari homogenisasi. Apabila suatu ketaksamaan sejak awal sudah terbukti bersifat homogen, maka nilai rasio ruas kiri dan ruas kanannya invarian (tidak berubah) terhadap perkalian skalar konstan.
    Dalam situasi ini, kita memiliki justifikasi analitis untuk "memaksa" menetapkan sebuah kondisi tambahan tanpa mengurangi keumuman (\textit{Without Loss of Generality /WLOG})
    Jika ketaksamaan homogen pada variabel $a, b, c$ kita diizinkan untuk menormalisasi dengan memisalkan 
    :::{math}
        a+b+c=1 \text{ atau } abc=1 \text{ atau } a+b+c=3
    :::
    Teknik ini sangat brutal dan mematikan untuk memecahkan ketaksamaan homogen yang rumit menjadi bentuk fungsi satu satu atau dua variabel yang sederhana.

:::::{prf:example}
:label: contoh-1.24
Diketahui $a, b, c$ adalah bilangan real yang memenuhi $a+b+c=0$. Dengan menggunakan Identitas Euler, tentukan nilai dari ekspresi $\frac{a^3+b^3+c^3}{abc}$
::::{solution} contoh-1.24
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.25
Faktorkan bentuk selisih pangkat ganjil $x^5 - y^5$ ke dalam perkalian dua polinomial.
::::{solution} contoh-1.25
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.26
Diketahui bilangan bulat $n>1$. Gunakan bentuk Sophie Germain untuk membuktikan bahwa $n^4 + 4^n$ tidak pernah bernilai prima.
::::{solution} contoh-1.26
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.27
Misalkan $a, b, c$ adalah panjang sisi segitiga. Gunakan substitusi Ravi untuk membuktikan ketaksamaan
:::{math}
(a+b-c)(b+c-a)(c+a-b) \leq abc
:::
::::{solution} contoh-1.27
:class: dropdown
ini solusi
::::
:::::

:::::{prf:example}
:label: contoh-1.28
Diberikan bilangan real positif $a, b, c$ yang memenuhi syarat $a^2+b^2+c^2+2abc=1$. Gunakan substitusi trigonometri $a=\cos A, b=\cos B, c=\cos C$ untuk membuktikan bahwa $a+b+c\leq \frac{3}{2}$
::::{solution} contoh-1.28
:class: dropdown
ini solusi
::::
:::::

::::{exercise}
:label: exe-1.26
Gunakan pemfaktoran Sophie Germain untuk mencari faktor-faktor dari polinomial $x^4+4$
::::

::::{exercise}
:label: exe-1.27
Nyatakan ekspresi $(a+b)(b+c)(c+a)$ dalam bentuk variabel simetris $p=a+b+c, q=ab+bc+ca$, dan $r=abc$
::::

::::{exercise}
:label: exe-1.28
Diberikan $a, b, c>0$ dengan $abc=1$. Gunakan substitusi $a=\frac{x}{y}, b=\frac{y}{z}, c=\frac{z}{x}$ untuk membuktikan identitas 
:::{math}
\frac{1}{1+a+ab}+\frac{1}{1+b+bc}+\frac{1}{1+c+ca}=1
:::
::::

::::{exercise}
:label: exe-1.29
Diketahui $a, b, c$ bilangan real positif yang memenuhi $a+b+c=abc$. Gunakan substitusi trigonometri $a=\tan A, b=\tan B, c=\tan C$ (di mana $A+B+C=\pi$) untuk membuktikan bahwa
:::{math}
\frac{a}{\sqrt{1+a^2}}+\frac{b}{\sqrt{1+b^2}} + \frac{c}{\sqrt{1+c^2}}
:::
::::

::::{exercise}
:label: exe-1.30
Misalkan $a, b, c$ adalah bilangan real tak negatif. Buktikan ketaksamaan Schur derajat 3 berikut dengan menggunakan ekspresi variabel simetris $p, q, r$
:::{math}
p^3+9r \geq 4pq
:::
::::

## Soal Evaluasi Bab 1

:::{exercise} 
Buktikan bahwa untuk setiap bilangan real positif $a$ dan $b$, berlaku $\frac{a^2}{b} + \frac{b^2}{a}\geq a+b$
:::
:::{exercise} 
Diberikan bilangan real $a, b, c>0$. Buktikan bahwa $(a+b)(b+c)(c+a)\geq 8abc$.
:::
:::{exercise} 
Diberikan $x, y\in \mathbb{R}$. Buktikan bahwa $x^2+y^2+1\geq xy+x+y$.
:::
:::{exercise} 
Tentukan nilai minimum dari ekspresi multivariabel $f(x,y)=x^2+2y^2+2xy-6y+10$ untuk $x, y\in \mathbb{R}$.
:::
:::{exercise} 
Buktikan bahwa untuk setiap bilangan real $x, y, z$ berlaku $x^2+y^2+z^2 + 3 \geq 2(x+y+z)$. Tentukan kesamaan terjadi.
:::
:::{exercise} 
Diberikan bilangan real $a, b>0$. Buktikan bahwa $2(a^2+b^2)\geq (a+b)^2$.
:::
:::{exercise} 
Diberikan bilangan real $x>1$. Tentukan nilai minimum dari fungsi $f(x)=x+\frac{4}{x-1}$. (Petunjuk: Manipulasi menjadi bentuk $(x-1) + \frac{4}{x-1} + 1$).
:::
:::{exercise} 
Tentukan nilai maksimum dari ekspresi $x^2y$ jika diketahui $x, y>0$ dan $x+y=6$.
:::
:::{exercise} 
Diberikan bilangan real $a, b, c>0$. Tentukan nilai minimum dari ekspresi $\frac{a^2+b^2}{a+b}+\frac{b^2+c^2}{b+c}+\frac{c^2+a^2}{c+a}$ dalam bentuk fungsi $a, b, c$.
:::
:::{exercise} 
Diketahui $a, b >0$ dan $a+b=1$. Gunakan Lemma Titu untuk menentukan nilai minimum dari $\frac{1}{a}+\frac{1}{b}$
:::
:::{exercise} 
Diketahui $x, y, z>0$ dan $x+y+z=6$. Tentukan nilai minimum dari $\frac{x^2}{y+z}+\frac{y^2}{z+x}+\frac{z^2}{x+y}$.
:::
:::{exercise} 
Buktikan bahwa untuk setiap bilangan real $x, y, z>0$, berlaku $\sqrt{x+y}+\sqrt{y+z}+\sqrt{z+x}\leq \sqrt{6(x+y+z)}$.
:::
:::{exercise} 
Diberikan bilangan real positif $x, y, z$ yang memenuhi $x^2+y^2+z^2=3$. Buktikan bahwa $\frac{1}{1+xy}+\frac{1}{1+yz}+\frac{1}{1+zx}\geq \frac{3}{2}$.
:::
::::{exercise} 
Diketahui bilangan real positif $a, b, c$ yang memenuhi $ab+bc+ca=1$. Gunakan ketaksamaan Cauchy-Schwarz untuk membuktikan bahwa
:::{math}
    \frac{a}{\sqrt{a^2+bc}}+\frac{b}{\sqrt{b^2 + ca}}+\frac{c^2}{\sqrt{c^2+ab}} \leq \frac{3}{2}
:::
::::
:::{exercise} 
Diberikan bilangan real positif $x, y, z$. Gunakan ketaksamaan Jensen pada fungsi $f(t)=\frac{1}{t}$ untuk membuktikan bahwa $\frac{1}{x}+\frac{1}{y}+\frac{1}{z}\geq \frac{9}{x+y+z}$
:::
:::{exercise} 
Diketahui $x, y, z \in (0, \pi)$. Tentukan nilai maksimum dari $\sin x +\sin y +\sin z$ jika diketahui $x+y+z=\pi$.
:::
::::{exercise} 
Diketahui $a, b, c>0$ dan $a+b+c=1$. Gunakan fungsi $f(x)=\left(x+\frac{1}{x}\right)^2$ dan tunjukkan konveksitasnya untuk membuktikan bahwa 
:::{math}
    \left(a+\frac{1}{a}\right)^2 + \left(b+\frac{1}{b}\right)^2 +\left(c+\frac{1}{c}\right)^2 \geq \frac{100}{3}
:::
::::
:::{exercise} 
Buktikan ketaksamaan $a^ab^bc^c \geq \left(\frac{a+b+c}{3}\right)^{a+b+c}$ untuk setiap bilangan real positif $a, b, c$. (Petunjuka: Ambil logaritma natural pada kedua ruas dan gunakan konveksitas $n \ln{x}$).
:::
::::{exercise} 
Diberikan $a, b, c>0$. Definisikan $f(x)=\frac{1}{\sqrt{x}}$. Buktikan menggunakan Ketaksamaan Jensen Bahwa
:::{math}
    \frac{a}{\sqrt{b+c}}+\frac{b}{\sqrt{c+a}}+\frac{c}{\sqrt{a+b}} \geq \frac{a+b+c}{\sqrt{\frac{2(a+b+c)}{3}}}
:::
::::
:::{exercise} 
Diberikan bilangan real $a, b, c>0$. Tanpa mengurangi keumuman (WLOG), asumsikan $a\geq b\geq c$. Susunlah barisan $a^2, b^2, c^2$ untuk membuktikan bahwa $a^3+b^3+c^3 \geq a^2b + b^2c + c^2a$.
:::
:::{exercise} 
Diketahui $a, b>0$. Buktikan bahwa $a^5 + b^5 \geq a^4b + ab^4$.
:::
::::{exercise} 
Diberikan $a, b, c$ adalah panjang sisi-sisi suatu segitiga. Buktikan menggunakan ketaksamaan Rearrangement bahwa:
:::{math}
    \frac{a}{b+c-a} + \frac{b}{c+a-b} + \frac{c}{b+a-c} \geq 3
:::
::::
:::{exercise} 
Diberikan $a, b, c>0$. Buktikan bahwa $a^4 + b^4 + c^4 \geq a^2bc + b^2ca + c^2ab$.
:::
::::{exercise} 
Diberikan $n$ buah bilangan real positif $x_1, x_2, \cdots, x_n$. Dengan menggunakan ketaksamaan Rearrangement berulang atau identitas aljabar, buktikan bahwa:
:::{math}
    \frac{x_1^3}{x_2^2} + \frac{x_2^3}{x_3^2} + \cdots + \frac{x_n^3}{x_1^2} \geq x_1+x_2+\cdots+x_n
:::
::::
:::{exercise} 
Diberikan bilangan real $a, b, c$. Jika $p=a+b+c$, dan $q=ab+bc+ca$, nyatakan ekspresi $a^2+b^2+c^2$ dalam variabel $p$ dan $q$.
:::
:::{exercise} 
Buktikan bahwa polinomial $P(x,y,z)=x^2y+y^2z+z^2x$ adalah fungsi homogen. Berapa derajat homogenitasnya?
:::
:::{exercise} 
Diketahui sistem persamaan $x+y+z=1, x^2+y^2+z^2 = 2$, dan $x^3+y^3+z^3=3$. Gunakan substitusi Simetris Dasar dan Identitas Euler untuk mencari nilai dari $xyz$.
:::
:::{exercise} 
Diberikan $x, y\in \mathbb{R}$ yang memenuhi $x^2+y^2=1$. Gunakan substitusi trigonometri untuk menentukan nilai maksimum dan minimum dari ekspresi $3x+4y$.
:::
::::{exercise} 
Diberikan bilangan real $a, b, c>0$ yang memenuhi kondisi $ab+bc+ca=1$. Gunakan substitusi setengah sudut $\tan\left(\frac{A}{2}\right)$ atau modifikasi aljabar lainnya untuk membuktikan bahwa
:::{math}
    \frac{1}{a+b}+\frac{1}{b+c}+\frac{1}{c+a}\geq \frac{5}{2}
:::
::::