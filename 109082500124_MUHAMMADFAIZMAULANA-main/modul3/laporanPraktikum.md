# <h1 align="center">Laporan Praktikum Modul 1 - ... </h1>
<p align="center">[MUHAMMADFAIZMAULANA] - [109082500124]</p>

## Unguided 

### 1. [Soal]
#### soal1.go

```go
package main

import "fmt"
func factorial(n int) int {
	result := 1
	for i := 2; i <= n; i++ {
		result *= i
	}
	return result
}
func permutation(n, r int) int {
	return factorial(n) / factorial(n-r)
}

func combination(n, r int) int {
	return factorial(n) / (factorial(r) * factorial(n-r))
}

func main() {
	var a, b, c, d int
	fmt.Scan(&a, &b, &c, &d)

	p1 := permutation(a, c)
	c1 := combination(a, c)

	p2 := permutation(b, d)
	c2 := combination(b, d)

	fmt.Println(p1, c1)
	fmt.Println(p2, c2)
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1](https://github.com/mfaizmaulana20/109082500124_MuhammadFaizMaulana_Modul3/blob/main/109082500124_MUHAMMADFAIZMAULANA-main/modul3/output/Out%20Put%20-soal1.png)
[penjelasan] : Program Go tersebut menghitung permutasi dan kombinasi menggunakan fungsi faktorial. Input dibaca dengan fmt.Scan, lalu dihitung permutasi (n!/(n−r)!) dan kombinasi (n!/(r!(n−r)!)) menggunakan fungsi factorial, kemudian hasilnya ditampilkan.

## Unguided 

### 2. [Soal]
#### soal2.go

```go
package main

import "fmt"
func f(x int) int {
	return x * x
}
func g(x int) int {
	return x - 2
}
func h(x int) int {
	return x + 1
}

func main() {
	var a, b, c int
	fmt.Scan(&a, &b, &c)

	result1 := f(g(h(a)))

	result2 := g(h(f(b)))

	result3 := h(f(g(c)))

	fmt.Println(result1)
	fmt.Println(result2)
	fmt.Println(result3)
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1](https://github.com/mfaizmaulana20/109082500124_MuhammadFaizMaulana_Modul3/blob/main/109082500124_MUHAMMADFAIZMAULANA-main/modul3/output/Out%20Put-Soal%202.png)
[penjelasan] : Program Go tersebut menghitung komposisi fungsi f, g, dan h dari input pengguna, lalu menampilkan hasil gabungan seperti f(g(h(a))), g(h(f(b))), dan h(f(g(c))).

## Unguided 

### 3. [Soal]
#### soal3.go

```go
package main

import (
	"fmt"
	"math"
)

func jarak(a, b, c, d float64) float64 {
	return math.Sqrt(math.Pow(a-c, 2) + math.Pow(b-d, 2))
}
func dalamLingkaran(cx, cy, r, x, y float64) bool {
	return jarak(cx, cy, x, y) <= r
}

func main() {
	var cx1, cy1, r1 float64
	var cx2, cy2, r2 float64
	var x, y float64

	fmt.Scan(&cx1, &cy1, &r1)
	fmt.Scan(&cx2, &cy2, &r2)
	fmt.Scan(&x, &y)
	in1 := dalamLingkaran(cx1, cy1, r1, x, y)
	in2 := dalamLingkaran(cx2, cy2, r2, x, y)

	if in1 && in2 {
		fmt.Println("Titik di dalam lingkaran 1 dan 2")
	} else if in1 {
		fmt.Println("Titik di dalam lingkaran 1")
	} else if in2 {
		fmt.Println("Titik di dalam lingkaran 2")
	} else {
		fmt.Println("Titik di luar lingkaran 1 dan 2")
	}
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1](https://github.com/mfaizmaulana20/109082500124_MuhammadFaizMaulana_Modul3/blob/main/109082500124_MUHAMMADFAIZMAULANA-main/modul3/output/Out%20Put-Soal%203.png)
[penjelasan] :Program Go tersebut mengecek apakah suatu titik berada di dalam lingkaran dengan menghitung jarak titik ke pusat dan membandingkannya dengan jari-jari, lalu menampilkan hasilnya.



