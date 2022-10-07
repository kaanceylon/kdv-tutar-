# kdv-tutar-
KDV TUTARI HESAPLAMA PROGRAMI

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
      double tutar, kdvOran = 0.18, kdvTutar, kdvliTutar;
      boolean kdvDurum;
      Scanner input = new Scanner(System.in);
      System.out.print("Ücret Tutarını Giriniz : ");
      tutar = input.nextDouble();

      kdvTutar = tutar * kdvOran;
      kdvliTutar = tutar + kdvTutar;

      kdvDurum = (0 < tutar ) && ( 1000 > tutar );
      kdvOran = kdvDurum ? 0.18 : 0.8;

      System.out.println("KDV'siz Tutar :" + tutar);
      System.out.println("KDV'li Tutar :" + kdvliTutar);
      System.out.println("kdv Oranı :" + kdvOran);
      System.out.println("KDV Tutar :" + kdvTutar);


    }
}
