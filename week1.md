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

<img src="https://3.bp.blogspot.com/-9-PtVzGOrEE/XG2pPuyK2MI…hsmxHMWchXPQCLcBGAs/s1600/getStarted-compiler.gif"/>

___
