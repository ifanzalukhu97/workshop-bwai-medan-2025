# Publish

Versi videonya bisa kamu lihat / click Youtube di bawah ini :

[![Exercise 4: Publish](https://img.youtube.com/vi/NCWE8_rBmrE/0.jpg)](https://www.youtube.com/watch?v=NCWE8_rBmrE&list=PLnyg3GbBr0YZdCyFGPrOebH_vhFMb9FeE&index=5)


Ok, kita sampai di exercise ke 4, yaitu kita akan publish flow yang sudah kita buat sebelumnya.

## Prerequisites
- Pastikan sudah menyelesaikan [exercise 3 : Url Tool.md](../exercise%203/exercise%203%20%3A%20Url%20Tool.md)
- Kalau belum, bisa import flow yg sudah kita buat di exercise 2 menggunakan file `GDG Agent - Exercise 3` yang ada di disini [GDG Agent - Exercise 3.json](../exercise%203/flow/GDG%20Agent%20-%20Exercise%203.json).
  Cara import flow bisa mengikuti panduan di [Import Flow](https://docs.langflow.org/components-data#file).

## Kenapa Publish?
Yah, tentunya karena kita perlu, pertanyaan macam apa ini 😀. 

Ok tujuan kita publish agar orang lain atau user bisa menggunakan flow yang kita buat.

Kalau dilihat dari dokumentasi Langflow di [Publish flows](https://docs.langflow.org/concepts-publish), untuk publish Langflow / integrasi ke aplikasi external / lain ada beberapa cara, seperti : 
- [API access](https://docs.langflow.org/concepts-publish#api-access)
- [Embed into site](https://docs.langflow.org/concepts-publish#embed-into-site)
- Dan dengan cara lainnya yang bisa diakses di dokumentasi mereka.


## API Access dengan Python
Ok, coba kita publish flownya dengan cara API access, dan kita coba akses menggunakan Python.
1. Kita buat file baru terlebih dahulu, contohnya namanya `api-access.py`
2. Dari workspace, klik button `Publish`. Pilih `API Access`, lalu klik `Python`. Copy semua kode tersebut ke file `api-access.py` yang sudah dibuat sebelumnya.
3. Ganti `input_value`nya menjadi 
    ```text
   Di event Google Cloud Roadshows x Build with AI Medan 2025, siapa saja speakernya?
    ```
4. Lalu jalankan file `api-access.py` tersebut, dan kita lihat hasilnya.
    ```bash
   python api-access.py
    ```
   Kurang lebih seperti itu hasilnya, harus di format terlebih dahulu JSON nya agar lebih mudah previewnya. 
5. Hasil chat ini juga akan tercatat di Playground.

> ⚠️ **Catatan:** Jika mengalamin error saat run filenya, bisa sesuaiin dengan error yang muncul.

1. Kalau mengalami error `ModuleNotFoundError : No module named 'request'` saat menjalankan `api-access.py`, bisa coba install `requests` terlebih dahulu di virtual env pythonnya, dengan perintah : 
   - Buat virtual environment baru
       ```bash
         uv venv
       ```
   - Aktifkan virtual environment yang udah kamu buat:
       ```bash
         source .venv/bin/activate # di Linux/Mac
         .venv\Scripts\activate # di Windows
       ```
   - Install requests
       ```bash
         uv pip install requests
       ```
   - Jalankan kembali `api-access.py`
       ```bash
         python api-access.py
       ```
   
2. Sedangkan jika mengalami error `Api Key`, bisa coba tambahkan API Key di `Langflow API` terlebih dahulu menggunakan cara di dokumentasi [Langflow API keys](https://docs.langflow.org/configuration-api-keys) ini.
Nanti key tersebut yg digunakan di `x-api-key` saat jalankan file api-access.py dan embed.html.



## Embed into site
Ok, kita coba publish menggunakan `Embed into site`, dan kita coba akses menggunakan browser.
1. Pertama, kita buat file baru terlebih dahulu, contohnya namanya `embed.html`
2. Isi file html tersebut dengan kode yg kurang lebih seperti ini : 
    ```html
   <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
    
    </body>
    </html>
    ```
3. Dari workspace, klik button `Publish`. Pilih `Embed into site`. Copy semua kode tersebut ke file `embed.html` yang sudah dibuat sebelumnya. Dan paste di bawah tag `</body>`.
4. Tanya pertanyaan yang sama seperti diatas, dan kita lihat hasilnya.
 ```text
    Di event Google Cloud Roadshows x Build with AI Medan 2025, siapa saja speakernya?
 ```

Kalau mau nge custom widgetnya bisa dilihat di dokumentasinya di [Chat widget configuration](https://docs.langflow.org/concepts-publish#chat-widget-configuration)

---

Selain cara di atas, bisa juga menggunakan Node JS menggunakan library `langflow-client`, karena saya tidak simulasi caranya, bisa dicoba sendiri mengikuti video panduan
dari Langflownya di video [How to Use the Langflow API in Node.js](https://www.youtube.com/watch?v=DwvZzqj4tUc) ini.
