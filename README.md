mport java.util.Scanner;
public class Segitiga
{
    public static void main(String[] args)
    {
        Scanner inp = new Scanner(System.in);
        while (true)
        {
            System.out.println("Menu Aplikasi Matematika:");
            System.out.println("1. Pertambahan\t2. pengurangan\3. Perkalian\t4. Pembagian");
            System.out.println("5. Sisa Bagi\t6. Keluar Aplikasi");
            System.out.println();

            System.out.print("Pilih Menu = ");
            int menu = inp.nextInt();

            if (menu > 6 || menu < 0)
            {
                System.out.println("Menu salah!");
                continue;
            }
            else if (menu == 6)
            {
                return;
            }

            System.out.print("Masukkan Angka Pertama = ");
            int noPertama = inp.nextInt();
            System.out.print("Masukkan Angka Kedua = ");
            int noKedua = inp.nextInt();

            int hasil = 0;
            String mode = "";

            switch (menu)
            {
                case 1:
                    hasil = noPertama + noKedua;
                    mode = "Pertama";
                    break;
                case 2:
                    hasil = noPertama - noKedua;
                    mode = "Pengurangan";
                    break;
                case 3:
                    hasil = noPertama * noKedua;
                    mode = "Perkalian";
                    break;
                case 4:
                    hasil = noPertama / noKedua;
                    mode = "Pembagian";
                    break;
                case 5:
                    hasil = noPertama % noKedua;
                    mode = "Sisa bagi";
                    break;
                case 6:
                    return;
            }

            System.out.println();

            System.out.print("Hasil " + mode + " antara " + noPertama + " dan " + noKedua + " adalah " + hasil);
            System.out.println();
        }
    }
}
