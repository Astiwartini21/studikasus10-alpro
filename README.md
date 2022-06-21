#include <iostream>
using namespace std;

class pointer{
public:
  void inputan();
private:
  char nama[30];
  char nim[15];
  pointer *next;
};

pointer *a = NULL;
pointer *b;
int pilihan = 0;


void pointer::inputan(){
  pointer *i, *j;
  i= new pointer;
  cout << endl;
  cout << "Masukkan Nama : ";
  cin >> i->nama;
  cout << "Masukkan Nim : ";
  cin >> i->nim;
  i->next=NULL;
  if(a==NULL){
    a=i;
    b = a;
  }
  else{
    j = a;
    while(j->next !=NULL){
      j=j->next;
    }
    j->next=i;
  }
  char lagi;cout<<endl;
  cout << "ulang? (y/t)  ";
  cin >>lagi;
  if(lagi=='y'){
    inputan();
  }
  else{
    cout << endl;
    cout << "SELESAI";
  }
}
int main(){
  pointer saya;
  cout<<"Data mahasiswa yang lolos Ke Babak Final";
  cout<<endl;
  saya.inputan();
}
