# Praktikum
Praktikum pertemuan kedua
#include<iostream>
using namespace std;
int main (){
	int menu, jumlah,total,bayar,ongkir,potong;
	float diskon;
	char jarak;
	char tambah;
	a:
	cout<<"\tMenu yang tersedia\n"<<endl;
	cout<<"1.Ayam Geprek\t=\tRp 21.000"<<endl;
	cout<<"2.Ayam Goreng\t=\tRp 17.000"<<endl;
	cout<<"3.Udang Goreng\t=\tRp 19.000"<<endl;
	cout<<"4.Cumi Goreng\t=\tRp 20.000"<<endl;
	cout<<"5.Ayam Bakar\t=\tRp 25.000"<<endl;
	cout<<"\n";
	cout<<"Pilihlah menu yang anda inginkan: ";cin>>menu;
	cout<<endl;
	cout<<"Jumlah pesanan: ";cin>>jumlah;
	cout<<endl;
	
	switch(menu){
		case 1:
			total = 21000*jumlah;
			break;
		case 2:
			total = 17000*jumlah;
			break;
		case 3:
			total = 19000*jumlah;
			break;
		case 4:
			total = 20000*jumlah;
			break;
		case 5:
			total = 25000*jumlah;
			break;
	}
	
	cout << "Masukkan Jarak tempuh[KM] yang akan dilalui : ";
	cin >> jarak;
	cout<<endl;
	
	if(jarak <= 3) {
		cout <<"Biaya Ongkir dikenakan sebanyak Rp.15,000" <<endl;
		ongkir = 15000;
		cout<<endl;
	} else if(jarak >= 3) {
		cout <<"Biaya Ongkir dikenakan sebanyak Rp.25,000" <<endl;
		ongkir = 25000;
		cout<<endl;
	} 
	
	if(total > 25000 && total <= 50000 ){
		cout <<"Mendapatkan potongan Ongkir Rp.3000\n";
		potong = ongkir - 3000;
		diskon = 0 * total;
 	
	} else if(total > 50000 && total <= 150000) {
		cout <<"\nMendapatkan potongan ongkir sebesar Rp.5000 dan diskon 15% \n";
		potong = ongkir - 5000;
		diskon = 0.15 * total;
	} else if(total > 150000) {
		cout <<"\nMendapatkan potongan ongkir sebesar Rp.8000 dan diskon 35% \n";
		potong = ongkir - 8000;
		diskon = 0.35 * total;
	} else {
		cout << "\nTidak mendapat potong";
	}
	cout <<"\nJumlah Bayar\t:\tRp." <<total <<endl;
	cout <<"Jarak tempuh\t:\t" <<jarak <<" KM." <<endl;
	cout <<"Total Ongkir\t:\tRp." <<potong <<endl;
	cout <<"Diskon\t\t:\tRp." <<diskon <<endl; 
	cout <<"Total Bayar\t:\tRp." <<total - diskon + potong <<endl<<endl;
	cout <<"Bayar\t\t:\tRp.";cin >> bayar; 
	cout <<"Kembali\t\t:\tRp.";
	cout <<(bayar - (total - diskon + potong)) <<endl<<endl;
	
	cout<<"Apakah ada pesanan lagi? (y/n)";
	cin>>tambah;

    if (tambah =='y'){
    cout<<"Pesanan mu telah selesai ";
    	system("cls");
    	goto a;
	}else(tambah =='n');{
		exit(0);
	}
}
