SayiTahminOyunu/
├── main.py
└── README.md
2. main.py kodu
python

import random

def oyun():
    gizli_sayi = random.randint(1, 100)
    deneme = 0

    print("🎮 SAYI TAHMİN OYUNU")
    print("1 ile 100 arasında bir sayı tuttum!")

    while True:
        try:
            tahmin = int(input("Tahminin: "))

            if not 1 <= tahmin <= 100:
                print("Lütfen 1 ile 100 arasında bir sayı gir.")
                continue

            deneme += 1

            if tahmin < gizli_sayi:
                print("Daha büyük bir sayı dene!")
            elif tahmin > gizli_sayi:
                print("Daha küçük bir sayı dene!")
            else:
                print(f"🎉 Tebrikler! {deneme} denemede buldun!")
                break

        except ValueError:
            print("Lütfen geçerli bir tam sayı gir.")

if __name__ == "__main__":
    oyun()
3. README.md kodu
markdown

# Sayı Tahmin Oyunu 🎮

Python ile geliştirilmiş basit bir sayı tahmin oyunu.

## Özellikler
- 1-100 arasında rastgele sayı
- Anlık ipuçları
- Hatalı giriş kontrolü
- Deneme sayacı

## Çalıştırma

Python 3 kurulu olmalıdır.

```bash
python main.py
```

## Lisans
MIT
