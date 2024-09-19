# Aygaz-Bootcamp-Project

VERİ SETİ HAKKINDA
property_type Bu bölümde altı farklı türümüz var:
​
Ev
Çiftlik Evi
Üst Kısım
Alt Kısım
Daire
Oda
Fiyat Fiyat, bu veri setinde bağımlı bir özellik/parametredir.
​
City; Bu veri setinde toplam şehir sayısı beştir:
​
Lahor
Karaçi
Faisalabad
Rawalpindi
İslamabad
​
Location parametresi her şehirdeki farklı konum türleriyle ilgilidir.

bedrooms parametresi evin yatak odası sayısı.

baths parametresi evin tuvalet sayısı.

price parameteresi Fiyat.

purpose parametresi ise satıldığını mı yoksa kiralandı mı onu gösterir.
​
ilk 5 satır:


![2024-09-19_23-20-37](https://github.com/user-attachments/assets/f7b43b39-a36a-4829-a772-30eb55cfab14)





Purpose ve property_type dağılımı grafiği:



![2024-09-19_23-27-27](https://github.com/user-attachments/assets/50ae398e-1efd-4419-8ab3-698673152e05)


Property_type ve City dağılımı


![2024-09-19_23-29-36](https://github.com/user-attachments/assets/d063472b-2b85-40e4-9926-bc471c0f11bc)


LabelEncoder kullanarak kategorik olan Purpose , city, location ve property_type sütunlarını numerik hale getirdim.


Veri setini X ve y diye ayırdıktan sonra da y değerlerinin logaritmik hallerini alarak performansı arttırmak istedim.

SUPERVISED

Sonrasında Linear regression, ADABOOST regressor, Gradient Boosting Regressor ve XGBoost algoritmalarını kullanarak modelimi eğittim.
Bütün modellerin R² skorlarına baktığımda,XGBoost modelinin en iyi skoru verdiğini gördüm ve bu yüzden en iyi model olarak onu seçtim.

Linear Regression R² skoru:0.9752984804700517

ADA Boost R² skoru:0.9595507744553684

Gradient Boosting R² skoru:0.9810552694406954

XGBoost R² skoru:0.9842103648408563

UNSUPERVISED

Veriseti çok büyük olduğundan dolayı minibatch K-Means algoritmasını kullandım burada verisetini böldüm o şekilde kullandım.

Price ve purpose arasında kurduğum bir K-Means grafiği

![download](https://github.com/user-attachments/assets/3323fdc0-1e41-4997-ba7d-76b29a714d82)

Bu Modelde silhoutte skorunu kullandım ve 0.27 gibi bir değer buldum. Bu skor da modelin skorunun kötü olduğu(Kötü, kümeler arasında belirgin ayrımlar yok, modelin iyileştirilmesi gerekiyor.) anlamına geliyor.
