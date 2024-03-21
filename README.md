#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    char op;
    float num1, num2;

    // it allows user to enter operator i.e. +, -, *, /
    cout << "Enter operator (+, -, *, /)";
    cin >> op;

    // it allows user to enter the operands
    cout << "Enter two operands: ";
    cin >> num1 >> num2;

    //switch statement begins 
    switch (op) {
        // if user enters +
        case '+':
            cout << "Result: " << num1 + num2;
            break;
        // if user enters -
        case '-':
            cout << "Result: " << num1 - num2;
            break;
        // if user enters *
        case '*':
            cout << "Result: " << num1 * num2;
            break;
        // if user enters /
        case '/':
            if (num2 != 0) {
                cout << "Result: " << fixed << setprecision(2) << num1 / num2;
            } else {
                cout << "Result: " << "Error! Division by zero is not allowed.";
            }
            break;
        // if the operator is other than +, -, *, /, error will message will display 
        default:
            cout << "Error! Operator is not correct";
    } // switch statement ends

    return 0;
}


///guided 2
#include <stdio.h>
#include <string.h>

//struct
struct Mahasiswa
{
    char name[50];
    char address[100];
    int age;
};
int main()
{
//menggunakan struct
struct Mahasiswa mhs1, mhs2;
//mengisi nilai ke struct
strcpy(mhs1.name, "Dian");
strcpy(mhs1.address, "Mataram");
mhs1.age = 22;
strcpy(mhs2.name, "Bambang");
strcpy(mhs2.address, "Surabaya");
mhs2.age = 23;

//cetak isis struct
printf("## Mahasiswa 1 ##\n");
printf("Nama: %s\n", mhs1.name);
printf("Alamat: %s\n", mhs1.address);
printf("Umur: %d\n", mhs1.age);
printf("\n");
printf("## Mahasiswa 2 ##\n");
printf("Nama: %s\n", mhs2.name);
printf("Alamat: %s\n", mhs2.address);
printf("Umur: %d\n", mhs2.age);
return 0;
}


//guided 3
#include <iostream>
#include <array>
using namespace std;

int main() {
    //deklarasi dan inisialisasi array
    int nilai[5];
    nilai[0] = 23;
    nilai[1] = 50;
    nilai[2] = 34;
    nilai[3] = 78;
    nilai[4] = 90;

    //mencetak array dengan tab
    cout << "Isi array pertama: " << nilai[0] << endl;
    cout << "Isi array kedua : " << nilai[1] << endl;
    cout << "Isi array ketiga: " << nilai[2] << endl;
    cout << "Isi array keempat: " << nilai[3] << endl;
    cout << "Isi array kelima: " << nilai[4] << endl;

    return 0;
}

//soal 1
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    char op;
    float num1, num2;

    // pilih rumus bangun datar
    cout << "pilih jenis bangun datar (p: persegi,g: persegi panjang,s: segitiga): ";
    cin >> op;

    // masukan nilai/angka yang akan dioperasikan 
    cout << "Masukan nilai/angka: ";
    cin >> num1 >> num2;

    //masukan rumus-rumus 
    switch (op) {
    //rumus luas persegi panjang
        case 'g':
            cout << "panjang: ";
            cin >> num1;
            cout << "lebar: ";
            cin >> num2;
            cout << "luas persegi panjang adalah: ", num1 * num2;
            break;
    // rumus luas persegi
        case 'p':
            cout << "panjang: ";
            cin >> num1, num2;
            cout << "luas persegi addalah: ", num1 * num1, num2 * num2;
            break;
    // rumus segitiga
        case 's':
            cout << "alasnya: ";
            cin >> num1;
            cout << "tingginya: ";
            cin >> num2;
            cout << "luas segitiga adalah: ", num1 * num2 /2;
            break;
    //jika tidak ada rumus lain selain yang disebutkan, maka akan error
        default:
            cout << "Error! tidak dapat mengoperasikan perhitungan" << endl;
    } // selesai memasukkan pernyataan

    return 0;
}
// Tipe data primitif ini merupakan tipe data yang ditentukan sistem, perbedaan penggunaan bahasa pemrograman terletak pada jumlah bit yang dimasukan untuk setiap bit tergantung pada bahasa pemrograman,compiler dan sistem operasinya.
// Contoh tipe data primitif adalah: Int(berfungsi untuk menyimpan bilangan bulat), Float(berfungsi untuk menyimpan bilangan desimal),
// Char(berfungsi untuk menyimpan data berupa sebuah huruf), Boolean(berfungsi untuk menyimpan dua nilai yaitu true dan false).

//soal 2
// Class :fitur Object Oriented Program(OOP) berfungsi untuk membungkus tipe data di dalamnya sebagai anggota.
// Fungsi: Abstraksi(class berfungsi untuk menggabungkan data dan struktur dalam satu kode program),
//inheritance(class yang berfungsi untuk membagikan variabel dan fungsi dari class pertama ke class kedua),
//encapsulation(class yang berfungsi untuk menyembunyikan detail implementasi dan hanya mengekspos metode publik),
//polymorphism(class yang menggunakan metode dengan nama yang sama pada class yang berbeda).
//contoh class:

#include <iostream>
using namespace std;

class binatang {
public:
    string name;

    binatang(string n) {
        name = n;
    }
};

int main() {
    // contoh binatang dalam kandang
    binatang hewan("kudanil");
    cout << "Nama: " << hewan.name << endl;

    // mengubah hewan dalam kandang
    cout << "Nama : " << hewan.name << endl;

    return 0;
}

//Fungsi dari struct: Value Type(type data yang hanya menyalin objek identik dan tidak berbagi objek dengan struct asli).
// contoh struct:

#include <stdio.h>
#include <string.h>

struct Mahasiswa
{
    char name[50];
    char address[100];
    int age;
};
int main()
{

struct Mahasiswa mhs1, mhs2;
strcpy(mhs1.name, "Dian");
strcpy(mhs1.address, "Mataram");
mhs1.age = 22;
strcpy(mhs2.name, "Bambang");
strcpy(mhs2.address, "Surabaya");
mhs2.age = 23;

printf("## Mahasiswa 1 ##\n");
printf("Nama: %s\n", mhs1.name);
printf("Alamat: %s\n", mhs1.address);
printf("Umur: %d\n", mhs1.age);
printf("\n");
printf("## Mahasiswa 2 ##\n");
printf("Nama: %s\n", mhs2.name);
printf("Alamat: %s\n", mhs2.address);
printf("Umur: %d\n", mhs2.age);
return 0;
}

//soal 3
//perbedaan array dengan map 
//Array adalah tipe data yang menggunakan indeks(int/angka) dengan tipe data yang sama dan ukuran yang dapat ditentukan saat deklarasi.
//sedangkan map merupakan tipe data yang menggunakan indeks(selain integer) dengan tipe yang tidak harus sama dan ukuran dapat berubah/dinamis serta memiliki key yang dapat diberi nama.
//tipe data map

#include <iostream>
#include <map>
using namespace std;

int main() {
    // Membuat map dengan key bertipe string dan value bertipe integer
    map<string, int> pendidikan;

    // Menambahkan data ke map
    pendidikan["SD"] = 6;
    pendidikan["SMP"] = 3;

    // Mengakses data dari map
    cout << "'SD' value from pendidikan: " << pendidikan["SD"] << endl;
    cout << "'SMP' value from pendidikan: " << pendidikan["SMP"] << endl;

    // Menggunakan iterator untuk iterasi melalui map
    map<string, int>::iterator it;
    for (it = pendidikan.begin(); it != pendidikan.end(); ++it) {
        cout << "Key: " << it->first << ", Value: " << it->second << endl;
    }

    return 0;
}
