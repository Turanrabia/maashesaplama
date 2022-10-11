/*
* Java'da "Employee"da fabrika çalışanlarını temsil eden ve metotları ile karşılamalarını hesaplayan bir sınıf yazmalısınız. Bu sınıf 4 nitelik ve 5 metoda sahip olacaktır.
Sınıfın Nitelikleri
isim : çalışanın adı ve soyadı
maaş : Çalışanın maaşı
çalışma Saatleri : Haftalık çalışma saati
kiralamaYıl : İşe başlangıç ​​yılı
Sınıfın Metotları
Çalışan(isim,maaş,çalışma saati,kiralıkYıl) : Kurucu metot olup 4 parametresi.
vergi(): Maaşa uygulanan vergiyi hesaptır.
Çalışanın maaşı 1000 TL'den az vergi uygulanmayacaktır.
Çalışanın maaşı 1000 TL'den fazla maaşının %3'ü kadar vergi ödenecektir.
bonus() : Eğer çalışan çalıştırılırsa 40 günlük bir süreçten yararlanılırsa, ikramiye işletmeciliği 30 TL olur.
upgradeSalary(): Çalışanın işe başlamak için gözden geçirilmesini hesapla. şu an ki yılı 2021 olarak alın.
Eğer çalışan 10 az bir sese maaşına %5 zamdan önce.
Eğer çalışan 9 çalışan çok ve 20 azsa maaşına %10 zam gibi.
Eğer çalışan 19 üretim işisa %15 zam yapımı.
toString : Çalışana ait olduğu konusunda emin olacaktır.
*/
genel  sınıf  Uygulaması {
    public  static  void  main ( String [] args ) İstisna { 'yi atar 
        Maas  m = yeni  Maas ( "Ahmet veren" , 2000 , 45 , 2002 );
        m . bilgi ();
        Maas  n = yeni  Maas ( "Yavuz Sisko" , 600 , 80 , 1975 );
        n . bilgi ();
    }
}

sınıf  Maas {
    dize  adı ;
    çift  ​​maaş ;
    int  çalışma saatleri ;
    int  kiralamaYıl ;

    Maas ( Dize  adı , çift  maaş , int  çalışmaSaatleri , int  kiralamaYıl ) {
        bu . isim = isim ;
        bu . maaş = maaş ;
        bu . kiralamaYıl = kiralamaYıl ;
        bu . workHours = workHours ;
    }

    çifte  vergi () {
        çift  ​​vergi ;
        if ( maaş > 1000 ) {
            vergi = maaş * 0.03 ;

        } başka {
            vergi = 0 ;
        }
        dönüş  vergi ;
    }

    çifte  bonus () {
        çifte  ikramiye ;
        if ( workHours > 40 ) {
            ikramiye = ( çalışma Saati - 40 ) * 30 ;
        } başka {
            ikramiye = 0 ;
        }
        iade  bonusu ;

    }

    çift  ​​zamMaaş () {
        double  artisMiktari = 0 ;
        çift  ​​kacYil = 2022 - kiralamaYıl ;
        if ( kacYil < 10 ) {
            artisMiktari = maaş * 0.05 ;
        }
        if ( kacYil >= 10 && kacYil < 20 ) {
            artısMiktari = maaş * 0.10 ;
        }
        if ( kacYil >= 20 ) {
            artısMiktari = maaş * 0.15 ;
        }
        dönüş  artisMiktari ;
    }

    geçersiz  bilgi () {
        çift  ​​toplam = maaş - vergi () + ikramiye () + zamMaaş ();
        Sistem . dışarı . println ( "------------------------------------" );
        Sistem . dışarı . println ( "İsim Soyisim:" + bu . isim );
        Sistem . dışarı . println ( "Hangi Yıl Başladi: " + bu . kiralamaYıl );
        Sistem . dışarı . println ( "Haftada kaç ssat calisiyor:" + bu .workSaat ) ;
        Sistem . dışarı . println ( "vergisiz bonussuz maasi:" + bu . maaş );
        Sistem . dışarı . println ( "vergi:" + vergi ());
        Sistem . dışarı . println ( "bonus:" + bonus ());
        Sistem . dışarı . println ( "Artis Miktari:" + zamMaaş ());
        Sistem . dışarı . println ( "Toplam Maas: " + toplam );
    }
}
