# LogoErpTables
Logo ERP ürün ailesinde (Start, Go, Go3, Go Wings, Tiger, Tiger Enterprise) SQL veritabanı mimarisi, transactional süreç yönetimi ve sistemsel parametrelerin yanı sıra; BI/raporlama Katmanları, CRM, e-Dönüşüm ve üçüncü parti entegrasyon protokollerinin ana veri omurgasını oluşturur.

# Logo ERP SQL Veritabanı Tablo Referansı

Bu depolama alanı, **Logo ERP** ürün ailesine (*Start, Go, Go3, Go Wings, Tiger, Tiger Enterprise*) ait SQL veritabanı tablolarını, modüler ilişkilerini ve açıklama detaylarını içermektedir.

Tablo adlarında geçen dinamik takılar:
* **`XXX`**: 3 haneli Firma Numarası *(Örn: 001, 018)*
* **`YY`**: 2 haneli Mali Dönem Numarası *(Örn: 01, 02)*
* **`L_` Ön Eki**: Sistem genelini kapsayan firma bağımsız parametre tabloları

---

<details>
<summary><b>1. Sistem, Yönetim ve Konfigürasyon Tabloları (L_ ve Genel)</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `L_CAPIDEF` | Kuruluş Bilgileri (Ambar, İşyeri, Fabrika vb.) |
| `L_CDBTMP` | Form Boyutları |
| `L_CITY` | Şehirler |
| `L_COUNTRY` | Ülkeler |
| `L_DAILYEXCHANGES` | Günlük Döviz Kurları |
| `L_GOUSERS` | Kullanıcılar |
| `L_LDOCNUM` | Döküman Numaralama Şablonları |
| `L_NET` | Network Kontrolü (Kimlerin Hangi Firma Ve Dönemle Çalıştığı) |
| `L_POSTCODE` | Posta Kodları |
| `L_RPLAYS_XXX` | Kaydedilen Rapor Tasarımları |
| `L_RPFILTSXXX` | Kaydedilen Rapor Filtreleri |
| `L_SHPAGENT` | Sevkiyat Firmaları |
| `L_SHPTYPES` | Sevkiyat Türleri |
| `L_TRADGRP` | Ticari İşlem Grupları |
| `LG_XXX_ACCCODES` | Entegrasyon Bağlantı Kodları |
| `LG_XXX_CHARCODE` | Özellik Kodları |
| `LG_XXX_CHARVAL` | Özellik Değerleri |
| `LG_XXX_CRDACREF` | Kart-Muhasebe Kodları |
| `LG_XXX_DISTLINE` | Dağıtım Şablonu Satırları |
| `LG_XXX_DISTTEMP` | Dağıtım Şablonları |
| `LG_XXX_FIRMDOC` | Döküman Katalog Girişi (Watermark) |
| `LG_XXX_LNGEXCSETS` | Bazı Kayıtların Diğer Dillerdeki Açıklamaları |
| `LG_XXX_LOGREP` | LOG (İzleme) Kaydı |
| `LG_XXX_PAYLINES` | Ödeme Plan Satırları |
| `LG_XXX_PAYPLANS` | Ödeme Planları |
| `LG_XXX_SPECODES` | Özel Kodlar |
| `LG_XXX_TRGPAR` | Trigger Parametreleri |
| `LG_XXX_YY_FOLDER` | Döküman Katalog Bilgileri (Watermark Varsa) |
| `LG_XXX_YY_PERDOC` | Döküman Bilgileri (Örnek Malzeme Resmi) |
| `LG_XXX_YY_TRANSAC` | Firma Dönem Bilgileri |

</details>

<details>
<summary><b>2. Stok ve Malzeme Yönetimi Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_ASCOND` | Alış/Satış Koşulları |
| `LG_XXX_CHARASGN` | Malzeme Özellik Ataması |
| `LG_XXX_DECARDS` | İndirim/Masraf Kartları |
| `LG_XXX_INVDEF` | Malzeme-Ambar Bilgileri |
| `LG_XXX_ITEMS` | Malzemeler |
| `LG_XXX_ITEMSUBS` | Malzeme Alternatifleri |
| `LG_XXX_ITMBOMAS` | Malzeme-Üretim Reçetesi Ataması |
| `LG_XXX_ITMCLSAS` | Malzeme-Malzeme Sınıfı Ataması |
| `LG_XXX_ITMFACTP` | Malzeme-Fabrika Bilgileri |
| `LG_XXX_ITMUNITA` | Malzeme-Birim Ataması |
| `LG_XXX_ITMWSDEF` | Malzeme-İş İstasyonu Bilgileri |
| `LG_XXX_ITMWSTOT` | Malzeme-İş İstasyonu Toplamları (Günlük) |
| `LG_XXX_LOCATION` | Stok Yerleri |
| `LG_XXX_PRCARDS` | Promosyon Kartları |
| `LG_XXX_PRCLIST` | Alış/Satış Fiyatları |
| `LG_XXX_SELCHVAL` | Malzeme-Özellik Değerleri |
| `LG_XXX_STCOMPLNK` | Karma Koli Satırları |
| `LG_XXX_SUPPASGN` | Malzeme-Tedarikçi Ataması |
| `LG_XXX_UNITSETC` | Birim Setleri Arası Çevrim Katsayıları |
| `LG_XXX_UNITSETF` | Birim Setleri |
| `LG_XXX_UNITSETL` | Birimler |
| `LG_XXX_YY_SERILOTN` | Malzeme Seri Lot No. Bilgileri |
| `LG_XXX_YY_SLTRANS` | Seri/Lot Hareketleri |
| `LG_XXX_YY_STFICHE` | Stok Fişleri |
| `LG_XXX_YY_STINVEN` | Malzeme Alış/Satış Aylık Toplamları |
| `LG_XXX_YY_STINVTOT` | Günlük Malzeme Ambar Toplamları |
| `LG_XXX_YY_STLINE` | Malzeme Hareketleri |

</details>

<details>
<summary><b>3. Cari Hesaplar Yönetimi Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_CLCARD` | Cari Hesap Kartları |
| `LG_XXX_CLINTEL` | Cari Hesap İstihbarat Bilgileri |
| `LG_XXX_YY_CLFICHE` | Cari Hesap Fişleri |
| `LG_XXX_YY_CLFLINE` | Cari Hesap Hareketleri |
| `LG_XXX_YY_CLRNUMS` | Cari Hesap Risk Tabloları |
| `LG_XXX_YY_CLTOTFIL` | Cari Hesap Aylık Toplamları |

</details>

<details>
<summary><b>4. Satış, Satınalma ve Fatura Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_ROUTETR` | Satış Rota Satırları |
| `LG_XXX_ROUTES` | Satış Yönetim Raporları |
| `LG_XXX_SLSCLREL` | Satış Elemanı-Cari Hesap İlişkisi |
| `LG_XXX_SLSMAN` | Satış Elemanları |
| `LG_XXX_TARGETS` | Satış Elemanı Hareketleri |
| `LG_XXX_YY_INVOICE` | Faturalar |
| `LG_XXX_YY_ORFICHES` | Sipariş Fişleri |
| `LG_XXX_YY_ORFLINE` | Sipariş Hareketleri |
| `LG_XXX_YY_PRODUCER` | Müstahsil Faturası |

</details>

<details>
<summary><b>5. Finans, Kasa, Banka ve Çek/Senet Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_BANKACC` | Banka Hesapları |
| `LG_XXX_BNCARD` | Bankalar |
| `LG_XXX_KSCARD` | Kasalar |
| `LG_XXX_YY_BNFICHE` | Banka Fişleri |
| `LG_XXX_YY_BNFLINE` | Banka Hareketleri |
| `LG_XXX_YY_BNTOTFIL` | Banka Aylık Toplamları |
| `LG_XXX_YY_CSCARD` | Çek/Senet Kartları |
| `LG_XXX_YY_CSHTOTS` | Kasa Aylık Toplamları |
| `LG_XXX_YY_CSROLL` | Çek/Senet Bordroları |
| `LG_XXX_YY_CSTRANS` | Çek/Senet Hareketleri |
| `LG_XXX_YY_KSLINES` | Kasa İşlemleri |
| `LG_XXX_YY_PAYTRANS` | Ödeme/Tahsilat Hareketleri |

</details>

<details>
<summary><b>6. Genel Muhasebe ve Sabit Kıymetler Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_EMCENTER` | Masraf Malzemeleri |
| `LG_XXX_EMUHACC` | Muhasebe Hesapları |
| `LG_XXX_FAREGISTS` | Sabit Kıymet Kayıtları |
| `LG_XXX_FAYEAR` | Sabit Kıymet Yıllık Kaydı |
| `LG_XXX_YY_EMFICHE` | Muhasebe Fişleri |
| `LG_XXX_YY_EMFLINE` | Muhasebe Hareketleri |
| `LG_XXX_YY_EMUHTOT` | Muhasebe Aylık Toplamları |

</details>

<details>
<summary><b>7. Üretim, Operasyon ve Reçete Yönetimi Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_BOMLINE` | Ürün Reçete Satırları |
| `LG_XXX_BOMASTER` | Ürün Reçeteleri |
| `LG_XXX_BOMREVSN` | Ürün Reçete Revizyonları |
| `LG_XXX_COPRDBOM` | Reçete-Ek Ürün Ataması |
| `LG_XXX_DISPLINE` | İş Emirleri |
| `LG_XXX_ENGCLINE` | Mühendislik Değişikliği İşlemi |
| `LG_XXX_LNOPASGN` | Operasyon-Malzeme İlişkisi |
| `LG_XXX_OCCUPATN` | Kaynak Kullanımları (Üretim) |
| `LG_XXX_OPATTASG` | Operasyon-Özellik Ataması |
| `LG_XXX_OPERTION` | Operasyonlar |
| `LG_XXX_OPRTREQ` | Operasyon İhtiyaçları |
| `LG_XXX_PEGGING` | İşlem Bağlantıları (Üretim Emri, Sipariş) |
| `LG_XXX_PRODORD` | Üretim Emirleri |
| `LG_XXX_PRVOPASG` | Önceki Operasyon İlişkileri |
| `LG_XXX_ROUTING` | Üretim Rotaları |
| `LG_XXX_RTNGLINE` | Üretim Rota Satırları |
| `LG_XXX_WORKSTAT` | İş İstasyonları |
| `LG_XXX_WSATTASG` | İş İstasyonu-Özellik Ataması |
| `LG_XXX_WSATTVAS` | İş İstasyonu-Özellik Değeri Ataması |
| `LG_XXX_WSCHCODE` | İş İstasyonu Özellikleri |
| `LG_XXX_WSCHVAL` | İş İstasyonu Özellik Değerleri |
| `LG_XXX_WSGRPASS` | İş İstasyonu-Grup Ataması |
| `LG_XXX_WSGRPF` | İş İstasyonu Grupları |

</details>

<details>
<summary><b>8. Kalite Kontrol ve İnsan Kaynakları Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_EMGRPASS` | Çalışan-Grup Ataması |
| `LG_XXX_EMPGROUP` | Çalışan Grubu |
| `LG_XXX_EMPLOYEE` | Çalışanlar |
| `LG_XXX_LABORREQ` | Çalışan İhtiyaçları |
| `LG_XXX_QASGN` | Kalite Kontrol Hareketi-Kalite Kontrol Ataması |
| `LG_XXX_QCLVAL` | Kalite Kontrol Değerleri |
| `LG_XXX_QCSLINE` | Kalite Kontrol Satırları |
| `LG_XXX_QCSET` | Kalite Kontrol Setleri |
| `LG_XXX_TOOLREQ` | Araç İhtiyaçları |
| `LG_XXX_YY_SLQCASGN` | Kalite Kontrol Hareketleri |

</details>

<details>
<summary><b>9. Hizmet Yönetimi ve Dönem İşlemleri Tabloları</b></summary>

<br/>

| Tablo Adı | Açıklama |
| :--- | :--- |
| `LG_XXX_SRVCARD` | Hizmet Kartları |
| `LG_XXX_SRVUNITA` | Hizmet Kaydı-Birim Ataması |
| `LG_XXX_YY_PRDCOST` | Maliyet Dönem Kapama Kayıtları |
| `LG_XXX_YY_SRVNUMS` | Aylık Hizmet Toplamları |
| `LG_XXX_YY_SRVTOT` | Aylık Hizmet Alış/Satış Toplamları |

</details>
