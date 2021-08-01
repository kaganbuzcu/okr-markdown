# Okr
Svelte Framework üzerinde bilgi birikim sahibi olmak, mevcut front-end bilgisinin geliştirmesi, farklı teknolojiler ile ufku arttırmak gibi amaçlar ile Shopify ve benzeri platformlardan satın alınan sanal ürünlerin kullanıma sunulacağı web tabanlı bir uygulama gerçekleştirimi yapılmak istenmektedir.
<br /><br />
Söz konusu projedeki satın alınan ürün bir e-dergi olabilir.

## Detaylar
Admin ve user olmak üzere iki tip kullanıcı vardır.
### Admin
- Kullanıcı ayarları:
    - Listeleme
    - Filtreleme
    - Aktifliği -pasif, aktif- değiştirme
    - Detay sayfası (Kullanıcının sahip olduğu ürünlerin görülebildiği sayfadır.)
- Ürün ayarları: 
    - Listeleme
    - Filtreleme
    - Aktifliği -pasif, aktif- değiştirme
    - Ekleme
    - Düzenleme
- Ürün match
    - Shopier üzerinde, ürünü satın alan kullanıcılar görülebilmektedir.
    - Hakediş ayarları bu sayfada yapılacaktır.
    - Kullanıcıların mail adresleri, ekleme sayfasındaki autocomplate input'a girilecek, kullanıcı var ise seçilecek yok ise e-posta adresinin tamamı yazıldıktan sonra ürün eşleştirme select'i üzerinde bir veya birden fazla ürün seçimi yapılabilecektir. Böylece kullanıcı daha önce kayıt olsa da olmasa da bu ekranda satın almayı gerçekleştiren mail adresi ile ürün eşleştirilmiş olacaktır.
    - Kullanıcının kayıt olma, giriş yapma ve ürüne ulaşma senaryosu, 
    [User](#User) tab'i altındadır.
### User
- Kullanıcı Shopier üzerinden sanal içeriği satın alır.
- Satın almayı gerçekleştiren kullanıcı e-posta adresleri sisteme girilebilmelidir.
- Girilen kullanıcı e-posta adresleri içerisinde sisteme kayıt olmamış -şifresi olmayan- kullanıcılar var ise kaydını tamamlamamış kullanıcı statüsünde tutulmalıdır.
    - Her bir e-posta hesabı için hash oluşturulur ve ilgili e-posta adresine bu hash’i barındıran bir url bilgisi iletilir.
    - Kullanıcı sisteme bu url ile giriş yapmaya çalışıyor ise ve oluşturulmuş bir şifresi yok ise şifre belirleme ekranına yönlendirilir.
    - Şifre oluşturma kuralları şu şekildedir:
    ```
        En az sekiz karakter ve en az bir harf ve sayı içermeli.
    ```
    - Şifresini oluşturan kullanıcı kayıt işlemini bitirmiştir ve ana sayfaya yönlendirilir.
- Kullanıcı şifresini daha önceden oluşturmuş -kayıt olmuş- ise giriş ekranına yönlendirilecektir.
- Giriş ekranında e-posta ve şifre girerek sisteme giriş yapabilecektir.
- Ana sayfada satın aldığı ürünlerin listesini görebilecektir.
- Listedeki ürüne tıklayarak detay sayfasına gidebilecektir.
- Detay sayfasında ürünün dergi görünümü yer alacaktır.

### FlipBook Plugins
Proje çıktısının anlamlı olması için aşağıdaki plugin'lerden birini satın alıp kullanabilirim.
* [Örnek 1](https://3dflipbook.net/)
* [Örnek 2](https://codecanyon.net/item/real3d-flipbook-jquery-plugin/4281720?irgwc=1&clickid=SfUza8QLbxyLUbHwUx0Mo3EtUkBwqlxZEXJl0M0&iradid=275988&irpid=1287877&iradtype=ONLINE_TRACKING_LINK&irmptype=mediapartner&mp_value1=&utm_campaign=af_impact_radius_1287877&utm_medium=affiliate&utm_source=impact_radius
)

### Back-end
Node.js ve postgresql ile basit bir web service yazabilirim.

### İhtiyaç duyulabilecek kaynaklar
* [Eğitim](https://www.udemy.com/course/sveltejs-the-complete-guide/)