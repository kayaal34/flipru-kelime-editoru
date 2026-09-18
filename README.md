# Kelime Konsolu

FlipRU'nun `assets/data/words.json` dosyasını yönetmek için tamamen yerel çalışan tek dosyalık bir araç. Sunucu, kurulum, internet bağlantısı gerektirmez.

## Kullanım

1. `index.html`'i **Chrome ya da Edge**'de çift tıklayarak açın (Firefox/Safari'de dosyaya doğrudan yazma çalışmaz, bkz. aşağı).
2. **"Dosya aç"** ile FlipRU projesindeki `assets/data/words.json`'ı seçin.
3. Arama kutusu, seviye (A1–C1) ve tema filtreleriyle kelimeleri bulun.
4. Bir satırın ✏️ ikonuna tıklayıp düzenleyin, 🗑️ ile silin, **"Yeni kelime"** ile ekleyin.
5. İşiniz bitince **"Diske kaydet"** — değişiklik doğrudan 2. adımda seçtiğiniz dosyaya, yani projedeki `assets/data/words.json`'a yazılır. **Bu kadar. Başka bir dosya indirip kopyalamanız gerekmez** — kopyalamak, kaydedilen dosyanın üzerine yazıp değişiklikleri siler.
6. Kaydettikten sonra **"Kayıt geçmişi"** → "Değişiklikleri göster" ile neyin yazıldığını görebilirsiniz. Geri almanız gerekirse bu liste kaynaktır.
7. Değişiklikler, uygulama yeniden derlenip yeni sürüm yayınlanana kadar kullanıcılara yansımaz.

> 17 Eylül 2026'ya kadar her kayıttan sonra eski içerik `words_backup_...json` adıyla indiriliyordu. O dosya "yeni dosya" sanılıp words.json'ın yerine konunca 96 düzenleme kayboldu; yedek indirme bu yüzden kaldırıldı.

## Neler var

- **Arama + seviye/tema filtresi**
- **Bakım filtresi**: vurgu işareti eksik, transkripsiyon formatı bozuk, örnek cümlesi yok, temel alanı boş, olası kopya — üstteki özet şeridine tıklayarak da filtrelenebilir
- **Olası kopya tespiti**: aynı Rusça kelimenin (vurgu işareti fark etmeksizin) birden fazla kaydı varsa işaretler
- **Eskiyle karşılaştırma**: bir alanı değiştirdiğinizde düzenleme panelinde eski değeri üstü çizili gösterir
- **Bu oturumdaki değişiklikler** paneli: neyin değiştiğini/eklendiğini/silineceğini listeler, JSON çıktısını panoya kopyalar
- **Silinenler** paneli: diske kaydetmeden önce yanlışlıkla sildiğiniz bir kelimeyi geri alabilirsiniz
- **Kaydetmeden önce bütünlük kontrolü**: satır sayısı, alan sayısı, tekil id kontrolü ve JSON'un geçerliliği doğrulanmadan hiçbir şey diske yazılmaz

## Tarayıcı desteği

Doğrudan diske yazma (dosyayı açtığınız yere kaydetme) [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_API) gerektirir — bu Chrome ve Edge'de çalışır. Desteklemeyen bir tarayıcıda dosya yalnızca **indirilir**; onu elle proje klasörüne taşımanız gerekir.

## Kullanıcı bildirimleri

Uygulama içindeki "hatalı kelime bildir" özelliği şu an e-postaya düşüyor. Bu konsol o bildirimleri otomatik çekmiyor — bildirimleri okuyup ilgili kelimeyi burada arayıp düzeltiyorsunuz.
