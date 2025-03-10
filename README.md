# NAMA : Abdul Haris Muhasibi
# NIM : 235150307111047

Repositori ini berisi kode Python untuk Pembuatan Kode Fungsi Alih Motor DC, mencakup:

# 1. Model Matematika Motor DC

# Persamaan Listrik
[ V = R i + L \frac{di}{dt} + K_e \omega ]

Penjelasan:
* ( V ) = Tegangan input (V)
* ( i ) = Arus motor (A)
* ( R ) = Resistansi (Ω)
* ( L ) = Induktansi (H)
* ( K_e ) = Konstanta GGL (V/rad/s)
* ( \omega ) = Kecepatan sudut (rad/s)

# Persamaan Mekanik
[ J \frac{d\omega}{dt} = T - B \omega ]

Penjelasan:
* ( J ) = Momen inersia (kg·m²)
* ( T ) = Torsi (Nm)
* ( B ) = Koefisien gesekan (Nm·s)

Torsi dihasilkan dari arus:
[ T = K_t i ]

dengan ( K_t ) sebagai konstanta torsi (Nm/A).

# 2. Transformasi Laplace

Menggunakan transformasi Laplace:

[ V(s) = (R + sL) I(s) + K_e \Omega(s) ]

[ J s \Omega(s) = K_t I(s) - B \Omega(s) ]

# 3. Fungsi Alih Motor DC

Dari dua persamaan di atas, diperoleh fungsi alih antara kecepatan sudut ( \Omega(s) ) dan tegangan ( V(s) ):

[ \frac{\Omega(s)}{V(s)} = \frac{K_t}{(J s + B)(R + sL) + K_e K_t} ]

Kode dalam repositori ini menggunakan SymPy untuk menyelesaikan perhitungan simbolik dan menyusun fungsi alih Motor DC.
