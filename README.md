Online Payments Fraud Detection - Machine Learning Models Comparison
Proje Açıklaması:
Bu proje, çevrimiçi ödeme dolandırıcılığını tespit etmek amacıyla çeşitli makine öğrenimi algoritmalarını karşılaştırmayı hedeflemektedir. Çalışmada hem Denetimli (Supervised Learning) hem de Denetimsiz (Unsupervised Learning) makine öğrenimi algoritmaları kullanılmıştır. Veri seti, farklı işlem türlerini ve bu işlemlerin dolandırıcılık olup olmadığını içermektedir.

İki farklı öğrenme türünü aynı veri seti üzerinde uygulayarak, hangi algoritmaların dolandırıcılığı daha iyi tespit ettiğini analiz ettik. Projede yer alan algoritmalar şunlardır:

Gaussian Naive Bayes (Denetimli Öğrenme)
Decision Tree (Gini & Entropy kriterleriyle) (Denetimli Öğrenme)
K-Means Clustering (Denetimsiz Öğrenme)
Veri Seti
Veri seti, çevrimiçi ödeme işlemlerini içeren "PS_20174392719_1491204439457_log.csv" dosyasından elde edilmiştir. Veri setinde, işlem türleri (type), işlem yapılan hesaplar (nameOrig ve nameDest), işlemin miktarı ve dolandırıcılık durumu gibi çeşitli özellikler yer almaktadır.

Veri setindeki isFraud etiketi, bir işlemin dolandırıcılık olup olmadığını belirtir. Bu projede, dolandırıcılık tespit etmek amacıyla bu etiket hedef değişken olarak kullanılmıştır.

Veri Ön İşleme
Proje boyunca verilerin analizi, işlenmesi ve görselleştirilmesi için şu adımlar gerçekleştirilmiştir:

Eksik ve Aykırı Değerlerin İncelenmesi: Veri setinde eksik değer bulunmamıştır, ancak aykırı değerler incelenmiş ve gerektiğinde göz ardı edilmiştir.
Gereksiz Sütunların Kaldırılması: nameOrig ve nameDest gibi sütunlar modelin performansını artırmak amacıyla kaldırılmıştır.
Label Encoding: Kategorik type değişkeni sayısal değerlere dönüştürülmüştür.
Veri Standartizasyonu: Model eğitimi için veriler StandardScaler ile ölçeklendirilmiştir.
Algoritmalar ve Performans Değerlendirmesi
Gaussian Naive Bayes
Açıklama: Gaussian Naive Bayes, hızlı ve basit bir şekilde uygulanabilir bir modeldir. Özellikle küçük veri setlerinde etkili performans gösterebilir.
Performans: Model dolandırıcılık tespitinde ortalama bir performans sergiledi. Verinin dağılımı göz önüne alındığında, Gaussiyen dağılımlara uygun olmayan verilerde zorluklar yaşadı.
Decision Tree (Gini & Entropy)
Açıklama: Karar ağaçları, veriyi dallar halinde ayırarak dolandırıcılık tespit etmeye çalışır. Gini ve Entropy kriterleri kullanılarak dallanmalar yapılmıştır.
Performans: Gini ve Entropy kriterleri ile oluşturulan karar ağaçları benzer sonuçlar vermiştir. Karar ağaçlarının avantajı, verinin görselleştirilebilir olması ve farklı veri türlerinde esnek çalışmasıdır. Ancak, büyük veri setlerinde fazla dallanma nedeniyle performans kaybı yaşanabilir.
K-Means Clustering
Açıklama: Denetimsiz öğrenme algoritmalarından biri olan K-Means, verileri kümelere ayırarak dolandırıcılığı tespit etmeye çalışır.
Performans: K-Means algoritması, etiketlenmemiş verilerde dolandırıcılığı tespit etmekte zorluk yaşamıştır. Kümeler ve gerçek sınıflar arasında uyumsuzluklar olduğu gözlemlenmiştir.
Sonuçlar ve Yorumlar
Denetimli öğrenme algoritmaları, bu veri setinde denetimsiz öğrenme algoritmalarına göre daha başarılı sonuçlar vermiştir.
Decision Tree algoritmaları, Gaussian Naive Bayes modeline göre biraz daha yüksek performans göstermiştir.
K-Means Clustering, sınıfları doğru bir şekilde ayıramadığı için dolandırıcılık tespitinde etkili olmamıştır.
Veri seti, dolandırıcılık tespiti için denetimli öğrenme algoritmalarına daha uygundur. Bu algoritmalar, verinin etiketlenmiş yapısını daha iyi kullanarak daha başarılı sonuçlar elde etmiştir.