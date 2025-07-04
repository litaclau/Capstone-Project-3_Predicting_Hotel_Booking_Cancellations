# CAPSTONE 3: Predicting Hotel Booking Cancellations

Dalam Capstone Project ini saya membangun sebuah model machine learning menggunakan dataset **Hotel Booking Demand**, Adapun sumber dataset yakni https://drive.google.com/drive/folders/17KIeOXK7eYGuzgpn_IljlUFcE4v96lSL

---

## Contents

1. Business Problem Understanding
2. Data Understanding
3. Data Preprocessing
4. Modeling (find best model & evaluation best model)
5. Conclusion & Recommendation

---

## Business Problem Understanding

Industri perhotelan sangat dipengaruhi oleh perilaku pemesanan customer atau tamu hotel. Perilaku ini dipengaruhi oleh beberapa faktor di antaranya faktor musiman (weekend, weekday, holiday), event (lokal & internasional), ekonomi, promosi serta diskon, dan lain sebagainya. Akibat ketidakpastian ini, pihak hotel harus memahami dan mengantisipasi perilaku customer yang berisiko merugikan hotel. Dalam hal ini, pembatalan reservasi yang berdampak pada operasional dan keuangan hotel. Tindakan antisipasi yang dapat dilakukan yakni memprediksi kemungkinan pembatalan reservasi oleh customer dengan memanfaatkan data historis pemesanan hotel sebelumnya.

---

## Data Understanding

Dataset terdiri dari 11 kolom yang terdiri dari 10 feature dan 1 target, yakni:

- Country
- Market Segment
- Previous Cancellations
- Booking Changes
- Deposit Type
- Days in Waiting List
- Customer Type
- Reserved Room Type
- Required Car Parking Spaces
- Total of Special Request
- Is Canceled

---

## Data Preprocessing

- Melakukan imputasi pada missing value di feature `country`
- Melakukan pengodean Ordinal dan One-Hot pada feature kategorik
- Melakukan Robust Scaling untuk feature numerik

---

## Modeling

Model machine learning yang diuji adalah sebagai berikut:
- Logistic Regression
- KNN
- Decision Tree
- **Random Forest (Best model)**
- XGBoost

---

## Conclusion
- *Model Random Forest dipilih sebagai model terbaik* dengan mempertimbangkan besar *recall (85%), **accuracy (59%), **F1-score (59%)*. Dengan begitu, model ini sensitif dalam mendeteksi pembatalan dan cukup akurat walaupun pada kondisi data yang imbalance. 
- Nilai *AUC (Area Under Curve) sebesar 0.83* menunjukkan bahwa model memiliki tingkat diskriminasi yang kuat. Dengan demikian, model Random Forest sangat layak digunakan sebagai sistem prediksi pembatalan reservasi hotel.
- Feature yang paling berpengaruh dalam memprediksi pembatalan reservasi adalah *required_car_parking_spaces*, artinya permintaan ruang parkir yang tinggi cenderung berhubungan dengan kemungkinan pembatalan. 
- Model ini berhasil memprediksi pembatalan reservasi hotel guna meminimalisasi risiko kerugian finansial, membantu pengambilan keputusan tim revenue management dan front office hotel, serta mengoptimalkan operasional hotel.
