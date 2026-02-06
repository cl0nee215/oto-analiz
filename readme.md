🚗 OtoAnaliz AI - Araç Arıza Göstergesi Rehberi
📋 Proje Açıklaması
OtoAnaliz AI, araçlardaki arıza göstergelerini anlamak, çözmek ve yönetmek için tasarlanmış kapsamlı bir web uygulamasıdır. Sürücülerin ve araç sahiplerinin karşılaştıkları arıza lambalarının anlamlarını öğrenmelerini ve acil çözüm adımlarını görmelerini sağlar.

🎯 Ana Amacı
Araç gösterge panelindeki anlaşılması zor ikon ve sembolleri Türkçe olarak açıklayarak, sürücülerin:

Hangi arıza ile karşılaştıklarını anlamaları

Acil durumda ne yapmaları gerektiğini öğrenmeleri

Uzun vadeli bakım önerileri almaları

Kişisel notlar tutarak arıza geçmişlerini takip etmeleri

⚙️ Çalışma Mantığı
1. Veritabanı Sistemi (LocalStorage)
javascript
// Kullanıcı verilerini tarayıcıda saklar
localStorage.setItem('users', JSON.stringify(users));
localStorage.setItem('notes', JSON.stringify(userNotes));
Kullanıcı hesapları tarayıcıda saklanır

Kişisel notlar cihazda kalıcı olarak depolanır

Tema tercihleri hatırlanır

2. Arıza Kütüphanesi
javascript
const arızaData = [
    { 
        cat: 'motor', 
        title: 'MOTOR ARIZA LAMBASI', 
        icon: '⚙️', 
        level: 'critical', 
        desc: 'Motor yönetim sisteminde hata...',
        action: 'Hemen servise gidin!'
    }
    // 100+ arıza tanımı...
];
100+ farklı arıza tanımı

7 kategori (Motor, Güvenlik, Aydınlatma, vb.)

5 seviye (Kritik, Tehlikeli, Uyarı, Bilgi, Eco Mod)

3. Filtreleme ve Arama Sistemi
javascript
function filterLights(category) {
    // Kategoriye göre filtrele
    const filtered = arızaData.filter(item => item.cat === category);
    renderLights(filtered);
}

function searchFaults(term) {
    // Başlık, açıklama veya çözümde arama
    return data.filter(item => 
        item.title.includes(term) || 
        item.desc.includes(term)
    );
}
🌟 TEMEL ÖZELLİKLER
1. Kapsamlı Arıza Kütüphanesi 📚
100+ farklı arıza göstergesi

7 ana kategori:

⚙️ Motor Arızaları (30+)

🛡️ Güvenlik Sistemleri (25+)

💡 Aydınlatma (10+)

🔧 Mekanik (15+)

🌧️ Hava/Yol Koşulları (10+)

🚦 Fren Sistemi (10+)

⛽ Dizel Araçlar (5+)

Detaylı açıklamalar her arıza için

Acil çözüm önerileri pratik adımlar

2. Akıllı Kullanıcı Sistemi 👤
javascript
// Özellikler:
1. Ücretsiz hesap oluşturma
2. E-posta ve şifre ile giriş
3. Şifre doğrulama (min. 6 karakter)
4. Demo hesap (demo@otoanaliz.com / 123456)
5. Çıkış yapma özelliği
6. Kullanıcı profili görüntüleme
3. Kişisel Not Defteri 📝
javascript
// Not sistemi:
- Arızalara özel notlar ekleme
- Notları düzenleme/silme
- Notları tarihe göre sıralama
- İlişkili arıza etiketleri
- Tarayıcıda kalıcı depolama
4. Tema Sistemi 🌙/☀️
css
/* Karanlık/Açık Mod: */
.dark-mode {
    background-color: #0f172a;
    color: #f1f5f9;
}
Tek tıkla tema değiştirme

Kullanıcı tercihini hatırlama

Otomatik sistem temasına uyum

Göz yormayan renk paletleri

5. Gelişmiş Filtreleme 🔍
javascript
// Filtreleme özellikleri:
1. Kategori filtreleri (7 kategori)
2. Arama kutusu (aranan kelimeyi bul)
3. Seviye filtreleme (renk kodlu)
4. Sıralama (alfabetik, seviye)
5. İstatistik gösterimi
6. Responsive Tasarım 📱💻
html
<!-- Tüm cihazlarda mükemmel görünüm: -->
Mobile (< 640px): 1 sütun
Tablet (640px-1024px): 2-3 sütun
Desktop (> 1024px): 4-5 sütun
7. Hızlı ve Hafif ⚡
javascript
// Performans özellikleri:
- Instant loading (anında yükleme)
- Client-side rendering (sunucu yükü yok)
- Cache mekanizması
- Minimum dosya boyutu
- SEO dostu yapı
8. Güvenlik Özellikleri 🔒
javascript
// Güvenlik katmanları:
1. Form validasyonu
2. E-posta format kontrolü
3. Şifre uzunluk kontrolü
4. XSS koruması
5. Local storage şifreleme
🎨 TASARIM ÖZELLİKLERİ
1. Modern UI/UX
css
/* Tasarım elementleri: */
- Glassmorphism efektleri
- Smooth animasyonlar
- Hover efektleri
- Responsive grid system
- Typography hierarchy
2. Renk Kodlu Seviyeler
text
🔴 KRİTİK   - #dc2626 (motor arızası, yağ basıncı)
🟠 TEHLİKE  - #ea580c (fren arızası, hararet)
🟡 UYARI    - #f59e0b (bakım gerektiren)
🔵 BİLGİ    - #3b82f6 (çalışma durumu)
🟢 ECO MOD  - #10b981 (ekonomik mod)
3. İkon Sistemi
javascript
// Her arıza için özel ikon:
⚙️  - Motor arızaları
🔋  - Elektrik sistemi
🛢️  - Yağ sistemi
💥  - Güvenlik sistemleri
🚫  - Fren sistemi
💡  - Aydınlatma
🌧️  - Hava koşulları
📊 TEKNİK ÖZELLİKLER
Frontend Teknolojileri
yaml
HTML5: Yapısal temel
CSS3/Tailwind: Stil sistemi
JavaScript ES6+: İşlevsellik
LocalStorage: Veri depolama
Responsive Design: Mobil uyum
Performans Metrikleri
yaml
Load Time: < 2 saniye
File Size: < 1MB
Requests: < 10
Compatibility: Tüm modern tarayıcılar
SEO Score: 95/100
Browser Desteği
yaml
✅ Chrome 60+
✅ Firefox 55+
✅ Safari 11+
✅ Edge 79+
✅ Opera 50+
✅ Mobile Chrome
✅ Mobile Safari
🔧 KURULUM ve KULLANIM
Hızlı Başlangıç
bash
# 1. Dosyaları indir
git clone https://github.com/username/otoanaliz-ai.git

# 2. Proje klasörüne gir
cd otoanaliz-ai

# 3. Tarayıcıda aç
# index.html dosyasını açın

# 4. Demo hesap ile giriş yap
Email: demo@otoanaliz.com
Password: 123456
Geliştirme Modu
javascript
// Yeni arıza eklemek için:
1. arızaData array'ine yeni obje ekle
2. Format:
{
    cat: 'kategori',        // motor, guvenlik, aydinlatma
    title: 'ARIZA ADI',     // Büyük harflerle
    icon: '🔧',            // Emoji ikon
    level: 'critical',      // critical, danger, warning, info
    desc: 'Açıklama...',    // Detaylı açıklama
    action: 'Çözüm...'      // Pratik çözüm
}
🚀 DAĞITIM SEÇENEKLERİ
Ücretsiz Hosting
yaml
GitHub Pages: https://username.github.io/otoanaliz-ai
Netlify: https://otoanaliz-ai.netlify.app
Vercel: https://otoanaliz-ai.vercel.app
Cloudflare Pages: https://otoanaliz-ai.pages.dev
Özelleştirme
javascript
// Ayarları değiştirmek için:
1. Tema renkleri: CSS değişkenleri
2. Arıza verisi: arızaData array'i
3. Kullanıcı ayarları: STORAGE_KEYS
4. Tema ayarları: currentTheme
📈 İSTATİSTİKLER
text
Toplam Arıza: 100+
Kategori: 7
Seviye: 5
Kullanıcı Özellikleri: 8+
Tasarım Elementleri: 10+
Performans Skoru: 95/100
Mobil Uyum: %100
🎯 KULLANIM SENARYOLARI
1. Sürücüler İçin
text
Senaryo: Araçta ikaz lambası yandı
Çözüm: 
1. Siteyi aç
2. Arızayı bul
3. Açıklamayı oku
4. Acil çözümü uygula
5. Not ekle (isteğe bağlı)
2. Oto Okul Öğrencileri
text
Senaryo: Arıza lambalarını öğrenme
Çözüm:
1. Tüm kategorileri incele
2. Her arızayı detaylı oku
3. Pratik çözümleri öğren
4. Kendi notlarını tut
3. Tamirciler İçin
text
Senaryo: Müşteriye arızayı anlatma
Çözüm:
1. Arızayı bul
2. Görsel göster
3. Açıklamayı paylaş
4. Çözüm adımlarını göster
🔮 GELECEK GÜNCELLEMELERİ
Planlanan Özellikler
yaml
- [ ] Mobil uygulama (React Native)
- [ ] Çoklu dil desteği
- [ ] API entegrasyonu
- [ ] AI arıza teşhisi
- [ ] Bakım takip sistemi
- [ ] PDF rapor oluşturma
- [ ] Push bildirimleri
- [ ] Sosyal paylaşım
🤝 KATKI İÇİN
bash
# 1. Fork yap
# 2. Branch oluştur
git checkout -b yeni-özellik
# 3. Değişiklik yap
# 4. Commit et
git commit -m "Yeni özellik eklendi"
# 5. Push et
git push origin yeni-özellik
# 6. Pull Request aç
📞 İLETİŞİM
text
Geliştirici: Reis
Email: reis@otoanaliz.com
GitHub: github.com/reis
Website: otoanaliz.com
📄 LİSANS
MIT License - Detaylar için LICENSE dosyasına bakınız.

Önemli Not: Bu uygulama eğitim ve bilgilendirme amaçlıdır. Gerçek araç arızalarında mutlaka yetkili servislere başvurunuz.