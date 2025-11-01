
# Serial Transfer of Single Byte / Character using 8051 (Keil)

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in Keil.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM

### (i) Serial Port Transfer a Single Character
vimal.a51
ORG 00HMOV TMOD, #20HMOV TH1, #0FDHMOV SCON, #50HSETB TR1 MOV SBUF, #'B'WAIT_TI:JNB TI, WAIT_TICLR TISJMP MAIN_LOOPEND 
vimalJ.C #include <reg51.h>void main() {TMOD = 0x20;TH1 = 0xFA;SCON = 0x50;TR1 = 1;while(1) {SBUF = 'A';while (TI == 0);TI = 0;} }

### (ii) Serial Port to Transfer a Message
vimal.a51
SCON=0X50;TR1=1;for(i-0;i<=12;i++){SBUF=msg[i];while(TI==0);TI=0;}while(1);}TANUJ.A51ORG 0000HMOV TMOD, #20HMOV TH1, #OFDHMOV SCON, #50HSETB TR1MOV A ,#'V'ACALL TRANSMOV A ,#'I'ACALL TRANSMOV A, #'M'ACALL TRANSMOV A, #'L'ACALL TRANSMOV A , #'L'ACALL TRANS SJMP $TRANS: MOV SBUF, AWAIT: JNB T1, WAITCLR T1RET END

### OUTPUT:
![WhatsApp Image 2025-11-01 at 08 58 15_731259a2](https://github.com/user-attachments/assets/7f2a4517-3e68-4a9f-a4de-b2c060fe5285)
![WhatsApp Image 2025-11-01 at 08 52 17_08a6810f](https://github.com/user-attachments/assets/fd777ebf-f917-4254-8174-649bacccabc5)


### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
