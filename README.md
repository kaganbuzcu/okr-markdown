# Okr
Svelte Framework üzerinde bilgi birikim sahibi olmak, mevcut front-end bilgisinin geliştirmesi, farklı teknolojiler ile ufku arttırmak gibi amaçlar ile localization uygulamalarında çeviri ve implementasyon işlemlerinin kolaylaştırılması için kullanılacak bir proje gerçekleştirimi yapılmak istenmektedir.

## Detaylar
Multilanguage çalışmalarında kullanılacak key-value setlerinin implementasyonunu kolaylaştırmak, Google Translate api ile çeviri yapan kişiye öneriler sunmak, ilgili sayfa için json veya csv dosya çıktısı oluşturmak gibi özellikler amaçlanmaktadır.
### UX
Sayfa içeriğindeki alanlar şu şekilde olacaktır:
- Dil çiftinin seçileceği alan
- Scope input'u
- Key input'u:
- İlk dil ve ikinci dil value input'ları
- İlk dil ve İkinci dil output input'ları
- message.js için Highlight çıktı alanı
- csv export alanı

### Akış
- Herhangi bir input'ta herhangi bir değişiklik olduğunda çıktı alanı da değişecektir.
- İlk dil value input'u dolu ise ve ikinci dil value input'u focus durumda ise Translate api'dan alınan sonuç öneri olarak sunulacak, "enter" tuşu ile birlikte öneri, input'un value'su olacaktır. 
- Kullanıcı isterse öneriyi düzenleyebilecektir. İkinci kez enter edildiğinde key value seti listede yerini alacak, input'lar temizlenecek ve key input'u focus durumuna gelecektir. 
- Kullanıcının yanlış giriş yapması ihtimaline karşı, obje görünümündeki liste üzerinden de düzenleme yapılabilecektir.
### Export
- Copy tuşları ile kullanıcı tüm listeyi kopyalabilir.
- Text'lerin -her iki dil için de- onaya sunulması amacıyla csv file export edilebilir.