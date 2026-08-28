# Line RC (inca n-am gasit nume)
## Structura 

Line RC este un robot line follower homebrew facut pentru Robochallange. Foloseste un ESP32 ca si microcontroller pentru avantajul de Update OTA, compatibilitatea cu majoritatea librariilor deja existente, simplitatea implementarii si pentru cele doua nuclee.
Design-ul urmareste o structura "prevazatoare", tintind spre redundanta, fara a compromite capacitatea de expansiune/depanare rapida/procesare.

## Bara de senzori

Bara de senzori este dezvoltata in jurul placilor XLINE de la JSumo, datorita rezilientei lor si a simplitatii design-ului. Bara este formata din 16 senzori IR conectati la un D/MUX analogic ce poate conecta fiecare dintre acestia direct la un pin ADC. Pe langa asta, bara mai dispune si de un connector FFC dar si de pini header de 2,54 mm.
Astfel, devenind compatibila cu barile XLINE si "detasata" de robot, design-ul putand fi folosit si cu alte placi de dezvoltare.

### Status:

- [x] PCB in mare parte
- [x] BOM
- [x] Schema
- [x] Foldere / subfoldere
- [ ] Gauri pentru tijele de suport
- [ ] Test points
- [ ] LED pentru status

## PCB Main

Este construit pentru compatibilitate cu acumulatori LiPO 2S1P, folosind mufe XT60. Placa are la dispozitie un port USB tip C pentru programare/debuggind, folosind un traductor de la USB la UART. Alimentarea circuitelor se poate face in doua moduri, fie folosind circuitul de buck intern, fie cel de pe ESC, selectia fiind facuta prin lipirea a unor pad-uri.
Avantajul acestei abordari este separarea datoriilor de OVP/OCP intre PCB si ESC, pentru a asigura ca si in cel mai nefavorabil caz, circuitul main inca poate fi folosit. Placa dispune si de un regulator liniar de 3.3V pentru a alimenta ESP-ul cat si o parte din electronica pentru achizitia de date (Bara de senzori). Desi ESP-ul are integrat un LDO, este mai usor/ieftin de schimbat un LDO decat un ESP.
Yappa yappa drivere yappa yappa motoare N20 yappa yappa turbina sau fara turbina yappa yappa

- [x] Schema
- [x] BOM
- [ ] PCB
- [ ] Test points
- [ ] Mufe extra pentru GPIO
- [ ] Gauri pentru tijele de suport
- [ ] Gaura pentru turbina
- [ ] Placement LiPo / ESC
- [ ] Roti
- [ ] LED Status
