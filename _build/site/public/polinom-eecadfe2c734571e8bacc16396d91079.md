# Polinomial (Suku Banyak)

## Sifat-Sifat Dasar, Algoritma Pembagian, dan Teorema Sisa/Faktor

Dalam eksplorasi aljabar tingkat lanjut, polinomial (suku banyak) menempati posisi yang sangat fundamental. Objek matematis ini tidak hanya berperan sebagai perluasan alami dari representasi bilangan real dalam bentuk fungsi, tetapi juga menjadi basis bagi aljabar abstrak dan teori bilangan. Sebelum menganalisis karakteristik akar dan identitas tingkat tinggi, penguasaan terhadap anatomi dasar dan operasi aritmatika polinomial adalah prasyarat mutlak.

### Pengantar

Polinomial dapat dipandang sebagai sebuah ekspresi aljabar yang dikonstruksi melalui operasi penjumlahan dan perkalian menggunakan konstanta dan sebuah variabel bebas (independen) yang dipangkatkan dengan bilangan cacah.

::::{prf:definition}
Sebuah polinomial $P(x)$ dalam variabel bebas $x$ di atas himpunan bilangan real $\mathbb{R}$ adalah ekspresi aljabar yang dapat dituliskan dalam bentuk standar:
:::{math}
P(x) = a_n x^n + a_{n-1} x^{n-1} + \dots + a_1 x + a_0
:::
di mana:
1. $n$ adalah bilangan cacah ($n \in \mathbb{W}$),
2. $a_0, a_1, \dots, a_n$ adalah konstanta real ($a_i \in \mathbb{R}$) yang disebut sebagai koefisien polinomial,
3. $a_n \neq 0$.
::::

Berdasarkan definisi struktural di atas, kita dapat menurunkan beberapa terminologi esensial yang melekat pada setiap polinomial:
* Derajat (Degree): Pangkat tertinggi dari variabel $x$ pada polinomial tersebut. Jika $a_n \neq 0$, maka polinomial $P(x)$ dikatakan berderajat $n$. Derajat polinomial umumnya dinotasikan secara analitik dengan $\deg(P(x)) = n$.
* Koefisien Utama (Leading Coefficient): Koefisien dari suku dengan pangkat tertinggi, yakni $a_n$.
* Suku Tetap (Konstanta / Constant Term): Suku yang tidak memuat variabel $x$ (atau $x^0$), yakni $a_0$.
* Polinomial Monik (Monic Polynomial): Sebuah polinomial khusus di mana nilai koefisien utamanya adalah tepat $1$ ($a_n = 1$).


:::{prf:definition}
Dua buah polinomial $P(x) = a_n x^n + \dots + a_0$ dan $Q(x) = b_m x^m + \dots + b_0$ dikatakan identik atau sama ($P(x) \equiv Q(x)$) jika dan hanya jika kedua polinomial tersebut memiliki derajat yang sama ($n = m$) dan koefisien pada setiap suku yang bersesuaian bernilai sama ($a_i = b_i$ untuk setiap $i$).
:::

Kumpulan seluruh polinomial dengan koefisien real tertutup terhadap operasi penjumlahan, pengurangan, dan perkalian. Misalkan diberikan dua polinomial $P(x)$ dan $Q(x)$, maka berlaku sifat-sifat derajat berikut:

::::{prf:proposition}
1. Penjumlahan/Pengurangan: Derajat dari polinomial hasil penjumlahan atau pengurangan tidak akan melebihi derajat maksimum dari kedua polinomial pembentuknya.
:::{math}
\deg(P(x) \pm Q(x)) \leq \max(\deg(P(x)), \deg(Q(x)))
:::
(Tanda ketaksamaan berlaku jika suku-suku berderajat tinggi saling menghilangkan).
1. Perkalian: Derajat dari polinomial hasil perkalian adalah eksak sama dengan jumlahan dari derajat masing-masing polinomial.
:::{math}
\deg(P(x) \cdot Q(x)) = \deg(P(x)) + \deg(Q(x))
:::
::::