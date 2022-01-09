# java-örnek-sorular
oryantasyon ödevi
https://youtu.be/f_3kHnk8-Mo
        
        örnek1
        
        kullanıcıdan alınan vize,final ve quiz notuna göre 
        ortalamayı hesaplayan ve ortalamaya göre ekrana geçtiniz ya da kaldınız 
        yazdıran program yapalım.
        
        
        
        package ortalamahesabiörnek;
import java.util.Scanner;
public class Ortalamahesabiörnek{
    public static void main(String[]args){
        Scanner input=new Scanner(System.in);
        
       
        
    int vize,finaln,quiz;
    double ortalama;
    System.out.println("vizeyi giriniz:");
    vize=input.nextInt();
    System.out.println("finaln giriniz:");
    finaln=input.nextInt();
    System.out.println("quizi giriniz:");
    quiz=input.nextInt();
    ortalama=vize*0.4+finaln*0.5+quiz*0.1;
    System.out.println("not ortalamanız:"+ortalama);
    String sonuc=(ortalama>=50)? "geçtiniz":"kaldınız";
    System.out.println(sonuc);
   
    
    }
}




      örnek2
    
    kullanıcıdan ürünün kdvsiz ücretini,kdv oranını alarak
    ürünün kdvli fiyatını yani yeni fiyatı hesaplayan program yapalım
    
package kdvhesabı;
import java.util.Scanner;
public class Kdvhesabı{
    public static void main (String[]args){
    Scanner input=new Scanner(System.in);
 
    double urun,kdvorani,kdvliurun;
    System.out.println("ürünün ücretini giriniz:");
    urun=input.nextDouble();
    System.out.println("kdv oranını giriniz:");
    kdvorani=input.nextDouble();
    kdvliurun=urun+urun*kdvorani/100;
    System.out.println("ürünün yeni fiyatı:"+kdvliurun);
           
    
    }
    
}




         örnek3
        
        kullanıcıdan alınan yarıçapa göre 
        dairenin alanını ve çevresini hesaplayan program yapalım
        


package dairealaniveçevresi;
import java.util.Scanner;
public class Dairealaniveçevresi{
    public static void main(String[]args){
  
 Scanner input=new Scanner(System.in);
 double pisayisi=3.14,r,alan,çevre;
 System.out.println("yariçapi giriniz:");
 r=input.nextDouble();
 alan=pisayisi*r*r;
 çevre=2*pisayisi*r;
 System.out.println("dairenin alani:"+alan);
 System.out.println("dairenin çevresi:"+çevre);
 

        
    }
}


          örnek4
         hesap makinesi yapalım
         
         package hesapmakinesi;
import java.util.Scanner;
public class Hesapmakinesi{
    public static void main(String[]args){
      
        Scanner input=new Scanner(System.in);
        int sayi1,sayi2,secim;
        System.out.print("sayi1 i giriniz:");
        sayi1=input.nextInt();
        System.out.print("sayi2 i giriniz:");
        sayi2=input.nextInt();
        
System.out.println("lütfen işlem seçiniz:");
System.out.println("1-toplam\n2-çıkarma\n3-çarpma\n4-bölme");
        System.out.println("seçiminiz:");
        secim=input.nextInt();
  if(secim==1){
      System.out.println("toplam:"+(sayi1+sayi2));
  }else if(secim==2){
      System.out.println("çıkarma:"+(sayi1-sayi2));
  }else if(secim==3){
      System.out.println("çarpma:"+(sayi1*sayi2));
  }else if(secim==4){
      if (sayi2==0){
          System.out.println("belirsiz sonuç");
      }else{
      System.out.println("bölme:"+(sayi1/sayi2));
  }
  }else{
              System.out.println("geçersiz işlem");
              }
  
    
  }
    
    }
    
    
    
   örnek5

girilen kullanıcı adı ve şifre doğruysa sırasıyla fen,matematik,sosyal ve
türkçe notlarını kullanıcıdan alıp notlara göre ortalamayı hesaplayan
ortalama değeri 50 den küçükse ekrana "kaldınız" yazdıran
 ortalama değeri  50 ye eşit ve 50 den büyükse ekrana "geçtiniz" yazdıran
ortalama değeri 70 den küçükse "herhangi bir belge alamıyorsunuz!" yazdıran
ortalama değeri 70 e eşit ve 85 den küçükse ekrana "teşekkür belgesi almaya hak kazandınız!" yazdıran
ortalama değeri 85 e eşit ve 85 den büyükse ekrana "tebrikler takdir belgesi almaya hak kazandınız!" yazdıran
 programın java kodunu yazalım.


package login;
import java.util.Scanner;
public class Login{
public static void main(String[]args){
Scanner input=new Scanner(System.in);

    String kullaniciadi,şifre;
    System.out.print("lütfen kullanıcı adınızı giriniz:");
    kullaniciadi=input.nextLine();
    System.out.print("lütfen şifrenizi giriniz:");
    şifre=input.nextLine();
    
    if(kullaniciadi.equals("gulcin")&&şifre.equals("isidogru")){
       System.out.println("hoşgeldiniz");
    double fen,matematik,sosyal,türkçe,ortalama;
    System.out.println("ortalamanızı hesaplamak için lütfen notlarınızı sırası fen,"
            + "matematik,sosyal ve türkçe olacak şekilde giriniz!");
    
    System.out.println("fen:"+(fen=input.nextDouble()));
    
    System.out.println("matematik:"+(matematik=input.nextDouble()));
    
    System.out.println("sosyal:"+(sosyal=input.nextDouble()));
    
    System.out.println("türkçe:"+(türkçe=input.nextDouble()));  
    
    ortalama=(fen+matematik+sosyal+türkçe)/4;
    System.out.println("ortalamanız:"+ortalama);
    
    if(ortalama<50){
        System.out.println("kaldınız");
    }
    else{
        System.out.println("geçtiniz");
        
    }
    
    if(ortalama<70){
        System.out.println("herhangi bir belge alamıyorsunuz!");
    }else if(ortalama<85){
        System.out.println("teşekkür belgesi almaya hak kazandınız!");
    }else if(ortalama>=85){
        System.out.println("tebrikler takdir belgesi almaya hak kazandınız!");
    }
      
      
       
       
    }else{
       System.out.println("kullanıcı adınız veya parolanız yanlış!");
    }
    

      
    }
}




         örnek6
        
        km birim fiyatı 0.10 olan
        12 yaşından küçükse toplam fiyata %50 indirim,
        12 ve 24 yaş arasındaysa %10 indirim,
        65 yaşından büyükse %30 indirim,
        gidiş-dönüş alırsa %20 indirim yapan
        yukardaki koşullara bağlı olarak uçak bileti fiyatı hesaplayan programı yapalım.

package uçakbiletfiyatihesabi;
import java.util.Scanner;
public class Uçakbiletfiyatihesabi{
    public static void main(String[]args){
        Scanner input=new Scanner(System.in);
    
     double km,biletfiyati;   
     int yaş,tip;
     System.out.println("mesafeyi km cinsinden giriniz:");
     km=input.nextDouble();
     System.out.println("yaşınızı giriniz:");
     yaş=input.nextInt();
     System.out.println("yolculuk tipini seçerken 1 e basmanız sadece gidişi\n"
             + "temsil ederken 2 ye basmanız hem gidişi hem de dönüşü \n"
             + "temsil etmektedir!!!");
     System.out.println("yolculuk tipini  seçiniz:");
     tip=input.nextInt();
       if(tip==1){
           System.out.println("sadece gidiş tipini seçtiniz");
       }else if(tip==2){
           System.out.println("hem gidiş hem dönüş tipini seçtiniz");
       }else{
           System.out.println("geçersiz seçim yaptınız!");
       }
       
       
       
       if(km>0&&yaş>0&&(tip==1||tip==2)){
           System.out.println("girdiler doğru");
       }else{
           System.out.println("girdiler yanlış");
       }     
       
       
       if((yaş<=12)&&(tip==1)){
           biletfiyati=(km*0.1)/2;
           System.out.println("tutar:"+biletfiyati);
       }else if((yaş<=12)&&(tip==2)){
           biletfiyati=(km*0.1*0.8);
           System.out.println("tutar:"+biletfiyati);
       }else if((yaş<=24)&&(tip==1)){
           biletfiyati=(km*0.1*0.9);
           System.out.println("tutar:"+biletfiyati);
       }else if((yaş<=24)&&(tip==2)){
           biletfiyati=(km*0.1*0.9*2*0.8);
           System.out.println("tutar:"+biletfiyati);   
       }else if((yaş<65)&&(tip==1)){
           biletfiyati=(km*0.1);
           System.out.println("tutar:"+biletfiyati); 
       }else if((yaş<65)&&(tip==2)){
           biletfiyati=(km*0.1*0.8*2);
           System.out.println("tutar:"+biletfiyati); 
       }else if((yaş>65)&&(tip==1)){
           biletfiyati=(km*0.1*0.7);
           System.out.println("tutar:"+biletfiyati);     
       }else if((yaş>65)&&(tip==2)){
           biletfiyati=(km*0.1*07*2*0.8);
           System.out.println("tutar:"+biletfiyati);
       }    
             

        
        
    }
}


       örnek7
        
        
      hava sıcaklığını kullanıcıdan alarak
      sıcaklık 30 ve 30dan fazlaysa yüzme öneren
      sıcaklık 5 den büyük ve 5 e eşit ayrıca 30 dan küçükse sinema öneren
      sıcaklık 4 ve daha az ise kayak öneren
      uygulamanın java kodunu yazalım

 package etkinlikönerenprogram;
import java.util.Scanner;
public class Etkinlikönerenprogram{
    public static void main(String[]args){
        Scanner input=new Scanner(System.in);
     
      double sicaklik;
      System.out.print("lütfen sıcaklık değerini giriniz:");
      sicaklik=input.nextDouble();
      
      if (sicaklik>=30){
          System.out.println("yüzmeye gidebilirsiniz");    
      }else if(sicaklik>=5 && sicaklik<30){
       System.out.println("sinema sizin için iyi bir seçenek gibi "
               + "duruyor");
      }else if(sicaklik<=4){
          System.out.println("kayağa gidebilirsiniz");
      } 
        
   
        
    }
}




        örnek8
        
       negatif bir değer girilene kadar kullanıcıdan girişleri
       kabul edilen ve girilen değerlerden tek sayıları toplayan programın java kodunu yazalım

package whileörn2;
import java.util.Scanner;
public class Whileörn2{
    public static void main(String[]args){
        Scanner input=new Scanner(System.in);
      
        int i;
        int toplam=0;
        
        while(true){
          System.out.print("sayı giriniz:");
          i=input.nextInt();
          if(i<0){
              System.out.println("negatif sayı girdiniz");
              break;}
          
         if(i%2==1){
             toplam=toplam+i;
             System.out.println("toplam:"+toplam);
         }
          
          
        }
 
        
    }
} 


        örnek9
        
      girilen sayıya kadar olan 2 nin kuvvetleri yazdıran programın java kodunu yazalım
      
  package whileörn3;
import java.util.Scanner;
public class Whileörn3{
    public static void main(String[]args){
        Scanner input=new Scanner(System.in);
     
      System.out.print("sayı giriniz:");
      int i=input.nextInt();
      int k=1;
      while(k<=i){
          System.out.println(k);
          k=k*2;
      }
        
        
    }
}    
  
        örnek 10
        
        kullanıcıdan girilen sayının harmonik değerini hesaplayan programın java kodunu yazalım
        
        package harmoniksayi;
import java.util.Scanner;
public class Harmoniksayi{
    public static void main(String[]args){
        Scanner input=new Scanner(System.in);
       
         double sonuc=0;
         System.out.println("sayı giriniz:");
         
         double i=input.nextDouble();
         while(i>0){
             sonuc=sonuc+(1/i);
             i--;
         }
         System.out.println("sonuç:"+sonuc);
    
        
    }
}
        
        
