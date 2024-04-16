import math

print("Nama : Valentino Silalahi")
print("Nim  : 2310431015")
print("Program Tabel Fungsi")

ulang = 'Y'
while ulang == 'Y' or ulang == 'y':

    print("\n==================================================")
    print("                  TABEL FUNGSI")
    print("==================================================")

    n = int(input("\nMasukkan banyak data : "))

    x = [0] * n
    f = [0] * n
    g = [0] * n
    h = [0] * n

    print("\nInputkan", n, "buah data :\n")
    for i in range(n):
        x[i] = int(input(f"Input nilai x ke-{i+1} = "))

        if x[i] >= 0:
            f[i] = (3*(x[i]**2)) + (7*x[i]) - 2
        if x[i] < 0:
            f[i] = (2*(x[i]**2)) - (5*x[i]) - 4

        g[i] = (f[i]**2) - math.sqrt(f[i])
        h[i] = f[i] * g[i]

    print("\nNo \tx \tf(x) \t    g(x) \t    \t   \th(x)")
    for i in range(n):
        print(f"{i+1}\t{x[i]}\t{f[i]}\t{g[i]}\t   {h[i]}")

    ulang = input("Mau ulang lagi [Y/T] : ")
