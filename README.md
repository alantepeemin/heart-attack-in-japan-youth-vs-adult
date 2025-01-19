# heart-attack-in-japan-youth-vs-adult  
Data analysis project for machine learning course.  

# Proje Özeti 
Bu proje, sağlıkla ilgili özellikler içeren bir veri setine dayanarak kalp krizi meydana gelmesini tahmin etmeyi amaçlamaktadır. Kullanılan veri seti Japonya Kalp Krizi Veri Seti olarak adlandırılmaktadır. Amaç, bir kişinin çeşitli sağlık göstergelerine dayanarak kalp krizi riski altında olup olmadığını sınıflandırmak için makine öğrenimi modelleri geliştirmek ve değerlendirmektir.  

## Veri Seti Açıklaması
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
  
## Ana Özellikler  
Veri Ön İşleme: Gereksiz sütunlar kaldırılarak ve kategorik değişkenler kodlanarak veri temizlenmiştir.  
Özellik Ölçeklendirme: Sayısal özellikler StandardScaler ile ölçeklendirilmiştir.  
Modelleme: Aşağıdaki makine öğrenimi modelleri uygulanmış ve değerlendirilmiştir:  
* **Random Forest Algoritması**  
* **Lojistik Regresyon**  
* **K-Nearest Neighbors ( KNN )** 
* **K-Means Clustering**
* 
### Algoritma Karşılaştırması
Projede dört farklı makine öğrenmesi modeli denendi: Lojistik Regresyon, Random Forest, Gradient Boosting, ve K-Nearest Neighbors 
(KNN). Her bir modelin kalp krizi riskini tahmin etme performansı karşılaştırıldı.    

Projede dört farklı makine öğrenmesi modeli denendi: **Lojistik Regresyon**, **Random Forest**, **Gradient Boosting**, ve **K-Nearest Neighbors (KNN)**. Her bir modelin kalp krizi riskini tahmin etme performansı karşılaştırıldı.

| **Algoritma**            | **Doğruluk (Accuracy)** | **Kesinlik (Precision)** | **Geri Çağırma (Recall)** | **F1-Score** | **Genel Performans**         |
|--------------------------|-------------------------|--------------------------|---------------------------|--------------|------------------------------|
| **Lojistik Regresyon**    | %50.88                  | %10.29                   | %49.83                    | %17.05       | Orta seviyede, dengesiz sonuç |
| **Random Forest**         | %89.87                  | %0                       | %0                        | %0           | Negatif sınıflar için harika, pozitif sınıflarda başarısız |
| **Gradient Boosting**     | %89.81                  | %0                       | %0                        | %0           | Negatif sınıflar için iyi, pozitif sınıflarda başarısız |
| **K-Nearest Neighbors**   | %89.20                  | %6.52                    | %0.49                     | %0.91        | Negatiflerde iyi, pozitiflerde zayıf |

## Değerlendirme
Bu projede, kalp krizi riskini tahmin etmek için Lojistik Regresyon, Random Forest, Gradient Boosting ve K-Nearest Neighbors (KNN) algoritmaları kullanıldı. Her algoritmanın performansı çeşitli metriklerle değerlendirildi. Genel olarak, modeller negatif sınıfları (kalp krizi geçirmeyen bireyler) doğru bir şekilde tahmin ederken, pozitif sınıfları (kalp krizi geçiren bireyler) tahmin etmekte zorlandılar.

Lojistik Regresyon, doğruluğu düşük olmasına rağmen pozitif sınıfları bir miktar yakalayabilen tek modeldi. Bununla birlikte, bu modelin genel performansı, pozitif sınıflarda düşük kesinlik ve F1-skoru nedeniyle zayıf kaldı. Random Forest ve Gradient Boosting modelleri, negatif sınıflarda mükemmel bir başarı göstererek %100'e yakın doğruluk sağladılar. Ancak, her iki model de pozitif sınıflarda hiçbir başarı gösteremedi, yani kalp krizi geçiren bireyleri tahmin etme konusunda tamamen başarısız oldular. KNN algoritması da negatif sınıflarda yüksek başarı gösterse de pozitif sınıflarda düşük performans sergiledi.

Bu sonuçların ana nedeni, veri setindeki sınıf dengesizliği olabilir. Eğer kalp krizi geçiren bireylerin sayısı çok azsa, modeller bu sınıfı öğrenmekte zorlanabilir ve bu da pozitif sınıfları doğru tahmin edememelerine yol açabilir. Ayrıca, kullanılan özelliklerin pozitif sınıfları ayırt etmek için yeterince belirleyici olmaması da bir başka etkendir. Örneğin, modeller sadece genel sağlık göstergelerine dayanarak pozitif sınıfları belirlemekte zorlanabilir. Bununla birlikte, modeller genellikle doğruluk metrikleri üzerinden optimize edilir ve pozitif sınıfların çok az olduğu bir veri setinde doğruluğu artırmak, negatif sınıfların doğru tahminiyle sağlanabilir. Bu da modellerin pozitif sınıfları göz ardı etmesine neden olur.

Sonuç olarak, sınıf dengesizliği ve verinin yetersiz temsil edilmesi, algoritmaların pozitif sınıfları tahmin etme yeteneğini sınırlamıştır. Daha iyi sonuçlar elde edebilmek için, veri setinin dengelenmesi, sınıf ağırlıkları üzerinde çalışılması ve pozitif sınıfı daha iyi ayırt eden yeni özelliklerin eklenmesi gerekmektedir.


## Proje Yapısı  
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
## Kullanım
japan_heart_attack_dataset.csv veri setini not defterine yükleyin.   
Not defterindeki hücreleri çalıştırarak verileri ön işleyin, modelleri eğitin ve sonuçları değerlendirin.  
Model performansını ROC eğrileri, karışıklık matrisleri ve diğer metriklerle görselleştirin.   
## Sonuçlar   
Modeller, çeşitli performans metriklerine göre değerlendirilmiştir. Sonuçlar, Rastgele Orman Sınıflandırıcısı modelinin en yüksek performansı sağladığını göstermektedir. Aşağıdaki metriklere odaklanılmıştır:   
(Accuracy, Precision, Recall, F1-Score, ROC-AUC )    

## Görselleştirme   
Ana görselleştirmeler şunları içermektedir:   
* Veri kümesinin korelasyon ısı haritası.
* Model değerlendirmesi için ROC eğrileri.
* Sınıflandırma performansını değerlendirmek için karışıklık matrisleri.

 
## Katkıda Bulunma  
Bu projeye katkıda bulunmak istiyorsanız, depoyu fork'layabilir ve önerilerinizi içeren bir pull request gönderebilirsiniz.    

## Lisans
Bu proje, MIT Lisansı altında açık kaynak olarak sunulmuştur.  


  




