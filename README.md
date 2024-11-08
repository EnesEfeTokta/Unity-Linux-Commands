![unity](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/LinuxCommandForUnity.png "Unity Linux")

# Unity Geliştiricileri İçin Kullanışlı Linux Komutları

## Amaç
Bu dokümanın amacı, Unity geliştiricilerine yönelik olarak Linux işletim sisteminde sıkça kullanılan ve geliştirme sürecini optimize edebilecek komutları kapsamlı bir şekilde sunmaktır. Bu kaynak, geliştiricilerin proje yönetimi, performans izleme ve sistem yapılandırması gibi alanlarda verimliliklerini artırmalarına yardımcı olmayı hedeflemektedir.

Not: Bu döküman yapılırken Linux dağıtımlardan LinuxMint 20.1 yüklü olduğunu varsayıyoruz.

## `cd` Komutu
`cd` (change directory) komutu, terminalde çalışırken dizinler arasında geçiş yapmamızı sağlar. Bu komut, dosya sisteminde gezinmek için temel bir araçtır ve aşağıdaki şekillerde kullanılabilir:

* `cd klasör_adi`: Belirtilen klasöre geçiş yapar. Örneğin, `/home` dizinine geçmek için:
    ```Bash
    cd /home
    ```
    ![cd_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cd.png "cd Komutu")

* `cd ..`: Bir üst dizine geçiş yapar. Bu, mevcut dizinin bir üst seviyesine çıkmak için kullanılır.
    ```Bash
    cd ..
    ```
    ![cd_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cd_pointpoint.png "cd .. Komutu")

* `cd .`: Bulunduğunuz dizinde kalır. Bu komut genellikle etkisizdir çünkü mevcut dizini değiştirmez.
    ```Bash
    cd .
    ```
    ![cd_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cd_point.png "cd . Komutu")

* `cd ~`: Kullanıcının ana dizinine (home directory) geçiş yapar. Bu, kullanıcıların kişisel dosyalarına hızlıca erişmesini sağlar.
    ```Bash
    cd ~
    ``` 
    ![cd_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cd_wave.png "cd ~ Komutu")

* `cd /`: Kök dizine (root directory) geçiş yapar. Bu, dosya sisteminin en üst seviyesine erişmek için kullanılır.
    ```Bash
    cd /
    ```
    ![cd_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cd_slash.png "cd / Komutu")

`cd` komutu, dosya sisteminde hızlı ve etkili bir şekilde gezinmek için vazgeçilmezdir. Özellikle karmaşık dizin yapılarında çalışırken, doğru dizine hızlıca geçiş yapmak için bu komutun farklı varyasyonlarını kullanabilirsiniz.

## `ls` Komutu
`ls` (list) komutu, bir dizinin içeriğini listelemek için kullanılan temel bir Linux komutudur. Unity projelerinizde dosya ve klasör yönetimi için oldukça faydalıdır. `ls` komutu, dosya ve dizinlerin adlarını, izinlerini, sahiplerini ve diğer bilgilerini görüntülemek için çeşitli seçeneklerle kullanılabilir. İşte `ls` komutunun bazı yaygın ve faydalı kullanımları:

* `ls`: Temel kullanım. Mevcut dizindeki dosya ve klasörleri listeler. Bu, hızlı bir şekilde dizin içeriğini görmek için kullanılır.
    ```Bash	
    ls
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls.png "ls Komutu")

* `ls -l`: Uzun format. Dosya ve klasörleri ayrıntılı bilgilerle (izinler, sahibi, boyut, değiştirilme tarihi) listeler. Bu, dosya izinlerini ve diğer meta bilgileri görmek için kullanışlıdır.
    ```Bash	
    ls -l
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_l.png "ls -l Komutu")

* `ls -a`: Gizli dosyaları da gösterir. Unity'de `.meta` dosyaları gibi gizli dosyaları görüntülemek için kullanışlıdır. Gizli dosyalar, genellikle bir nokta (.) ile başlar.
    ```Bash
    ls -a
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_a.png "ls -a Komutu")

* `ls -la` veya `ls -al`: Uzun format ve gizli dosyaları birleştirir. Tüm dosyaları ayrıntılı bilgilerle listeler. Bu, dizindeki tüm dosyaların tam bir görünümünü sağlar.
    ```Bash	
    ls -la
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_l_a.png "ls -la Komutu")

* `ls -lh`: Dosya boyutlarını insan okunabilir formatta (KB, MB, GB) gösterir. Bu, dosya boyutlarını daha anlaşılır bir şekilde görmek için kullanılır.
    ```Bash
    ls -lh
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_l_h.png "ls -lh Komutu")

* `ls -R`: Alt dizinleri de içerecek şekilde tüm içeriği recursive olarak listeler. Büyük Unity projelerinde dikkatli kullanın, çünkü çok fazla çıktı üretebilir.
    ```Bash
    ls -R
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_r.png "ls -R Komutu")

* `ls -t`: Dosyaları değiştirilme tarihine göre sıralar (en yeni en üstte). Bu, en son değiştirilen dosyaları hızlıca bulmak için kullanışlıdır.
    ```Bash	
    ls -t
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_t.png "ls -t Komutu")

* `ls -S`: Dosyaları boyuta göre sıralar (en büyük en üstte). Bu, büyük dosyaları hızlıca bulmak için kullanışlıdır.
    ```Bash
    ls -S
    ```
    ![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_s.png "ls -S Komutu")

### Unity Projeleri İçin Özellikle Faydalı Kullanımlar:
* `ls Assets/`: Assets klasörünün içeriğini listeler. Bu, Unity projenizin ana kaynak dizinini hızlıca incelemek için kullanılır.
* `ls -R *.unity`: Tüm Unity sahne dosyalarını recursive olarak bulur. Bu, projedeki tüm sahneleri listelemek için kullanışlıdır.
* `ls -lh *.asset`: Tüm asset dosyalarını boyutlarıyla birlikte listeler. Bu, hangi asset dosyalarının daha fazla yer kapladığını görmek için kullanışlıdır.

Not: `ls` komutunu farklı seçeneklerle kombine edebilirsiniz. Örneğin, `ls -lhrt` en son değiştirilen dosyaları okunabilir boyutlarıyla birlikte listeler. Bu, dosya yönetimini daha etkili hale getirir.

## `pwd` Komutu
`pwd` komutu, bulunduğumuz dizini gösterir. Bu komut, Unity projelerinde klasörler arasında geçiş yapmak için kullanışlıdır. `pwd` komutunun işlevleri şu şekildedir:

* `pwd`: Bulunduğumuz dizini gösterir.
    ```Bash
    pwd 
    ```
    ![pwd_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/pwd.png "pwd Komut")

* `pwd -P`: Dizinlerin tam adını gösterir.
    ```Bash
    pwd -P
    ```
    ![pwd_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/pwd_point.png "pwd -P Komut")

## `cp` Komutu
`cp` komutu, bir dosya veya klasörü başka bir yere kopyalamak için kullanılır. `cp` komutunun işlevi şu şekildedir:
* `cp dosya_adi yeni_yol`: Dosyayı başka bir yere kopyalar.
    ```Bash
    cp dosya_adi yeni_yol
    ```
    ![cp_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cp.png "cp Komutu")

* `cp -r klasör_adi yeni_yol`: Dosya ve alt klasörleri içindeki tüm içeriği kopyalar.
    ```Bash    
    cp -r klasör_adi yeni_yol
    ```
    ![cp_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cp_r.png "cp -r Komutu")

## `mv` Komutu
`mv` komutu, bir dosya veya klasörü başka bir yere taşımak için kullanılır. `mv` komutunun işlevi şu şekildedir:
* `mv dosya_adi yeni_yol`: Dosyayı başka bir yere taşımak için kullanılır.
    ```Bash
    mv dosya_adi yeni_yol
    ```
    ![mv_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/mv.png "mv Komutu")

* `mv -r klasör_adi yeni_yol`: Dosya ve alt klasörleri içindeki tüm içeriği taşımak için kullanılır.
    ```Bash
    mv -r klasör_adi yeni_yol
    ```
    ![mv_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/mv_r.png "mv -r Komutu")

## `rm` Komutu
`rm` komutu, bir dosya veya klasörü silmek için kullanılır. `rm` komutunun işlevi şu şekildedir:
* `rm dosya_adi`: Dosyayı silmek için kullanılır.
    ```Bash
    rm dosya_adi
    ```
    ![rm_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/rm.png "rm Komutu")

* `rm -r klasor_adi`: Klasörü silmek için kullanılır.
    ```Bash
    rm -r klasor_adi
    ```
    ![rm_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/rm_r.png "rm -r Komutu")

## `mkdir` Komutu
`mkdir` komutu, bir yeni klasör oluşturmak için kullanılır. `mkdir` komutunun işlevi şu şekildedir:
* `mkdir klasor_adi`: Yeni bir klasör oluşturur.
    ```Bash
    mkdir klasor_adi
    ```
    ![mkdir_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/mkdir.png "mkdir Komut")

* `mkdir -p klasor_adi/klasor_adi`: Yeni klasörü oluşturur ve onun içindeki alt klasörleri de oluşturur.
    ```Bash
    mkdir -p klasor_adi/klasor_adi
    ```
    ![mkdir_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/mkdir_point.png "mkdir -p Komut")

## `touch` Komutu
`touch` komutu, bir dosya oluşturmak için kullanılır. `touch` komutunun işlevi şu şekildedir:
* `touch dosya_adi`: Yeni bir dosya oluşturur.
    ```Bash
    touch dosya_adi
    ```
    ![touch_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/touch.png "touch Komutu")

* `touch -a dosya_adi`: Dosyanın son değiştirilme tarihini günceller.
    ```Bash
    touch -a dosya_adi
    ```
    ![touch_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/touch_a.png "touch -a Komutu")

## `ip` Komutu
`ip` komutu, bilgisayarın IP adresini gösterir.
```Bash
ip a
```
![ip_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ip.png "ip Komutu")

## `grep` Komutu
`grep` komutu, bir dosyadaki belirli bir kelimeyi aramak için kullanılır. `grep` komutunun işlevi şu şekildedir:
* `grep -R kelime dosya_adi`: Dosyadaki tüm kelimeleri bulur.
    ```Bash
    grep -R kelime dosya_adi
    ```
    ![grep_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/grep_r.png "grep Komutu")

* `grep -R -i kelime dosya_adi`: Büyük küçük harf duyarlılığıyla kelimeleri bulur.
    ```Bash
    grep -R -i kelime dosya_adi
    ```
    ![grep_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/grep_r_i.png "grep -i Komutu")

## `cat` Komutu
`cat` komutu, bir dosyayı okumak için kullanılır. `cat` komutunun işlevi şu şekildedir:
* `cat dosya_adi`: Dosyayı okumak için kullanılır.
    ```Bash
    cat dosya_adi
    ```
    ![cat_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cat.png "cat Komutu")

* `cat -n dosya_adi`: Dosyayı okumak için kullanılır ve her satıra bir numara verir.
    ```Bash
    cat -n dosya_adi
    ```
    ![cat_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/cat_n.png "cat -n Komutu")

## `ps` Komutu
`ps` komutu, bilgisayardaki oturumların listesini gösterir. `ps` komutunun işlevi şu şekildedir:
* `ps`: Bilgisayardaki oturumların listesini gösterir.
    ```Bash
    ps
    ```
    ![ps_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ps.png "ps Komutu")

* `ps aux`: Bilgisayardaki oturumların listesini gösterir ve süreçleri gösterir.
    ```Bash
    ps aux
    ```
    ![ps_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ps_aux.png "ps aux Komutu")

* `ps -u`: Bilgisayardaki oturumların list esini gösterir ve kullanıcı adını gösterir.
    ```Bash
    ps -u
    ```
    ![ps_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ps_u.png "ps -u Komutu")

* `ps -u -e`: Bilgisayardaki oturumların listesini gösterir ve kullanıcı adını gösterir. 
    ```Bash
    ps -u -e
    ```
    ![ps_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ps_u_e.png "ps -ue Komutu")

## `ls -R --color=auto` Komutu
`ls -R --color=auto` komutu, klasörlerdeki dosyaları ve alt klasörleri gösterir. `ls -R --color=auto` komutunun işlevi şu şekildedir:
```Bash
ls -R --color=auto
```
![ls_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/ls_R_color.png "ls -R --color=auto Komutu")

## `lsmod` Komutu
`lsmod` komutu, modüllerin listesini gösterir. `lsmod` komutunun işlevi şu şekildedir:
* `lsmod`: Modüllerin listesini gösterir.
    ```Bash
    lsmod
    ```
    ![lsmod_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/lsmod.png "lsmod Komutu")

* `modinfo modül_adi`: Modül hakkında daha fazla bilgi verir.
    ```Bash
    modinfo modül_adi
    ```
    ![lsmod_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/modinfo.png "modiinfo Komutu")

## `gzip` Komutu
`gzip` komutu, ilgili dosyayı sıkıştırarak zip dosyasına çeviriyor. `gzip` komutunun işlevi şu şekildedir:
```Bash
gzip dosya_adi
```
![gzip_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/gzip.png "gzip Komutu")

## `gunzip` Komutu
`gunzip` komutu, ilgili zip dosyasını açmak için kullanılır. `gunzip` komutunun işlevi şu şekildedir:
```Bash	
gunzip zip_dosya_adi
```
![gunzip_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/gunzip.png "gunzip komutu")

## `traceroute` Komutu
`traceroute` komutu, bir sunucuya yollayıp, bu sunucuya kadar gelmek için gerekli olan tüm noktaların IP adreslerini gösterir. `traceroute` komutunun işlevi şu şekildedir:
```Bash
traceroute sunucu_adi
```
![traceroute_komutu](https://github.com/EnesEfeTokta/Unity-Linux-Commands/blob/main/Images/traceroute.png "tracer Route Komutu")

## Proje Bilgileri
Bu doküman, Atatürk Üniversitesi Bilişim Sistemleri ve Teknolojileri Bölümü'nde yürütülen İşletim Sistemleri dersi kapsamında hazırlanmış bir akademik çalışmadır. Projenin geliştiricisi Enes Efe Tokta tarafından *6 Kasım 2024* ile *18 Kasım 2024* tarihleri arasında titizlikle hazırlanmış ve dersin ilk ara sınav ödevi olarak sunulmuştur.

Bu çalışma, Linux işletim sistemi komutlarını Unity geliştirme ortamı bağlamında incelemekte ve açıklamaktadır. Doküman, hem akademik hem de pratik amaçlara hizmet etmek üzere tasarlanmıştır.

© 2024 Enes Efe Tokta. Tüm hakları saklıdır. [LICENSE](https://github.com/EnesEfeTokta/Unity-Windows-Commands/blob/main/LICENSE "Click on LICENSE file.")