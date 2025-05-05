# RGB Clock

Tento projekt zobrazuje aktuální čas na RGB LED matici pomocí Raspberry Pi Pico W a CircuitPythonu.  
Hodiny jsou synchronizované přes internet a aktualizují se automaticky, jednou za minutu se ukáže animace projíždějícího vlaku.

## Požadavky

- Raspberry Pi Pico W (doporučuji verzi WH s předdělaným pinoutem)
- Waveshare RGB LED Matrix 64×32 P4 ale může mít i jinou rozteč diod, např. 2.5mm
- CircuitPython (doporučená verze 9.0.0 nebo kompatibilní)
- Knihovny pro CircuitPython:
  - `adafruit_matrixportal`
  - `adafruit_display_text`
  - `adafruit_displayio_layout`
  - `adafruit_ntp`
  - a další potřebné knihovny (viz složka `lib/`)

## Funkce

- Automatická synchronizace času přes WiFi.
- Zobrazení hodin a minut na RGB LED matici.
- Barevné zobrazení číslic.
- každou minutu animace vlaku

## Poznámky

- Projekt je určen pro desku Raspberry Pi Pico W.
- RGB LED matice musí být kompatibilní s ovladačem HUB75.

## Zprovoznění
- Zapojte do zásuvky
- Připojte se přes hotspot, zadejte do prohlížeče 192.168.4.1 a nakonfigurujte wifi ke které se má raspberry pi připojit, pak se raspberry samo restartuje
- Na displeji se zobrazí synchronizované hodiny

## Vlastní instalace
Primárně zdroj: https://www.waveshare.com/wiki/RGB-Matrix-P2.5-64x32#Working_With_Raspberry_Pi_Pico
1. Nahraj CircuitPython uf2 file na Raspberry Pi Pico W.
2. Nakopíruj zdrojové soubory (`code.py` a složku `lib/`) na disk zařízení.
3. Připoj RGB matici k Pico W podle dokumentace výrobce výše.
4. Nakonfiguruj skrze hotspot (nebo do wifi.txt) na kterou wifi se má připojit
5. Restartuj zařízení – čas se automaticky načte a zobrazí.
