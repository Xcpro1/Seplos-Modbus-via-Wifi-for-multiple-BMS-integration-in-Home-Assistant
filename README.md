Con questo progetto ho raccolto tutte le informazioni e le configurazioni necessarie per poter integrare direttamente i BMS Seplos, ma anche moltissimi altri conoscendone i protocolli ModBus, in Home Assistant. 

Cosa vi occorre?

- Un cavo LAN non switchato.

- un Elfwin EW11A (o similari)

- Ovviamente un BMS con protocollo ModBus 

Procediamo:

Tagliare il cavo lan e spellare  i cavi bianco-arancio e arancio- Collegare il primo al pin A e il secondo. Quindi collegarlo all'uscita RS485 del Seplos (vedi immagine).

Accedere al AP dell'Elfwin, andare su "others" e caricare il file di backup "EW11_Seplos", avendo cura di modificare l'indirizzo IP con il proprio assegnato dal vostro router. 

Impostare dal router l'IP dell'Elfwin come statico.

Inserire i file yaml alla root di Home Assistant, modificando il "configuration.yaml" con le stringhe del file "configuration..." allegato alla repository. 
