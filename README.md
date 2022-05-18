# Console-Telefon-Rehberi-Uygulamas-
Telefon Numarası Kaydet
Telefon Numarası Sil
Telefon Numarası Güncelle
Rehber Listeleme (A-Z, Z-A seçimli)
Rehberde Arama
*************************************************************************************************************************************************************************
namespace TelefonRehberiUygulaması01
{
    internal class Program
    {
        static void Main(string[] args)
        {


            List<string> kullaniciListesi = new List<string>();


            while (true)
            {
                Console.WriteLine("Lütfen yapmak istediğiniz işlemi seçiniz:");
                Console.WriteLine("*****************************************");
                Console.WriteLine("(1)Yeni numara kaydetmek");
                Console.WriteLine("(2)Varolan numarayı silmek");
                Console.WriteLine("(3)Varolan numarayı güncelleme");
                Console.WriteLine("(4)Rehberi Listelemek");
                Console.WriteLine("(5)Rehberde arama yapmak");
                Console.WriteLine("Lütfen tuşlayınız:");

                string sayi = Console.ReadLine();

                
                    switch (sayi)
                    {
                        case "1":
                            Console.WriteLine("Lütfen isminizi giriniz:");
                                   string a =  Console.ReadLine();
                        kullaniciListesi.Add(a);

                            break;
                        case "2":
                            Console.WriteLine("Lütfen numarasını silmek istediğiniz kişinin adını ya da soyadını giriniz:");
                        string b = Console.ReadLine();

                        if (kullaniciListesi.Contains(b)) {
                         kullaniciListesi.Remove(b);
                        Console.WriteLine("İstediğiniz veri silinmiştir"); }
                        else
                        {
                            Console.WriteLine("Veri bulunamamıştır.");
                        }
                        break;
                        case "3":

                            Console.WriteLine("Güncellemek istediğiniz veriyi giriniz:");
                        Console.WriteLine("Yeni veriyi giriniz:");
                        string d = Console.ReadLine();
                        string e = Console.ReadLine();
                        if (kullaniciListesi.Contains(d))
                        {
                            kullaniciListesi.Remove(d);
                            kullaniciListesi.Add(e);
                            Console.WriteLine("Güncellenmiştir.",d);
                        }
                        else
                        {
                            Console.WriteLine("Bulunamamıştır..");
                        }
                            


                        
                        
                            break;
                        case "4":
                        Console.WriteLine("A-Z tanımlamak için bir'e / Z-A için 0 basınız:");

                         string sayi1=Console.ReadLine();
                        
                        if (sayi1 == "1")
                        {
                            kullaniciListesi.Sort();
                        }
                        else
                        {
                            kullaniciListesi.Reverse();

                        }

                        foreach (var item in kullaniciListesi)
                        {
                            Console.WriteLine(item);
                        }

                       break;

                       case "5":
                        Console.WriteLine("Rehberde aramak istediğiniz veriyi giriniz:");
                        string c = Console.ReadLine();
                        if (kullaniciListesi.Contains(c)) 
                        {
                            Console.WriteLine("{0} listede bulunmaktadır",c);
                        }
                        

                        break;


                       
                        
                            
                      
                       
                        
                           
                       
           
                    }

                
            }
        

        


            
           

          
        }
    }
}
