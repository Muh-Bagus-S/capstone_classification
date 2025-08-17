# capstone_classification
For Capstone Project Data Classification Class

## Project Title: Amazon Basics Battery Customer Review Classification

## Project Overview:
1. Latar Belakang: Banyaknya jumlah review serta isi review yang beragam memerlukan waktu dan usaha banyak apabila dilakukan secara manual, maka dengan menggunakan Model AI dari IBM yaitu IBM Granite Model 3.3 8b instruct, proses review dapat berjalan dengan cepat dan efisien. 
2. Permasalahan: jumlah review, ragam review, waktu yang diperlukan, konsistensi.
3. Tujuan: a. Melakukan classification terhadap review-review berupa sentimen konsumer (Positive, Negative, Mixed, Unclear)
           b. Melakukan kategorisasi terhadap setiap review (Battery Life, Battery Quality, Brand Satisfaction, Packaging, Shipping/Delivery, Value for Money)
           c. Memasukkan output menjadi format Excel yang teratur dan langsung bisa di-Pivot
4. Pendekatan: a. Membuka Google Colab,
               b. Connect API Key dengan Replicate,
               c. Mulai mengkode untuk: install pip, download dataset csv customer review, memastikan csv path konsisten dan masuk kode,
               d. Mulai mengkode untuk: setup api token, memuat model, memasukkan parameter, target path csv file dataset, mengambil jumlah review, meng-chunk agar output bisa dalam jumlah banyak, parse agar bisa dijadikan Excel yang teratur, menulis prompt, menyimpan file excel dari output dan download file lewat menu Colab sisi kiri, membuat pivot table dan pivot chart.

## Raw Dataset Link
https://www.kaggle.com/datasets/datafiniti/consumer-reviews-of-amazon-products/data?select=Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv

## Insights and Findings
# Insights: 
1. Review dari konsumen sangat beragam dan tidak terduga, seperti tone, typo, ketidakjelasan kategori review (seperti hanya menyebutkan "saya baru saja membeli, nanti akan saya kabari") tapi mereka tetap menuliskan review, penyebutan brand lain. Semua faktor memengaruhi konsistensi model AI dalam mengklasifikasikannya.
2. Format Output dari AI yang dituliskan di Google Colab tidak bisa 100% konsisten. Meski sudah diberi tanda kata seperti "IMPORTANT follow this foratm, MUST follow this format, DO NOT add addition, commentary). Namun, model AI IBM Granite terkadang tetap saja keluar jalur. (atau mungkin Saya yang kurang mengutak-atik lagi lebih lama).
3. File dataset yang berisi beragam jenis barang (baterai, smartwatch, dsb.) bisa memengaruhi penyusunan output secara keseluruhan, karena kategorisasi baterai (seperti battery life, battery quality) berbeda dari kategorisasi smartwatch. Maka, Saya memutuskan untuk mengambil hanya 50 review dari atas (beribu-ribu review dari urutan atas adalah barang Baterai, namun Saya membatasi 50 agar Credits tidak berkurang cepat).

# Findings:
1. Dari 50 review baterai, 31 bersetimen Positif, 10 Negatif, 6 Mixed, dan 3 Unclear.
2. Kategori positif didominasi oleh Battery Quality disebutkan sebanyak 30 kali, lalu Value for Money sebanyak 29. Kategori negatif didominasi oleh Battery Quality yang disebutkan sebanyak 9 kali, lalu Battery Life sebanyak 8 kali.

## AI Support Explanation
1. LLM AI IBM Granite Instruct: merupakan Model AI LLM yang digunakan untuk menganalisis sentimen dan kategorisasi review. LLM (large language models) merupakan contoh tipe AI yang telah dilatih dengan bahan jumlah teks yang sangat besar sehingga AI dapat membuat output yang dapat memahami bahasa manusia. Lalu, model "instruct" dari IBM ini memungkinkan user untuk melakukan analisis secara presisi, paham konteks yang ada pada teks, efisien dalam waktu dan resource yang digunakan, serta dapat mengikuti instruksi format output dari user.
2. ChatGPT: membantu menerjemahkan keinginan user menjadi kode yang siap dimasukkan ke google colab. Membantu user untuk menganalisis Error dan memberikan saran lanjutan terhadap kode.
3. Gemini: melakukan analisis dan perbaikan secara langsung pada Google Colab.
