
# ogrenci_kayit_sistemi
#include<stdio.h>
#include<stdlib.h>
#include<string.h>

 typedef struct ogrenci{
 	int no;
 	char ad[50];
 	float vize;
 	float final;
 	
 	struct ogrenci* next;
 }
 ogrenci* bas=NULL;
 ogrenci* yeniogrenci(int no, const char* ad,float vize , float final ){
 ogrenci* ogr=(ogrenci*)malloc(sizeof(ogrenci));
 ogr->no=no;
 strcpy(ogr->ad=ad);
 ogr->vize=vize;
 ogr->final=final;
 ogr->next=NULL;
 return ogr;
 }
 void kayitekle{
 	int no;
 	char[50];
 	float vize;
 	float final;
 	
 	printf("ogrenci no girin:");
 	scanf("%d",&no);
 	printf("ogrenci ismi girin:");
 	scanf("%c",ad);
 	printf("vize notu girin:");
 	scanf("%f",&vize);
 	printf("final notu girin:");
 	scanf("%f",&final);
 	
 	ogrenci* yeni=yeniogrenci(no,ad,vize,final);
 	if (bas==NULL){
 		NULL=ogrenci;
	 }
 else {
 	ogrenci* gecici=bas
 	while(gecici->sonraki != NULL)
 		gecici=gecici->sonraki;
 		gecici->gecici=yeni;
 	}
	 printf("kayit  ba�ar�yla eklendi.");
 	}
 	float basarinotu(ogrenci* ogr){
 	return ogr->vize * 40/100+ ogr->final * 60/100;
 
 	}
 	void kayitListele() {
    int secim;
    char ad[50];
    int no;
    printf("\n--- Listeleme Men�s� ---\n");
    printf("1- Numaraya g�re ara\n");
    printf("2- �sme g�re ara\n");
    printf("3- Ba�ar� notu >= 60 olanlar\n");
    printf("Se�im: ");
    scanf("%d", &secim);

    Ogrenci* gecici = bas;
    int bulundu = 0;

    if (secim == 1) {
        printf("��renci numaras�: ");
        scanf("%d", &no);
        while (gecici != NULL) {
            if (gecici->no == no) {
                printf("No: %d, Ad: %s, Vize: %.2f, Final: %.2f, Ortalama: %.2f\n"),
                    gecici->no, gecici->ad, gecici->vize, gecici->final, basariNotu(gecici));
                bulundu = 1;
                break;
            }
            gecici = gecici->sonraki;
        }
        if (!bulundu) printf("Kay�t bulunamad�.\n");

    } else if (secim == 2) {
        printf("�sim: ");
        scanf(" %[^\n]", ad);
        while (gecici != NULL) {
            if (strstr(gecici->ad, ad)) {
                printf("No: %d, Ad: %s, Vize: %.2f, Final: %.2f, Ortalama: %.2f\n"),
                    gecici->no, gecici->ad, gecici->vize, gecici->final, basariNotu(gecici));
                bulundu = 1;
            }
            gecici = gecici->sonraki;
        }
        if (!bulundu) printf("Kay�t bulunamad�.\n");

    } else if (secim == 3) {
        while (gecici != NULL) {
            if (basariNotu(gecici) >= 60.0) {
                printf("No: %d, Ad: %s, Ortalama: %.2f\n",
                    gecici->no, gecici->ad, basariNotu(gecici));
                bulundu = 1;
            }
            gecici = gecici->sonraki;
        }
        if (!bulundu) printf("Hi�bir ��renci 60 ve �zeri de�il.\n");
    }
}
 	int main(){
 		
 		int secim;

    do {
        printf("\n--- ogrenci Kayit Sistemi ---\n");
        printf("1- Yeni Kayit Ekleme\n");
        printf("2- Kayit Listeleme\n");
        printf("3- Kayit Guncelleme\n");
        printf("4- Kayit Silme\n");
        printf("5- Sinif Ortalamasi Hesapla\n");
        printf("6- En Basarili ogrenciyi Goster\n");
        printf("0- ��k�\n");
        printf("Seciminiz: ");
        scanf("%d", &secim);

        switch (secim) {
            case 1: kayitEkle(); break;
            case 2: kayitListele(); break;
            case 3: kayitGuncelle(); break;
            case 4: kayitSil(); break;
            case 5: ortalamaHesapla(); break;
            case 6: enBasarili(); break;
            case 0: printf("��k�l�yor...\n"); break;
            default: printf("Ge�ersiz se�im!\n");
        }

    } while (secim != 0);

    return 0;
}	
	 }
 	
 	
 	
 	
 	
 	
 	
 	
