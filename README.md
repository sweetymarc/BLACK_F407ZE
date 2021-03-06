# Black STM32F407ZET6

MicroPython board definition files for the unbranded black STM32F407ZET6 dev board.

**Brand:** Unbranded/Generic

**Markings:** STM32F4XX STM32_F4XX V3.0 1606

![board](docs/STM32F407ZET6.jpg)

You can buy one for around $14 USD on [AliExpress](https://www.aliexpress.com/item/Free-shipping-STM32F407ZET6-development-board-M4-STM32F4-core-board-arm-development-board-cortex-M4/32689262341.html)

### Build and deploy the firmware:

* Clone the board definitions to your [MicroPython](https://github.com/micropython/micropython) ports/stm32/boards folder.

```
cd micropython/ports/stm32/boards
git clone https://github.com/mcauser/BLACK_F407ZE.git
```

* Disconnect the board from USB
* Set BOOT0 jumper to ON (BT0->3V3)
* Connect the board via USB

```
cd micropython/ports/stm32
make BOARD=BLACK_F407ZE
make BOARD=BLACK_F407ZE deploy
```

* Disconnect the board from USB
* Set BOOT0 jumper to OFF (BT0->GND)
* Connect the board via USB

```
$ screen /dev/tty.usbmodem1422
```

### Specifications:

* STM32F407ZET6 ARM Cortex M4
* 168MHz, 210 DMIPS / 1.25 DMIPS / MHz
* 1.8V - 3.6V operating voltage
* 8MHz system crystal
* 32.768KHz RTC crystal
* 2.54mm pitch pins
* JTAG/SWD header
* 512KByte Flash, 192 + 4 KByte SRAM
* 3x SPI, 3x USART, 2x UART, 2x I2S, 3x I2C
* 1x FSMC, 1x SDIO, 2x CAN
* 1x USB 2.0 FS / HS controller (with dedicated DMA)
* 1x USB HS ULPI (for external USB HS PHY)
* Micro SD
* Winbond W25Q16 16Mbit SPI Flash
* RTC battery CR1220
* 1MB SRAM footprint, unpopulated (IS62WV51216-1M)
* 1x 10/100 Ethernet MAC
* 1x 8 to 12-bit Parallel Camera interface
* 3x ADC (12-bit / 16-channel)
* 2x DAC (12-bit)
* 12x general timers, 2x advanced timers
* AMS1117-3.3V: 3.3V LDO voltage regulator, max current 800mA
* Micro USB for power and comms
* Yellow user LED D1 (PF9) active low
* Yellow user LED D2 (PF10) active low
* Yellow power LED D3
* 2x jumpers for bootloader selection
* Reset button, Wakeup button, 2x user buttons K0 (PE4) and K1 (PE3)
* 2x30 side pins + 2x16 bottom pins + 1x4 ISP pins
* 2x16 FMSC LCD Interface
* NRF24L01 socket
* M3 mounting holes
* Dimensions: 95.1mm x 74.6mm

### Modifications:

* change HSE_VALUE from 8000000 to 25000000
* change PLL_M from 8 to 25

### Links:

* [STM32F407ZE on st.com](http://www.st.com/content/st_com/en/products/microcontrollers/stm32-32-bit-arm-cortex-mcus/stm32-high-performance-mcus/stm32f4-series/stm32f407-417/stm32f407ze.html)
* [Buy on AliExpress](https://www.aliexpress.com/item/Free-shipping-STM32F407ZET6-development-board-M4-STM32F4-core-board-arm-development-board-cortex-M4/32689262341.html) or search for "STM32F407ZET6"
* [STM32F407ZET6 datasheet](https://github.com/mcauser/BLACK_F407ZE/blob/master/docs/STM32F407ZET6_datasheet.pdf)
* [STM32F407ZET6 schematics](https://github.com/mcauser/BLACK_F407ZE/blob/master/docs/STM32F407ZET6_schematics.pdf)
