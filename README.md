# Sınıfı Gecme Durumu
Patika.dev > Java101 > Koşullu İfadeler ve Kod Blokları > Pratik3 - Sınıfı Geçme Durumu

## Eğer girilen ders notları 0 veya 100 arasında değilse ortalamaya katılmasın.
- Dersler: Matematik, Fizik, Türkçe, Kimya, Müzik
- Geçme Notu: 55

		import java.util.*;
		
		public class sinifiGecme {

			public static void main(String[] args) {
				// Yeni bir tarayıcı(scanner) oluştur.
				Scanner sc= new Scanner(System.in);
		
				// Kullanıcıdan not değerlerini al.
				System.out.println("Matematik notunuz: ");
				int mat =sc.nextInt();
		
				System.out.println("Fizik notunuz: ");
				int fizik =sc.nextInt();
		
				System.out.println("Türkçe notunuz: ");
				int turkce =sc.nextInt();

				System.out.println("Kimya notunuz: ");
				int kimya =sc.nextInt();
		
				System.out.println("Müzik notunuz: ");
				int muzik =sc.nextInt();
		
				// Ortalama koşullarını oluştur.
				double ortalama, toplam = 0;
				int n = 0;
				if (mat > 0 && mat <= 100) {
					toplam = toplam + mat;
					n++;
				}
        			
				if (fizik > 0 && fizik <= 100) {
					toplam = toplam + fizik;
					n++;
				}
				
				if (turkce > 0 && turkce <= 100) {
					toplam = toplam + turkce;
					n++;
				}
				
				if (kimya > 0 && kimya <= 100) {
					toplam = toplam + kimya;
					n++;
				}
				
				if (muzik > 0 && muzik <= 100) {
					toplam = toplam + muzik;
					n++;
				}
        		
				ortalama = toplam / n;
		
				if (ortalama > 55)
					System.out.println("Ortalamanız: " + ortalama + "\nSınıfı geçtiniz. Tebrikler!");
				else
					System.out.println("Ortalamanız: " + ortalama + "\nSınıfta kaldınız. Seneye tekrar görüşmek üzere!");
			}
		}
