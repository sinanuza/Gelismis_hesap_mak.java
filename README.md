# Gelismis_hesap_mak.java
www.patika.dev



import java.util.Scanner;

public class Gelismis_Hesap_Makinesi {
    static int sum(int a,int b){
        int result=a+b;
        System.out.println("toplam: "+ result);
        return a+b;
    }
    static int minus(int a,int b){
        int result=a-b;
        System.out.println("fark :"+result);
        return a-b;
    }
    static int times(int a,int b){
        int result=a*b;
        System.out.println("Carpım : "+result);
        return a*b;
    }
    static int divided(int a,int b){
        if  (b==0){
            System.out.println("ikinci sayi sifirdan farkli olmali!!");

            return 0;
        }
        int result=a/b;
        System.out.println("bolum: "+ result);
        return a/b;
    }
    static int power(int a,int b) {
        int result = 1;
        for (int i = 1; i <= b; i++) {
            result *= a;

        }
        return result;
    }
    static int mod(int a, int b){
        return a%b;
    }
    static void rectangular(int a,int b){
        System.out.println("cevresi"+(2*a+2*b));
        System.out.println("Alani"+(a*b));
    }
    public static void main(String[] args) {
        Scanner scan =new Scanner(System.in);
        int select;
        String menu ="1-Toplama\n"
                + "2-Cikarma\n"
                +"3-Carpma\n"
                +"4-Bolme\n"
                +"5-Uslu Sayi\n"
                +"6-Mod Alma\n"
                +"7-Dikdortgen Alan Bulma\n"
                +"0-Cikis";
        System.out.println(menu);
        while (true){

            System.out.println("bir islem seciniz;");
            select =scan.nextInt();
            if (select==0) {
                break;
            }
                System.out.println("ilk sayiyi girin:");
                int a = scan.nextInt();
                System.out.println("ikinci sayiyi girin:");
                int b = scan.nextInt();

                switch (select) {
                    case 1:
                        sum(a, b);
                        break;
                    case 2:
                        minus(a,b);
                        break;
                    case 3:
                        times(a,b);
                        break;
                    case 4:
                        divided(a,b);
                        break;
                    case 5:
                        System.out.println("us alma: "+power(a,b));
                        break;
                    case 6:
                        System.out.println("mod islemi: "+mod(a,b));
                        break;
                    case 7:
                        rectangular(a,b);
                        break;
                }
        }
    }
}
