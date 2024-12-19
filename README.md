# Low-Voltage-Motor-Driver-Circuit

![pcb_on](https://github.com/user-attachments/assets/3185e925-4f6b-4a28-b1ef-4887451499d7) ![PCBdoc](https://github.com/user-attachments/assets/4f8eb9ff-2043-4bae-89ed-d3658a745d8d)

# **DC Motor Sürücü ve Güç Regülatör Devresi**

Bu proje, DC motorların kontrolü ve sistem kararlılığı sağlamak için bir motor sürücü devresi, akım algılama birimi ve 3.3V sabit voltaj sağlayan bir regülatör içerir. Devre, robotik uygulamalar, otomasyon sistemleri ve eğitim projeleri gibi birçok farklı alanda kullanılabilir. Tasarım, **Altium Designer** kullanılarak detaylı bir şekilde oluşturulmuştur.


## 📜 **Proje Özeti**
- **Amaç:** Düşük güçlü DC motorların hassas kontrolünü sağlamak ve güç stabilizasyonu sunmak.
- **Kapsam:** 
  - Motor kontrolü (PWM tabanlı sürüş)
  - Akım algılama ve geri besleme
  - Güç regülasyonu
- **Teknoloji:** Altium Designer ile şematik tasarım ve PCB üretimi.


## 🛠️ **Devre Özellikleri**
1. **Motor Sürücü:**
   - QFN paket motor sürücü IC kullanılarak iki yönlü motor kontrolü sağlanır.
   - PWM sinyalleri ile hassas hız ve yön kontrolü.
   - Aşırı akım koruması.

2. **Akım Algılama:**
   - **MCP6043 Op-Amp** kullanılarak akım algılama ve motor akımının gerçek zamanlı izlenmesi.
   - Geri besleme döngüsü ile motor akımı kararlı tutulur.

3. **Güç Regülatörü:**
   - **L78L33ABUTR Regülatör** ile 3.3V sabit çıkış gerilimi.
   - Giriş gerilim aralığı: 5V-12V.
   - Yüksek verimlilik ve düşük sıcaklık artışı.

4. **PCB Tasarımı:**
   - Düşük EMI ve parazitlenme için optimize edilmiş hat yerleşimi.
   - Yüksek güç hatları için geniş bakır dolgular.
   - Kompakt ve montaj dostu tasarım.


## 🖥️ **Devre Şeması ve Bileşenler**

### **Devre Şeması**

![sematik](https://github.com/user-attachments/assets/f4eb6c9d-66e8-44f2-bdba-d9fcf4193ebf)

### **Kritik Bileşenler**
| **Bileşen**       | **Model/Değer**               | **Açıklama**                                 |
|--------------------|-------------------------------|---------------------------------------------|
| **Motor Sürücü IC**| A3918SESTR-T                 | Çift yönlü DC motor kontrolü                |
| **Op-Amp**         | MCP6043T-E/CH                | Akım algılama ve geri besleme devresi       |
| **Regülatör**      | L78L33ABUTR                  | 3.3V sabit çıkış sağlayıcı                  |
| **Dirençler**      | 10 kΩ, 0.1 Ω                 | Sinyal şekillendirme ve akım algılama       |
| **Kapasitörler**   | 100 nF, 10 µF, 470 µF        | Gerilim stabilizasyonu ve parazit filtreleme|


## ⚙️ **Sistem Çalışma Prensibi**
1. **Motor Kontrolü:**
   - PWM sinyali, motor sürücü IC'ye uygulanır.
   - Motorun ileri/geri yönde çalıştırılması için H-köprüsü topolojisi kullanılır.

2. **Akım Algılama:**
   - Shunt direnci üzerinden geçen akım, MCP6043 op-amp ile ölçülür.
   - Geri besleme yoluyla akım kontrolü sağlanır.

3. **Voltaj Regülasyonu:**
   - L78L33ABUTR regülatör, giriş geriliminden 3.3V sabit çıkış üretir.
   - Yük dalgalanmaları, kapasitörlerle dengelenir.

### **Test Süreci**
1. Giriş voltajını (5V-12V) bağlayın.
2. PWM sinyali ile motorun hızını ve yönünü test edin.
3. Akım algılama devresinin çalışmasını ölçü aleti ile doğrulayın.
4. 3.3V çıkış gerilimini kontrol edin.


## 🌟 **Katkı Sağlama**
Projeye katkıda bulunmak isteyenler aşağıdaki adımları izleyebilir:
1. Bu repoyu forklayın.
2. Değişikliklerinizi yapın.
3. Pull request göndererek önerilerinizi paylaşın.


## 📧 **İletişim**
Herhangi bir sorunuz ya da öneriniz için benimle iletişime geçebilirsiniz:
- **Email:** [ilknurylmz.1707@gmail.com](mailto:ilknurylmz.1707@gmail.com)

---

### **Not:**
Bu proje, açık kaynaklıdır ve eğitim/araştırma amaçlı kullanılabilir. Ticari kullanımlar için proje sahibinden izin alınmalıdır.
