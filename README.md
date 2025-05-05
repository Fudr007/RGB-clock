# RGB Clock

Tento projekt zobrazuje aktuální čas na RGB LED matici pomocí Raspberry Pi Pico W a CircuitPythonu.  
Hodiny jsou synchronizované přes internet a aktualizují se automaticky.

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

## Poznámky

- Projekt je určen pro desku Raspberry Pi Pico W.
- RGB LED matice musí být kompatibilní s ovladačem HUB75.

## Zprovoznění
- Zapojte do zásuvky
- Připojte se přes bluetooth a nakonfigurujte wifi ke které se má raspberry pi připojit
- Na displeji se zobrazí synchronizované hodiny
- Pro pokročilejší konfiguraci (změna času, timer,...) přejděte na webovou stránku "doplnitWebStránku.cz"

## Vlastní instalace
Primárně: https://www.waveshare.com/wiki/RGB-Matrix-P2.5-64x32#Working_With_Raspberry_Pi_Pico
1. Nahraj CircuitPython na Raspberry Pi Pico W.
2. Nakopíruj zdrojové soubory (`code.py` a složku `lib/`) na disk zařízení.
3. Připoj RGB matici k Pico W podle dokumentace.
4. Nakonfiguruj skrze hotspot na kterou wifi se má připojit
5. Restartuj zařízení – čas se automaticky načte a zobrazí.
