# Akbank_Makine_Ogrenmesine_Giris_Bootcamp
## Kaggle Notebook

Projeyi Kaggle üzerinde görüntülemek için aşağıdaki bağlantıya tıklayabilirsiniz:

[Kaggle Notebook Linkim](https://www.kaggle.com/code/merygcl/d-nyadan-covid-19-verileri)


Bu Jupyter Notebook projesi, COVID-19 salgınının küresel verilerini analiz etmeyi ve görselleştirmeyi amaçlamaktadır. Proje, salgının zamansal eğilimlerini, coğrafi dağılımını ve sosyo-ekonomik faktörlerle ilişkisini inceleyerek, COVID-19'un dünya üzerindeki etkilerini anlamlandırmaya çalışmaktadır.

## Kullanılan Veriler
Projede, Kaggle'dan temin edilen ve dünya genelindeki COVID-19 verilerini içeren owid-covid-data.csv adlı CSV dosyası kullanılmıştır. Bu veri seti, geniş bir yelpazede bilgileri barındırmaktadır:

Coğrafi ve Zamansal Bilgiler: iso_code, continent, location (ülke), date.
Vaka ve Ölüm Sayıları: total_cases, new_cases, total_deaths, new_deaths (hem ham sayılar hem de düzeltilmiş/milyon kişi başına düşen değerler).
Sağlık Sistemi Kapasitesi: icu_patients, hosp_patients, weekly_icu_admissions, weekly_hosp_admissions, hospital_beds_per_thousand.
Test ve Pozitiflik Oranları: total_tests, new_tests, positive_rate, tests_per_case.
Aşılama Verileri: total_vaccinations, people_vaccinated, people_fully_vaccinated, total_boosters (hem ham sayılar hem de yüzdelik değerler).
Sosyo-Ekonomik ve Demografik Göstergeler: population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, extreme_poverty, cardiovasc_death_rate, diabetes_prevalence, female_smokers, male_smokers, handwashing_facilities, life_expectancy, human_development_index.
Hükümet Tedbirleri: stringency_index (sıkı önlemler endeksi).
Aşırı Ölüm Oranları: excess_mortality_cumulative_absolute, excess_mortality_cumulative, excess_mortality, excess_mortality_cumulative_per_million.
Veri seti, 220.343 satır ve 67 sütundan oluşmaktadır. Veri ön işleme adımlarında, date sütunu datetime formatına dönüştürülmüş ve sayısal sütunlardaki eksik değerler (NaN) 0 ile doldurulmuştur. Ancak, continent gibi bazı kategorik sütunlarda eksik değerler korunmuştur.

## Analizler ve Sonuçlar
Projede gerçekleştirilen temel analizler ve elde edilen olası sonuçlar şunlardır:

Küresel Vaka ve Ölüm Eğilimleri:

Analiz: Günlük toplam vaka ve ölüm sayıları zamana göre çizdirilerek küresel salgın eğilimi incelenmiştir.
Olası Sonuç: Bu grafikler, salgının başlangıcından itibaren vaka ve ölüm sayılarının nasıl arttığını, zirve dönemlerini ve azalmalarını görsel olarak sunar.
Mortalite Oranı Analizi:

Analiz: Her ülkenin en son verileri kullanılarak ölüm oranı (Mortality_Rate = total_deaths / total_cases) hesaplanmış ve en yüksek ölüm oranına sahip ilk 10 ülke sıralanmıştır.
Olası Sonuç: Bu analiz, belirli ülkelerdeki sağlık sistemlerinin kapasitesi, veri raporlama farklılıkları veya demografik yapı gibi faktörlerin ölüm oranı üzerindeki etkilerini gösterebilir. Örneğin, Kuzey Kore gibi bazı ülkelerde oranın çok yüksek çıkması, veri eksikliklerine veya farklı raporlama yöntemlerine işaret edebilir.
Günlük Yeni Vaka ve Ölüm Eğilimleri:

Analiz: Küresel çapta günlük yeni vaka ve yeni ölüm sayıları zamana göre görselleştirilmiştir.
Olası Sonuç: Bu grafikler, salgının farklı dalgalarını ve yeni enfeksiyon ile ölüm sayılarındaki anlık değişimleri daha net bir şekilde ortaya koyar.
Kıta Bazında Durum Analizi:

Analiz: En güncel verilere göre kıtalara göre toplam vaka ve ölüm sayıları özetlenmiş ve bar grafikleri ile görselleştirilmiştir.
Olası Sonuç: Bu analiz, salgının coğrafi dağılımındaki eşitsizlikleri ve hangi kıtaların salgından daha fazla etkilendiğini gösterir.
Pozitiflik Oranı Eğilimleri:

Analiz: Belirli örnek ülkeler (örn: ABD, Hindistan, Brezilya, Birleşik Krallık, Türkiye) için zaman içindeki pozitiflik oranı eğilimleri çizdirilmiştir.
Olası Sonuç: Pozitiflik oranı, test stratejileri ve virüsün toplumdaki yaygınlığı hakkında bilgi verir. Grafikler, test kapasitesindeki değişimler veya virüsün yayılımındaki gerçek artışlar arasındaki ilişkiyi anlamaya yardımcı olabilir.
Korelasyon Analizi:

Analiz: total_cases, total_deaths, population, gdp_per_capita, life_expectancy, hospital_beds_per_thousand, stringency_index, total_vaccinations, people_fully_vaccinated_per_hundred, median_age, aged_65_older gibi COVID-19 metrikleri ve sosyo-ekonomik faktörler arasındaki korelasyon matrisi oluşturulmuştur.
Olası Sonuç: Bu ısı haritası, hangi faktörlerin vaka ve ölüm sayılarıyla güçlü bir ilişki içinde olduğunu gösterir. Örneğin, yüksek aşılanma oranlarının vaka/ölüm sayılarıyla negatif korelasyonu veya yaşlı nüfus oranının ölüm sayılarıyla pozitif korelasyonu gibi ilişkiler gözlemlenebilir.
