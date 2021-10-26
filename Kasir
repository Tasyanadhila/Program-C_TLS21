#include <iostream>
#include <conio.h>
#include <iomanip>
#define max 100
using namespace std;
int main(){
	string menu[max];
	char kembali;
	int harga[max], jumlah[max], kembalian, bayar, total=0, i=0;
	do{
		cout << " Masukkan nama menu\t: ";
		getline(cin, (menu[i]));
		cout << " Masukkan harga menu\t: ";
		cin >> harga[i];
		cout << " Masukkan jumlah menu\t: ";
		cin >> jumlah[i];
		cout << " Ingin menginput lagi? (y/n)";
		cin>>kembali;
		cin.ignore();
		total = total + (harga[i]*jumlah[i]);
		i++;
		
	}while(kembali == 'y' || kembali == 'Y');
	
	cout << "\t+===============================================================+\n";
	cout << "\t|               MENU                  Jumlah        Harga (IDR) |\n";
	cout << "\t|_______________________________________________________________|\n";
	cout << "\t|                                                               |\n";
	for(int j = 0 ; j < i; j++){
			cout << "\t|  "<< setw(27) << menu[j] << "       " << setw(5) << jumlah[j] << "            "<< setw(7) << harga[j]<<"   |" << endl;
	}
	cout << "\t|                                                               |\n";
	cout << "\t+---------------------------------------------------------------+\n";
	cout << "\t|                                         Total : IDR " << setw(7) << total << "   |" << endl;
	cout << "\t+===============================================================+\n\n\n";
	cout << " Uang dibayarkan\t: IDR ";
	cin >> bayar;
	kembalian = bayar - total;
	cout << " Uang kembalian\t\t: IDR " << kembalian;
}
