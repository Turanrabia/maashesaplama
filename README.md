# maashesaplama
public  class  Çalışan {
    dize  adı ;
    çift  ​​maaş ;
    int  çalışma saatleri ;
    int  kiralamaYıl ;


    Çalışan ( Dize  adı , int  maaş , int  çalışmaSaatleri , int  kiralamaYıl ) {
        bu . isim = isim ;
        bu . maaş = maaş ;
        bu . workHours = workHours ;
        bu . kiralamaYıl = kiralamaYıl ;


    }

    çifte  vergi () {

        if ( bu . maaş > 1000 ) {
            çift  ​​maaşVergi = ( bu . maaş * 0.03 );
             maaş iadesiVergi ;
        } başka {
            Sistem . dışarı . println ( "Vergi borcunuz yoktur." );
             0 döndür ;
        }
    }

    int  bonusu () {

        if ( workHours - 40 > 0 ) {
            int  bonusSaat = ( workHours - 40 ) * 30 ;
            dönüş  bonusSaat ;
        } başka {
             0 döndür ;
        }
    }

    çift  ​​zamMaaş () {
        int  zamHesap =   2021 - bu . kiralamaYıl ;
        çift  ​​maasArtisi ;
        if ( yükseltHesap < 10 ) {
            maasArtisi = ( bu . maaş ) * 0.05 ;
            dönüş  maasArtisi ;
        } else  if ( upgradeCalc > 9 && upgradeCalc < 20 ) {
            maasArtisi = ( bu . maaş ) * 0.1 ;
            dönüş  maasArtisi ;
        } else  if ( Calc > 19 ) {
            maasArtisi = ( bu . maaş ) * 0.15 ;
            dönüş  maasArtisi ;
        } başka {
            Sistem . dışarı . println ( "Maaş Artışı Yoktur." );
             0 döndür ;
        }

    }

    public  String  toString () {
        çift  ​​toplam = maaş - vergi () + ikramiye () + zamMaaş ();
        çift  ​​vergili = maaş + ikramiye () - vergi ();

        Sistem . dışarı . println ( "Adı: " + bu . isim );
        Sistem . dışarı . println ( "Maaşı:" + bu .maaş ) ;
        Sistem . dışarı . println ( "Çalışma Saati:" + bu .workHours ) ;
        Sistem . dışarı . println ( "Başlangıç ​​Yıllı: " + this . RentalYear );
        Sistem . dışarı . println ( "Vergi:" + vergi ());
        Sistem . dışarı . println ( "Bonus :" + bonus ());
        Sistem . dışarı . println ( "Maaş artışı : " + zamSalary ());
        Sistem . dışarı . println ( "Vergi ve Bonuslar ile birlikte maaş : " + vergili );
        Sistem . dışarı . println ( "Toplam Maaş: " + toplam );

         null döndür ;
    }
}
