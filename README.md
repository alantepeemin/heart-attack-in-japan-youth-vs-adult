## heart-attack-in-japan-youth-vs-adult 🇯🇵  
Data analysis project for machine learning course.  
## Makine Öğrenimi ile Kalp Krizi Tahmini 
# Proje Özeti 
Bu proje, sağlıkla ilgili özellikler içeren bir veri setine dayanarak kalp krizi meydana gelmesini tahmin etmeyi amaçlamaktadır. Kullanılan veri seti Japonya Kalp Krizi Veri Seti olarak adlandırılmaktadır. Amaç, bir kişinin çeşitli sağlık göstergelerine dayanarak kalp krizi riski altında olup olmadığını sınıflandırmak için makine öğrenimi modelleri geliştirmek ve değerlendirmektir.  

# Veri Seti Açıklaması
Veri seti şu sütunlardan oluşmaktadır:  

* **Age (Yaş):**   Kişinin yaşı.  
* **Gender (Cinsiyet):**   Kişinin cinsiyeti (1 erkek, 0 kadın).  
* **Region (Bölge):**   Kişinin yaşadığı coğrafi bölge.  
* **Smoking History (Sigara Kullanım Geçmişi):**   Kişinin sigara kullanım geçmişini belirtir.  
* **Diabetes History (Diyabet Geçmişi):**   Kişinin diyabet geçmişini belirtir.  
* **Hypertension History (Hipertansiyon Geçmişi):**   Kişinin hipertansiyon geçmişini belirtir.  
* **Cholesterol Level (Kolesterol Seviyesi):**   Kişinin kolesterol seviyesi.  
* **Physical Activity (Fiziksel Aktivite):**   Fiziksel aktivite seviyesi.  
* **Diet Quality (Diyet Kalitesi):**   Kişinin diyet kalitesini belirtir.  
* **Alcohol Consumption (Alkol Tüketimi):**   Kişinin alkol tüketip tüketmediğini belirtir.  
* **Stress Levels (Stres Seviyeleri):**   Kişinin stres seviyesi.   
* **BMI (Vücut Kitle İndeksi):**   Kişinin vücut kitle indeksi.  
* **Heart Rate (Kalp Atış Hızı):**   Kişinin kalp atış hızı.  
* **Systolic BP (Sistolik Kan Basıncı):**   Kişinin sistolik kan basıncı.  
* **Diastolic BP (Diastolik Kan Basıncı):**   Kişinin diyastolik kan basıncı.  
* **Family History (Aile Geçmişi):**   Kişinin ailede kalp hastalığı geçmişi olup olmadığını belirtir.  
* **Heart Attack Occurrence (Kalp Krizi Durumu):**   Hedef değişken; kişinin kalp krizi geçirip geçirmediğini belirtir (1 evet, 0 hayır).  
# Ana Özellikler  
Veri Ön İşleme: Gereksiz sütunlar kaldırılarak ve kategorik değişkenler kodlanarak veri temizlenmiştir.  
Özellik Ölçeklendirme: Sayısal özellikler StandardScaler ile ölçeklendirilmiştir.  
Modelleme: Aşağıdaki makine öğrenimi modelleri uygulanmış ve değerlendirilmiştir:  
* **Random Forest Algoritması**  
* **Lojistik Regresyon**  
* **K-Nearest Neighbors ( KNN )** 
* **K-Means Clustering**  
# Değerlendirme
Modeller, accuracy, precision, recall, F1 skoru ve ROC-AUC gibi metriklerle değerlendirilmiştir.  

# Proje Yapısı  
MachineLearningFinal.ipynb: Veri ön işleme, model eğitimi ve değerlendirmesi için kodları içeren ana Jupyter not defteri.  
japan_heart_attack_dataset.csv: Analiz için kullanılan veri seti (gizlilik nedeniyle depo içerisine dahil edilmemiştir).  

## Kurulum  

Bu projeyi yerel ortamınızda çalıştırmak için:  

1. Depoyu klonlayın:   
   ```bash
   git clone https://github.com/yourusername/heart-attack-in-japan-youth-vs-adult.git
   cd heart-attack-in-japan-youth-vs-adult
2. Sanal Oturum Oluşturun ve Etkinleştirin  
   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows için: venv\Scripts\activate
3. Bağımlılıkları yükleyin:  
   ```bash
   pip install -r requirements.txt
4. Jupyter not defterini açın:  
   ```bash
   jupyter notebook
# Kullanım
japan_heart_attack_dataset.csv veri setini not defterine yükleyin.   
Not defterindeki hücreleri çalıştırarak verileri ön işleyin, modelleri eğitin ve sonuçları değerlendirin.  
Model performansını ROC eğrileri, karışıklık matrisleri ve diğer metriklerle görselleştirin.   
# Sonuçlar   
Modeller, çeşitli performans metriklerine göre değerlendirilmiştir. Sonuçlar, Rastgele Orman Sınıflandırıcısı modelinin en yüksek performansı sağladığını göstermektedir. Aşağıdaki metriklere odaklanılmıştır:   
(Accuracy, Precision, Recall, F1-Score, ROC-AUC )    

# Görselleştirme   
Ana görselleştirmeler şunları içermektedir:   
* Veri kümesinin korelasyon ısı haritası.
* Model değerlendirmesi için ROC eğrileri.
* Sınıflandırma performansını değerlendirmek için karışıklık matrisleri.

 
# Katkıda Bulunma  
Bu projeye katkıda bulunmak istiyorsanız, depoyu fork'layabilir ve önerilerinizi içeren bir pull request gönderebilirsiniz.    

# Lisans
Bu proje, MIT Lisansı altında açık kaynak olarak sunulmuştur.  


  




