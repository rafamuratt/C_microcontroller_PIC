# C-Language 

 MURAT-TECH SORTER v.1.00
 By Rafa Muratt 03.2026
 Memory optimized 16x2 LCD HMI (4 bits mode) with full system control (core: PIC16F628A @4MHz, internal oscillator)
 
 MURAT-TECH CHANNEL: https://www.youtube.com/@Murat-TechChannel-EN
 MURAT-TECH HUB: https://murat-tech.eu/

 Runs continuosly a transport belt/ system, sorting objects in boxes with following conditions:
 - As long the emergency button is not active
 - As long objects are present and moving along the belt (not stuck)
 - As long the job counter is not finished
 - As long the user doesn't reset or power off
 - As long the ESC button is not pressed

 EEPROM AUTO SAVE (power loss recovery):
 - The counter of last full box
 - All parameter settings: Sort time (min & sec), max pices per box and max box quantity (job size)

 LIVE PARAMETERS UPDATE:
 - Sort time can be updated any time, no impact on the job process (for safety the transport belt stops while in settings page)
 - If quantities are updated (pieces per box or box quantitiy), all counters are reset and a new job start

 PARAMETERS
 Sorting time:     from 0 to 1 minute and 59 seconds  (Default: 3s)
 Objects count:    from 1 to 999 pieces               (Default: 5 pieces)
 Job size:         from 1 to 99 boxes                 (Default: 4 boxes)
 Objects timeout:  fixed parameter                    (Default: approx 30s)
 
 Note: ONE_SECOND definition has to be empirically fine tunned (to approx. 1 second) for correct 30s obj timeout


IDE: MiKroC Pro for PIC

Note: `MikroC_project`: Contains all IDE configuration and intermediate files.
HMI Screens.png shows all HMI pages and possible states (9 in total)
A copy of main C file is available in the main folder for easier visibility.


CAUTION:
According with IDE: 
"Used ROM (program words): 2034 (99%)  Free ROM (program words): 14 (1%) Used ROM (program words): 2034 (99%)  Free ROM (program words): 14 (1%)". Means the full memory is used. 
The code is stable but be aware IN NOT USING IN CRITICAL APPLICATION. DO IT AT YOUR OWN RISK


Project detais on https://murat-tech.eu/
