## Screenshots

<img src="screenshots/preview.png">

**Versão macOS suportada**: 13.* - 14.0
<br>
**Versão OpenCore**: 0.9.3
<br>
**Data de Lançamento**: 12/06/2023

## Especificações de hardware

|Item|Descrição|
|-|:-------:|
|CPU|Intel Core i5-6300U (Skylake)|
|Memória|8Gb DDR4|
|Armazenamento|NVMe SanDisk 256Gb|
|GPU|Intel(R) UHD Graphics 520|
|Ethernet|Intel I219-LM PCI-E Gigabit Ethernet Adapter|
|WLAN|Intel Wireless Gigabit Ethernet 802.11AC (M.2, 8260AC)|
|Bluetooth|Intel Bluetooth(R) 4.1|
|Áudio|Realtek ALC293 (ALC3235)|
|Tela|12,5" 60Hz|
|Webcam|USB Buil-in|
|Leitor de Cartão|USB Built-in|
|TouchPad & Teclado|HID I2C|

## O que esta funcionando?
- Audio
- HDMI/DP
- Todas as portas USB
- Ethernet
- Tudo relacionado ao iCloud (Drive, iMessage, Facetime, etc)
- Desligamento/reinicialização/atualização para versões mais recentes do macOS

## O que não esta funcionando?
- Wi-Fi
- E necessário usar o HeliPort + itlwm (incluso nas Kexts) até que a correção do AirportItlwm seja liberada.

## Obrigado/Créditos
- [Opencore Team](https://dortania.github.io/getting-started/)
- [OpenIntelWireless](https://github.com/OpenIntelWireless)
- [Acidanthera](https://github.com/acidanthera)
- [FireWolf](https://github.com/0xFireWolf/RealtekCardReader)
