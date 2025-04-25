# Install Langflow

Versi videonya bisa kamu lihat / click Youtube di bawah ini :

[![Exercise 0: Cara Install Langflow](https://img.youtube.com/vi/KPtFHbBm1I4/0.jpg)](https://www.youtube.com/watch?v=KPtFHbBm1I4&list=PLnyg3GbBr0YZdCyFGPrOebH_vhFMb9FeE&index=1)


Di sini kita bakal pakai `uv` buat install Langflow, karena kadang kalau pakai `pip` suka ada kendala.

Sebelum mulai, pastikan kamu udah install `uv` dan `python` di device kamu, sesuai yang dijelasin di bagian **prerequisites** di [readme.md](../../readme.md).

Disini kita menggunakan virtual environment (venv) untuk menghindari konflik dengan package lain yang mungkin udah terinstall di sistem kamu. Jadi, kita bakal bikin virtual environment baru dan aktifin itu sebelum install Langflow.
```bash
  uv venv
```
Aktifkan virtual environment yang udah kamu buat:
```bash
  source .venv/bin/activate # di Linux/Mac
  .venv\Scripts\activate # di Windows
```

Untuk install Langflow, cukup jalankan perintah ini di terminal:
```bash
  uv pip install langflow
```
Atau jika ingin menggunakan spesifik versi, bisa pakai perintah ini:
```bash
  uv pip install langflow==1.3.4 --force-reinstall
```

Kalau installnya berhasil, kamu bisa langsung jalanin Langflow dengan command ini:
```bash
  uv run langflow run
```

Setelah itu, buka browser kamu dan akses http://127.0.0.1:7860 buat lihat tampilan Langflow.

Untuk deaktifin virtual environment, kamu bisa pakai perintah ini:
```bash
  deactivate
```

Kalau ada masalah atau pengen lihat panduan lebih detail, atau kalau kamu lebih nyaman pakai `pip`, bisa langsung cek dokumentasi Langflow di sini (https://docs.langflow.org/get-started-installation#install-and-run-langflow-oss).


Versi videonya bisa kamu lihat di Youtube Exercise 0: Cara Install Langflow
[![Exercise 0: Cara Install Langflow](https://img.youtube.com/vi/KPtFHbBm1I4/0.jpg)](https://www.youtube.com/watch?v=KPtFHbBm1I4)
