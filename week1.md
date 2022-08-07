## Week 1

- [JVM nedir, ne işe yarar?](#jvm-nedir-ne-işe-yarar)
- [JDK nedir, ne işe yarar?](#jdk-nedir-ne-işe-yarar)
- [Garbage Collector'ın görevi nedir, nasıl çalışır?](#garbage-collectorın-görevi-nedir-nasıl-çalışır)
- [.jar formatı nedir?](#jar-formatı-nedir)
- [Javada .class ve .java formatının farkı nedir?](#javada-class-ve-java-formatının-farkı-nedir)
- [Abstract class nedir, nasıl çalışır, ne işe yarar?](#abstract-class-nedir-nasıl-çalışır-ne-işe-yarar)

___

### JVM nedir, ne işe yarar?
**JVM (Java Virtual Machine)**, 
- Java dilinin en önemli özelliği olan bir kere yaz her yerde çalıştır mantığını sağlayan mekanizmadır. 
- Java kodları hemen hemen tüm platformlar üzerinde çalışabilir.
- Java kodları .java uzantılı dosyalara yazılır. Daha sonra bu dosya compile edilerek byte koda dönüştürülür. 
- Bu byte kodlar .class uzantılı dosyalara yazılır. Daha sonra bu byte kodlar JVM üzerinde çalıştırılır ve sistemin anlayacağı şekle dönüştürülür.
 
<img src="https://3.bp.blogspot.com/-9-PtVzGOrEE/XG2pPuyK2MI/AAAAAAAACt4/WzUL37YxtbcopA6PYaUWVhsmxHMWchXPQCLcBGAs/s400/getStarted-compiler.gif" width="400" height="93"/>

- Özetle JVM, sistemin üzerinde çalışarak Java kodlarının her sistemde çalışabilmesini sağlar. 
- Bunu yapabilmesi için her sisteme özel bir JVM olması gerekir. 
- Sistemin Java kodu ile uygun bir şekilde çalışabilmesi için gerekli düzenlemeleri JVM yapar. 
- Bizim yapmamız gereken tek şey Java kodunun çalışacağı makineye uygun JVM'yi yüklemek ve kodumuzu derlemektir.

![alt text](https://4.bp.blogspot.com/-vTqyF7UgP9I/XG2pPpfkRUI/AAAAAAAACuE/7XxYXLoXzQAk_aiwZNiTHzMhy_zjCv4uwCEwYBhgL/s400/helloWorld.gif")

___

### JDK nedir, ne işe yarar?
**JDK (Java Deveplopment Kit)**
- JDK, Java uygulamaları geliştirmek için gerekli tüm araçları bize sağlar.
- İçerisinde JVM, JRE, Java kütüphaneleri, Java Compiler ve Interpreter içerir.
- Bir java uygulaması geliştirmek için JDK yüklememiz yeterlidir çünkü diğer araçları JDK içirisinde barındırır.


![alt text](https://3.bp.blogspot.com/-FJlgPrqlK_U/XG2thrIIx-I…_7WlvF4WLXUMgaksvswCLcBGAs/s640/javagenelyapi.jpg)


___

### Garbage Collector'ın görevi nedir, nasıl çalışır?
**Garbage Collector 'ın Görevi**
- Java'da Garbage Collector, Java programlarının otomatik bellek yönetimini gerçekleştirme işelmidir. 
- Otomatik çöp toplama; yığın belleğe bakma, hangi nesnelerin kullanımda olduğunu ve hangilerinin kullanılmadığını belirleme ve kullanılmayan nesneleri silme işlemidir.
- Garbage Collector'ın temel amacı,  artık kullanılmayan tüm nesneleri yok ederek yığın belleğini boşaltmaktır. 
-  Garbage Collector uygulaması JVM'de yaşar.

**Garbage Collector Nasıl Çalışır**

```java
public class Main {
	public static void main(String[] args) {
	    Integer a = new Integer(5);	
	}
}
```
- Program “new” operatörünü çalıştırdığı zaman “heap” belleğe gider ve bellekte yeterli bir yer olup olmadığına kontrol eder. Yeterli alan varsa referans, bellekteki bu yeri gösterir, nesnenin yapılandırıcı metodu çalışır.

Peki bellekte yeterli alan yoksa ne olur ?

“Garbage Collector” devreye girer ve uygulamanın ihtiyaç duymadığı tüm objeler belleğin heap bölgesinden temizlenir.

Özetle; “new” anahtar kelimesi ile nesne oluşturuldu, uygulama heap belleğe gitti ve yer olmadığını anladı. Garbage Collector devreye girdi ve gerekli alan tahsis(allocated) edildi.
___

### .jar formatı nedir?
- JAR dosya uzantısı Java arşivleri için kullanılır.
- Java Arşivi (JAR) dosya biçimi, birden çok dosyayı tek bir arşiv dosyasında birleştirmenize olanak tanır. 
- Tipik olarak bir JAR dosyası, uygulamalar ve uygulamalarla ilişkili sınıf dosyalarını ve yardımcı kaynakları içerir.
- JAR dosyaları JDK kurulumu içerisinde yer alan ‘bin’ klasörü içerisindeki ‘jar utility’ ile oluşturulabilir. JAR dosyası, ZIP, RAR gibi bir sıkıştırılmış dosyadır
___

### Javada .class ve .java formatının farkı nedir?
- Java dilinde yazdığımız programlar derlendiğinde .class uzantılı dosyalara dönüşür.
- Class dosyaları kısaca yazdığımız .java uzantılı Java sınıflarının java derleyicisi tarafından derlenmesi sonucu oluşan ve içeriğini JVM'in anlayıp yorumlayabildiği dosyalardır. Bu dosyaların içinde JVM için tanımlanmış bir takım bilgiler ve aynı zamanda JVM’nin çalıştırdığı bytecode’lar yer alır. Bytecode JVM’nin çalıştırdığı özel komutlara verilen addır ve class dosyasının içinde belli bölümlerde yer almaktadırlar. 
___

### Abstract class nedir, nasıl çalışır, ne işe yarar?
- Ortak özellikleri olan nesneleri modellemek için Java dilinde abstract(soyut) sınıflar kullanır.
- Soyut sınıflar oluşturulurken class ismi yerine “abstract class” kelimeleri kullanılır.
- Soyut sınıflar kalıtım özelliğini kullanarak kod tekrarını azaltır.
- Soyut sınıflar kendisinden türeyen sınıflardır.Bu sınıflardan nesne oluşturamayız.
- Erişim belirleyiciler ( public, private… ) kullanılabilir.

Abstract classlarda neler olmaz?

- Abstract classların içerisindeki soyut metotların gövdesi boş olması gerekir(Kullanılacak yere göre işlem farklılığı olacağından.)Ama soyut olmayan metotların gövdeleri olmak zorundadır.
- Abstract classlar private olarak tanımlanamazlar.Çünkü kalıtım özelliğini her daim göstermek zorundadır(Zaten soyut sınıfların sihri bu).


Abstract classlar neden kullanılır?

- Bazı durumlarda oluşturacağımız tasarımda benzer özellikler taşıyan sınıflara rastlayabiliriz.Bu sınıflarda tekrar tekrar aynı kodları yazmaktansa soyut sınıfları kullanmak daha kolaylık sağlıyor(kodun yeniden kullanılabilirliği).
- Genelde metotları sonradan geliştirilmek için kullanılır.


Abstract classlar nasıl kullanılır?

```java
Public abstract class Ders
{		
	private String ad;
	public int sinifNo = 1;
	public abstract String getAd();

	public int  getsinifNo()
	{
		return this.sinifNo;
	}
}
```
- Burada getAd() isminde soyut metot ve getsinifNo() isminde normal bir metot bulunmaktadır.
- getAd() metodu soyut olduğundan dolayı bu abstractı extend eden alt sınıflar bu metodu implemente etmek zorundadır.



```java
Public class Matematik extends Ders
{
	public String getAd()
	{
		return “Matematik”;
	}

	public int getsinifNo()
	{
		return super.getsinifNo();
	}
}
```
- getsinifNo() metodu üst sınıfta(abstract) tanımlanmaktadır.Bu metot değiştirilerek (re-implemente) yada olduğu gibi kullanılabilir.


```java
Public class Fizik extends Ders
{
	Ders ders = new Ders();
	ders.sinifNo = 2;
	public String getAd()
	{
		return “Fizik”;
	}
	public int getsinifNo()
	{
		return getsinifNo();
	}
}
```
- Özet olarak getAd() soyut olarak tanımlandığı için alt sınıfların hepsinde getAd() isminde implementasyonu yapılmış sınıf olarak kullanılmak zorundadır.getsinifNo() ise normal metot olarak belirtildiğinden dolayı diğer sınıflarda kendilerine özgü kullanılabilir yada abstract sınıfta belirtildiği şekilde kullanılabilirler.












