# Kullanici_sifre
Kullanıcıdan alınan şifrenin doğru olup olmadığını kontrol eden program

import java.util.Scanner;
public class sifrepatika {
    public static void main(String[] args){
        Scanner input= new Scanner(System.in);
        System.out.println("Kullanıcı adınız: ");
        String username = input.nextLine();
        System.out.println("Şifreniz: ");
        String password = input.nextLine();

        if(username.equals("Kodluyoruz")){
            if(password.equals("Java123")){
                System.out.println("Giriş başarılı!");
            }
            else {
                System.out.println("Giriş başarısız!\nŞifrenizi sıfırlamak ister misiniz?");
                String cevap=input.nextLine();
                if(cevap.equalsIgnoreCase("evet")){
                    System.out.println("Yeni şifrenizi girin: ");
                    String new_password= input.nextLine();
                    if(!(password.equals(new_password)))
                        System.out.println("Gişir yapıldı.");
                    else
                        System.out.println("Şifreniz aynı, değiştirmeniz gerek.");
                }
            }

        }
    }
}
