
#include <iostream>
#include <conio.h>
#include <iomanip>
#define max 100
//define : mendefinisikan variable max bernilai 100
using namespace std;
/* using namespace std berfungsi untuk meminimalisir kesalahan akbiat tidak 
 * dikenalinya fungsi cout dan cin apabila dalam penulisan secara langsung
 */
int main(){
	string menu[max];	//membuat variable menu dengan 100 index array bertipe data string
	char kembali;	//membuat variable kembali bertipe data char
	int harga[max], jumlah[max], kembalian, bayar, total=0, i=0;
	/* membuat variable harga dan jumlah dengan 100 index array bertipe data integer
	 * membuat variable kembalian dan bayar bertipe data integer
	 * membuat vatiable total dan i bernilai 0
	 */
	do{	// menjalankan fungsi do
		cout << " Masukkan nama menu\t: ";
		getline(cin, (menu[i]));	// input nilai kedalam variable menu[i]
		cout << " Masukkan harga menu\t: ";
		cin >> harga[i];	// input nilai kedalam variable harga[i]
		cout << " Masukkan jumlah menu\t: ";
		cin >> jumlah[i];	// input nilai kedalam variable jumlah[i]
		cout << " Ingin menginput lagi? (y/n)";
		cin<<kembali;	// kembali ke fungsi awal jika mau input barang lebih dari 1 jenis
		cin.ignore();	// mengabaikan sebuah new line dari hasil getline(cin, (menu[i]));
		total = total + (harga[i]*jumlah[i]);	// menyimpan nilai total dari perulangan harga[i] dikalikan dengan jumlah[i]
		i++;
		
	}while(kembali == 'y' || kembali == 'Y');	// menjalankan fungsi while sebagai perulangan jika variable kembali = 'y' atau 'Y'
	
	cout << "\t+===============================================================+\n";
	cout << "\t|               MENU                  Jumlah        Harga (IDR) |\n";
	cout << "\t|_______________________________________________________________|\n";
	cout << "\t|                                                               |\n";
	for(int j = 0 ; j < i; j++){ // melakukan perulangan pada seluruh nilai yang tersimpan dalam array sebanyak i
			cout << "\t|  "<< setw(27) << menu[j] << "       " << setw(5) << jumlah[j] << "            "<< setw(7) << harga[j]<<"   |" << endl;
	} // setw berfungsi untuk mengatur lebar tampilan dilayar dari suatu nilai variable
	cout << "\t|                                                               |\n";
	cout << "\t+---------------------------------------------------------------+\n";
	cout << "\t|                                         Total : IDR " << setw(7) << total << "   |" << endl;
	cout << "\t+===============================================================+\n\n\n";
	cout << " Uang dibayarkan\t: IDR ";
	cin >> bayar;
	kembalian = bayar - total;
	cout << " Uang kembalian\t\t: IDR " << kembalian;
}
