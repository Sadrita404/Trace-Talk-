<div align="center">
  <table border="0" cellpadding="0" cellspacing="0">
    <tr>
      <td align="center" style="background: #ffffff; border: 1px solid #d0d7de; border-radius: 12px; padding: 16px; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">
        <img src="" width="100%" max-width="800px" alt="Rough Layout For The PCB" style="border-radius: 6px;" />
        <div style="margin-top: 12px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; font-size: 13px; color: #57606a; font-weight: 500;">
      </td>
    </tr>
  </table>
</div>


| Title | Trace Talk |
| :-- | :---|
|Author |Sadrita Neogi|

## What's this?

TraceTalk is a walkie-talkie small radio  powered by a custom PCB and an ATMEGA328P (Arduino) microcontroller. It features a built-in rechargeable battery that charges with any standard USB-C cable and power brick. I also put together a custom enclosure to keep the PCB safe.
## Why I built it ?

From a very starting point, I walkie talkie due to their principle of work like the transmission between two devices without any internet connection and we are able to talk to each other. This made me fascinated, and I also wanted to make one for myself, but in general, the walkie-talkie that we see is balki and heavy so I made it pocket size, slim, walkie-talkie that can be connected via headphone and we can use it.

## How to use ?

To use the walkie-talkie, just plug any headphones with a mic into the 3.5mm jack, then flip the switch on the left side of the board and the LED will turn on. Just press and hold the button on the board to transmit your voice, and any nearby walkie-talkies will pick it up and play the audio. No pairing or setup needed.

The battery will lasts for about 4 hours( according to my calculation that I have made by going to the data sheet of each components, and this is what I approximately estimated ) and charges with any USB-C cable and power source. While it's charging, an LED near the USB port will light up, and it'll turn off once the battery is fully charged. Just a heads-up: the headphones you use can affect the audio quality, so you might want to try a few different pairs to see what works best.


## Technical Description
This project runs on an ATMEGA328P microcontroller sitting on a custom PCB (TraceTalk). It sends all the audio data through an NRF24L01 radio module. The ATMEGA328P runs at 3.3V and 8MHz, and you can program it right through the Arduino IDE. While you could technically use an external programmer like a USBTinyISP, the Arduino IDE is definitely the easiest and most straightforward way to go.

For the radio, I used the SMD version of the NRF24L01 to keep the board as small as possible. It gets a maximum range of about 100 meters.

The LiPo battery is soldered straight onto the board's battery terminals. I’d recommend picking up a battery with a 100-150mAh capacity—that’s the sweet spot for getting the best results.


<div align="center">

| | Building Process | |
| :---: | :---: | :---: |
| <img src="https://github.com/user-attachments/assets/21229011-99ab-47b0-af64-b32a4537fa7f" width="100%" /> | <img src="https://github.com/user-attachments/assets/877ea42e-45ca-4cc2-b729-94c5ba9c5a93" width="100%" /> | <img src="https://github.com/user-attachments/assets/0e335cac-e2f7-49dc-9697-e55b6eff8da7" width="100%" /> |
| <img src="https://github.com/user-attachments/assets/7ea7322f-0e10-4a6d-9d60-a4e6e71f683e" width="100%" /> | <img src="https://github.com/user-attachments/assets/27fe0f33-f51a-4988-8de3-35e985724217" width="100%" /> | <img src="https://github.com/user-attachments/assets/4edec555-f9f7-4221-b8ee-0c4b1766f00f" width="100%" /> |
| <img src="https://github.com/user-attachments/assets/ad673f34-ba12-44f6-99f1-33ce8b79d85b" width="100%" /> | <img src="https://github.com/user-attachments/assets/54c83cc0-4afa-4cd0-914f-8b911a2370cf" width="100%" /> | <img src="https://github.com/user-attachments/assets/9e68fd51-9424-48f9-8847-189dfb406ee9" width="100%" /> |




<div align="center">
  <h2> Final Look </h2>
  <table border="0" cellpadding="10" cellspacing="0" style="border-collapse: collapse;">
    <tr>
      <!-- FRONT SIDE CARD -->
      <td align="center" valign="top" width="50%" style="background: #ffffff; border: 1px solid #d0d7de; border-radius: 12px; padding: 16px; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">
        <img src="https://github.com/user-attachments/assets/8e9e1b70-c7b3-4bd6-91c4-1aba6ea3785b" width="100%" alt="Front Side View" style="border-radius: 6px;" />
        <div style="margin-top: 12px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; font-size: 13px; color: #57606a; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px;">
          ▲ Front Side View
        </div>
      </td>
      <!-- SPACER FOR GITHUB MOBILE DEGRADATION -->
      <td width="2%">&nbsp;</td>
      <!-- BACK SIDE CARD -->
      <td align="center" valign="top" width="50%" style="background: #ffffff; border: 1px solid #d0d7de; border-radius: 12px; padding: 16px; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">
        <img src="https://github.com/user-attachments/assets/6d68a229-8a32-42cb-bf86-cb04ece2303d" width="100%" alt="Back Side View" style="border-radius: 6px;" />
        <div style="margin-top: 12px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; font-size: 13px; color: #57606a; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px;">
          ▲ Back Side View
        </div>
      </td>
    </tr>
  </table>
</div>
</div>



<div align="center">
  <h2> Bill of Materials </h2>
</div>

| Name | Purpose | Qty | Total (USD) | Link | Distributor |
| :--- | :--- | :---: | :---: | :---: | :--- |
| PCBA SMT Assembly | SMT assembly of all SMD components | 5 | 51.93 | — | JLCPCB |
| PCB Fabrication (Trace Talk) | 2-layer PCB — the board itself | 5 | 2.00 | — | JLCPCB |
| C10,C11,C3 | 100nF 50V X7R ±10% 0805 MLCC | 25 | 0.87 | [Link](https://lcsc.com/product-detail/C476766.html) | JLCPCB |
| D1,D2 | Red Water Clear 0805 LED Indication | 22 | 0.31 | [Link](https://lcsc.com/product-detail/C434431.html) | JLCPCB |
| J1 | 1A 3.5mm Headphone Jack 30V SMD R/A | 6 | 0.63 | [Link](https://lcsc.com/product-detail/C521460.html) | JLCPCB |
| J2 | 0.3mm 1mm 5P Right Angle Top Contact FFC/FPC Connector | 6 | 0.59 | [Link](https://lcsc.com/product-detail/C262360.html) | JLCPCB |
| R1,R5,R6 | 330Ω 125mW 150V Thick Film Resistor ±5% 0805 | 25 | 0.07 | [Link](https://lcsc.com/product-detail/C25306.html) | JLCPCB |
| R2,R3 | 5.1kΩ 125mW 150V Thick Film Resistor ±1% 0805 | 10 | 0.04 | [Link](https://lcsc.com/product-detail/C27834.html) | JLCPCB |
| R10,R4 | 1kΩ 125mW 150V Thick Film Resistor ±1% 0805 | 20 | 0.09 | [Link](https://lcsc.com/product-detail/C95781.html) | JLCPCB |
| R11,R12,R13,R7,R8,R9 | 10kΩ 125mW 150V Thick Film Resistor ±1% 0805 | 30 | 0.13 | [Link](https://lcsc.com/product-detail/C17414.html) | JLCPCB |
| C1,C2,C4,C5,C6,C8 | 10V 10uF X5R ±10% 0805 MLCC | 40 | 7.11 | [Link](https://lcsc.com/product-detail/C17024.html) | JLCPCB |
| SW1 | PCM12SMTR SPDT Surface Mount Vertical Slide Switch | 5 | 6.23 | [Link](https://lcsc.com/product-detail/C221841.html) | JLCPCB |
| SW2 | PTS645 Tactile Switches 12V 50mA SMD-4P 6x6mm | 5 | 1.53 | [Link](https://lcsc.com/product-detail/C221871.html) | JLCPCB |
| U2 | MIC5205-3.3YM5-TR Fixed 3.3V 150mA Linear LDO SOT-23-5 | 5 | 1.88 | [Link](https://lcsc.com/product-detail/C37970.html) | JLCPCB |
| U3 | TP4056X-42-ESOP8 1A 4.2V Lithium Battery Charging IC | 5 | 1.00 | [Link](https://lcsc.com/product-detail/C2763448.html) | JLCPCB |
| U4 | LM358DR2G 32V Dual Operational Amplifier SOIC-8 | 5 | 0.29 | [Link](https://lcsc.com/product-detail/C7950.html) | JLCPCB |
| U5 | ATMEGA328P-AU 8-Bit AVR 20MHz TQFP-32 Microcontroller | 5 | 11.38 | [Link](https://lcsc.com/product-detail/C14877.html) | JLCPCB |
| USB1 | USB Type-C Receptacle 16P Female SMD R/A | 5 | 0.92 | [Link](https://lcsc.com/product-detail/C165948.html) | JLCPCB |
| X1 | 8MHz 33pF SMD3213-3P Ceramic Resonator | 5 | 1.92 | [Link](https://lcsc.com/product-detail/C341522.html) | JLCPCB |
| RG1 | 470kΩ 125mW 150V Thick Film Resistor ±1% 0805 | 5 | 0.02 | [Link](https://lcsc.com/product-detail/C17709.html) | JLCPCB |
| C7,C9 | 330nF 50V X7R ±10% 0805 MLCC | 20 | 0.66 | [Link](https://lcsc.com/product-detail/C1740.html) | JLCPCB |
| 3.7V 100mAH | To power the circuit | 2 | 0.00 | [Link](https://www.electropi.in/3.7v-100mah-lipo-battery-model-321225-india) | Self Sourced |
| Shipping PCB	| E- Post (Cheapest) | 	- |	$10.98	| — | 	JLCPCB |
| Total |    |     |   $100.58    |   |    |   |

**I have provided the links to the parts that I will self - sourced , So that if a reader wanted to recreate this project they would be able to find all the parts.. Which is also updated on the BOM csv file too..**



Also I don't have any experience soldering SMD components. Since I don't own a hot plate,So I wouldn't be able to assemble it manually myself and finish the project. So, to stay within that $100 budget, I'm going with PCB assembly instead. And I will order 5 assemble PCB as I want two to get it tested and I want some extra to get in between the Channel and check it . Also getting 5 assembled PCB will cost $100 in total which is my allocated budget for this project Tier 3.

**Project Under Hack Club**



