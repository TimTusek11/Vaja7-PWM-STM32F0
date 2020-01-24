# Vaja7-PWM-STM32F0

1. V levem Pinout oknu razširite nabor možnosti za časovnik TIM1. Clock Source nastavite kot Internal
Clock. Prvi kanal aktivirajte kot PWM Generation CH1. Kateri pin ste omogočili? Kaj se
izpiše poleg pina?

- PIN PA8.
- Izpise se TIM1_CH1.

2. V Configuration kliknemo TIM1 gumb. Vrednost Prescaler v zavihku Parameter Settinngs določite tako,
da bo časovnik delal s frekvenco 1 MHz. Koliko je vrednost Prescaler?

- Prescaler je vreden 16, da dobimo frekvenco 1 MHz.

3. Parameter Counter Period nastavimo na 100 in s tem še dodatno znižamo takt časovnika. Koliko znaša
sedaj?

- Sedaj znaša 10kHz.

4. Pulse (16 bits value) nastavite na 50. Kaj pomeni ta parameter? Namig – največja vrednost je lahko 100
odstotkov (znak za odstotek v polja ne pišemo).

- Ta parameter pomeni vrednost širine pulza.

5. Zapišite kaj počnejo ukazi v 1.,2. in 3. vrstici (v user code begin 3):

- Na začetku program nastavi htim1.Instance->CCR1 na vrednost spremenljivke dutyCycle.
- Vsakič ko gre program loopa skozi to vrstico doda spremenljivki dutyCycle + 10
- Preveri, če je vrednost dutyCycle-a večja od 90, če je, potem nastavi dutyCycle nazaj na 10 kar pomeni da je to neskončna zanka.
