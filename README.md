#staj-projesi github çalışma senaryosu.#

#######Aşama 1: Yerel Çalışma Alanını Kurmak#######

GitHub'daki o boş kutuyu bilgisayarına bir klasör olarak indirmen lazım.

Clone: Reponun URL'sini (HTTPS olanı tercih et) kopyala ve terminaline şunu yaz:

git clone https://github.com/kullanici-adin/staj-projesi.git
cd staj-projesi


İlk Dosya: Klasör bomboş olduğu için Git henüz bir şey takip edemez. Bir başlangıç dosyası yapalım.

README.md dosyası oluştur ve içine "Bu proje staj kapsamında geliştirilmektedir." yaz.

Takibe Al ve Kaydet:

git add README.md
git commit -m "Initial commit: Proje dokümantasyonu başlatıldı"
git push origin main






######Aşama 2: Profesyonel Çalışma Düzeni######

Yeni Dal Aç:

git checkout -b feature/iletisim-sayfasi

Dosya Ekle: iletisim.html adında bir dosya oluştur ve içine rastgele bir şeyler yaz.

git add .
git commit -m "Feat: İletişim sayfası iskeleti oluşturuldu"



######Aşama 3: Sunucuya Gönderme ve PR ######

Pushla (Bağlantı Kurarak):

git push -u origin feature/iletisim-sayfasi



Pull Request (PR) Aç: Şimdi GitHub sitesine git. Üstte sarı bir bantla "Compare & pull request" butonu göreceksin.



#####Aşama 4: Onay ve Senkronizasyon#####

Senaryo gereği; PR'ın onaylandığını ve GitHub üzerinden "Merge" edildiğini varsayalım. Şimdi senin bilgisayarın (local) geride kaldı.

Ana Dala Dön:

git checkout main




Güncel Kodu Çek: (Buluttaki o yeni birleşmiş hali bilgisayarına al)

git pull origin main



Temizlik: İşin bittiği için o dalı silebilirsin:

git branch -d feature/iletisim-sayfasi

