---
description: Indica il motivo per cui un'operazione WLAN non è riuscita.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (wlanapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba0ae705244541063564431809cffa953a0f3fd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530163"
---
# <a name="wlan_reason_code"></a>\_codice motivo \_ WLAN

Il tipo di **\_ \_ codice motivo WLAN** indica il motivo per cui un'operazione WLAN non è riuscita.

È possibile usare la funzione [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) per eseguire il mapping di un codice motivo numerico (ad esempio, 0x00050007) al significato del testo. È anche possibile usare la tabella di ricerca per interpretare il valore numerico del codice motivo. Per visualizzare la tabella di ricerca, vedere Appendice E: mapping dei codici motivo ai messaggi di evento nel documento [risoluzione dei problemi relativi alle connessioni wireless di Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



Nella tabella seguente sono elencati i codici di errore generali.



| Codice motivo                 | Significato                            |
|-----------------------------|------------------------------------|
| \_ \_ \_ esito positivo codice per WLAN | L'operazione ha esito positivo.            |
| \_codice motivo \_ WLAN \_ sconosciuto | Il motivo dell'errore è sconosciuto. |



 

Nella tabella seguente sono elencati i codici di errore della configurazione automatica.



| Codice motivo                                  | Significato                                         |
|----------------------------------------------|-------------------------------------------------|
| \_ \_ rete codice motivo \_ WLAN \_ non \_ compatibile | La rete wireless non è compatibile.         |
| \_ \_ profilo codice motivo \_ WLAN \_ non \_ compatibile | Il profilo di rete wireless non è compatibile. |



 

Nella tabella seguente sono elencati i codici di errore di connessione automatici.



| Codice motivo                                                | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_codice motivo \_ WLAN \_ senza \_ \_ connessione automatica                   | Il profilo specifica nessuna connessione automatica.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_codice motivo \_ WLAN \_ non \_ visibile                           | La rete wireless non è visibile.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \_codice motivo \_ WLAN \_ \_ negato                             | La rete wireless è bloccata da criteri di gruppo.                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_codice motivo \_ WLAN \_ negato dall'utente \_                           | La rete wireless è bloccata dall'utente.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_codice motivo \_ WLAN \_ \_ \_ non \_ consentito per il tipo BSS                | Il tipo di Basic Service Set (BSS) non è consentito in questa scheda wireless.                                                                                                                                                                                                                                                                                                                                                                               |
| \_codice motivo \_ WLAN \_ in \_ \_ Elenco errori                       | La rete wireless si trova nell'elenco errori.                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_codice motivo \_ WLAN \_ nell' \_ \_ elenco bloccato                      | La rete wireless è nell'elenco bloccati.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_ \_ elenco SSID codice motivo WLAN \_ \_ \_ troppo \_ lungo                  | Le dimensioni dell'elenco degli identificatori del set di servizi (SSID) superano le dimensioni massime supportate dall'adapter.                                                                                                                                                                                                                                                                                                                                                  |
| \_chiamata di connessione del codice motivo WLAN \_ \_ \_ \_ non riuscita                    | La chiamata di connessione CSM (media Specific Module) non riesce.                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_chiamata di analisi del codice motivo WLAN \_ \_ \_ \_ non riuscita                       | La chiamata di analisi MSM ha esito negativo.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ rete codice motivo \_ WLAN \_ non \_ disponibile                | La rete specificata non è disponibile. Questo codice motivo viene utilizzato anche in caso di mancata corrispondenza tra le funzionalità specificate in un profilo XML e le funzionalità di rete e/o di interfaccia. Se, ad esempio, un profilo specifica l'uso di WPA2 quando la scheda di interfaccia di rete supporta solo WPA, viene restituito questo codice di errore. Inoltre, se un profilo specifica l'utilizzo della modalità FIPS quando la scheda di interfaccia di rete non supporta la modalità FIPS, viene restituito questo codice di errore.<br/> |
| \_ \_ profilo codice motivo \_ WLAN \_ modificato \_ o \_ eliminato          | Il profilo è stato modificato o eliminato prima che venisse stabilita la connessione.                                                                                                                                                                                                                                                                                                                                                                               |
| \_chiave codice motivo WLAN non \_ \_ \_ corrispondente                          | La chiave del profilo non corrisponde alla chiave di rete.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_codice motivo \_ WLAN \_ \_ non \_ risponde dall'utente                     | L'utente non risponde.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ \_ profilo AP del codice motivo WLAN \_ \_ non \_ consentito \_ per il \_ client | Un'applicazione ha tentato di applicare un profilo di rete wireless ospitato a una scheda di rete wireless fisica usando la funzione [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , invece che a un dispositivo virtuale.                                                                                                                                                                                                                                                    |
| \_ \_ profilo AP del codice motivo WLAN \_ \_ \_ non \_ consentito              | Un'applicazione ha tentato di applicare un profilo di rete wireless ospitato a una scheda di rete wireless fisica usando la funzione [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , invece che a un dispositivo virtuale.                                                                                                                                                                                                                                                    |



 

Nella tabella seguente sono elencati i codici di errore di convalida del profilo.



| Codice motivo                                                    | Significato                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_schema del \_ \_ profilo non valido per \_ il codice motivo \_ WLAN                   | Profilo non valido in base allo schema.                                                                                                                                                                                                  |
| \_ \_ profilo codice motivo \_ WLAN \_ mancante                           | Manca l'elemento WLANProfile.                                                                                                                                                                                                           |
| \_nome del \_ \_ profilo non valido nel codice \_ motivo WLAN \_                     | Il nome del profilo non è valido.                                                                                                                                                                                                           |
| \_tipo di \_ \_ profilo non valido per \_ il codice motivo \_ WLAN                     | Il tipo del profilo non è valido.                                                                                                                                                                                                           |
| \_tipo di \_ \_ PHY non valido nel codice \_ motivo WLAN \_                         | Il tipo PHY non è valido.                                                                                                                                                                                                                      |
| \_sicurezza del \_ codice MSM del codice per WLAN \_ \_ \_ mancante                     | Impostazioni di sicurezza MSM mancanti.                                                                                                                                                                                                        |
| \_codice motivo \_ WLAN \_ IHV \_ sicurezza \_ non \_ supportata              | Impostazioni di sicurezza del fornitore dell'hardware indipendente (IHV) mancanti.                                                                                                                                                                          |
| \_codice motivo \_ WLAN \_ IHV \_ oui non \_ corrispondente                         | Il profilo IHV OUI non corrisponde alla scheda OUI.                                                                                                                                                                                       |
| \_codice motivo \_ WLAN \_ IHV \_ Oui \_ mancante                          | Impostazioni IHV OUI mancanti.                                                                                                                                                                                                             |
| \_ \_ Impostazioni IHV del codice motivo WLAN \_ \_ \_ mancanti                     | Mancano le impostazioni di sicurezza IHV.                                                                                                                                                                                                        |
| \_codice motivo \_ WLAN \_ IHV \_ connettività \_ non \_ supportata          | Un'applicazione ha tentato di applicare un profilo IHV su una scheda che non supporta le impostazioni di connettività IHV.                                                                                                                                   |
| \_sicurezza dei \_ conflitti del codice per \_ la rete WLAN \_                         | Conflitto tra le impostazioni di sicurezza.                                                                                                                                                                                                               |
| \_sicurezza del codice per la rete WLAN \_ \_ \_ mancante                          | Impostazioni di sicurezza mancanti.                                                                                                                                                                                                            |
| \_tipo di \_ \_ BSS non valido nel codice \_ motivo WLAN \_                         | Il tipo BSS non è valido.                                                                                                                                                                                                                    |
| \_modalità di \_ \_ \_ connessione Adhoc non valida per il \_ codice \_ motivo WLAN           | Impossibile impostare la connessione automatica per una rete ad hoc.                                                                                                                                                                                     |
| \_codice motivo \_ WLAN \_ non \_ broadcast \_ impostato \_ per ad \_ hoc            | Impossibile impostare la non trasmissione per una rete ad hoc.                                                                                                                                                                                            |
| \_ \_ \_ \_ set di Commuter automatico del codice motivo WLAN \_ \_ per ad \_ hoc              | Non è possibile impostare l'opzione automatica per una rete ad hoc.                                                                                                                                                                                              |
| \_ \_ Switch automatico codice motivo WLAN \_ \_ \_ impostato \_ per \_ \_ connessione manuale | Non è possibile impostare l'opzione automatica per un profilo di connessione manuale.                                                                                                                                                                                    |
| \_codice motivo \_ WLAN \_ IHV \_ sicurezza \_ Onex \_ mancante               | Le impostazioni di sicurezza di IHV 802.1 X sono mancanti.                                                                                                                                                                                                 |
| \_ \_ SSID profilo codice motivo WLAN \_ \_ \_ non valido                     | SSID nel profilo non valido o mancante.                                                                                                                                                                                                |
| \_codice motivo \_ WLAN \_ troppi \_ \_ SSID                            | Nel profilo è stato specificato un numero eccessivo di SSID.                                                                                                                                                                                                 |
| \_codice motivo \_ WLAN \_ IHV \_ connettività \_ non \_ supportata          |                                                                                                                                                                                                                                               |
| \_codice motivo \_ WLAN \_ \_ numero massimo \_ di client non valido \_ \_ \_ per \_ AP     | Un'applicazione ha tentato di applicare un profilo di rete wireless ospitato a una scheda di interfaccia di rete fisica usando la funzione [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) e ha specificato un valore non accettabile per il numero massimo di client consentiti. |
| \_ \_ canale codice motivo WLAN \_ non valido \_                           | Il canale specificato non è valido.                                                                                                                                                                                                             |
| \_ \_ modalità operativa del codice motivo WLAN \_ \_ \_ non \_ supportata            |                                                                                                                                                                                                                                               |
| profilo punto di \_ \_ accesso automatico del codice motivo WLAN \_ \_ \_ \_ non \_ consentito            | Si è verificato un errore interno del sistema operativo nella rete ospitata senza fili.                                                                                                                                                                 |
| \_ \_ connessione automatica codice motivo WLAN \_ \_ \_ non \_ consentita             |                                                                                                                                                                                                                                               |



 

Nella tabella seguente sono elencati i codici di errore di incompatibilità della rete CSM.



| Codice motivo                                            | Significato                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| \_codice motivo \_ WLAN \_ \_ set di sicurezza non \_ supportato \_ dal \_ sistema operativo | Le impostazioni di sicurezza non sono supportate dal sistema operativo. |
| \_set di \_ \_ sicurezza non supportato dal \_ codice \_ motivo WLAN         | Le impostazioni di sicurezza non sono supportate.                         |
| \_codice motivo WLAN senza \_ \_ corrispondenza del \_ tipo BSS \_                 | Il tipo BSS non corrisponde.                                     |
| \_Tipo PHY del codice motivo WLAN non \_ \_ \_ \_ corrispondente                 | Il tipo PHY non corrisponde.                                     |
| \_codice motivo rete WLAN \_ \_ senza \_ corrispondenza                  | La velocità dei dati non corrisponde.                                    |



 

La tabella seguente elenca i codici di errore della connessione CSM.



| Codice motivo                                       | Significato                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| \_codice motivo \_ WLAN \_ \_ annullato dall'utente               | L'operazione è stata annullata dall'utente.                                                                             |
| \_errore di \_ \_ associazione codice motivo WLAN \_          | Driver disconnesso durante l'associazione.                                                                       |
| \_ \_ \_ timeout associazione codice motivo \_ WLAN          | Timeout dell'associazione.                                                                                       |
| \_errore di \_ pre \_ - \_ sicurezza del codice \_ per la rete WLAN        | Errore di sicurezza pre-associazione.                                                                            |
| \_errore di \_ \_ sicurezza di avvio codice motivo \_ WLAN \_      | Non è stato possibile avviare la sicurezza dopo l'associazione.                                                                  |
| \_errore di \_ sicurezza del codice per \_ la rete WLAN \_             | La protezione termina con un errore.                                                                               |
| \_ \_ \_ timeout sicurezza codice per \_ WLAN             | Timeout dell'operazione di sicurezza.                                                                                |
| \_errore di \_ roaming del codice per \_ \_ la rete WLAN              | Driver disconnesso durante il roaming.                                                                           |
| \_errore di \_ \_ sicurezza roaming \_ del \_ codice per la rete WLAN    | Non è stato possibile avviare la sicurezza per il roaming.                                                                        |
| \_codice motivo \_ WLAN \_ errore di sicurezza ad hoc \_ \_      | Non è stato possibile avviare la sicurezza per il peer ad hoc.                                                                    |
| \_driver di \_ codice motivo WLAN \_ \_ disconnesso          | Driver disconnesso.                                                                                         |
| \_ \_ \_ \_ errore operazione driver codice motivo \_ WLAN    | Il driver non è riuscito a eseguire alcune operazioni.                                                                    |
| \_codice motivo \_ WLAN \_ IHV \_ non \_ disponibile           | Il servizio IHV non è disponibile.                                                                            |
| \_codice motivo \_ WLAN \_ IHV \_ non \_ risponde          | Timeout della risposta da parte del servizio IHV.                                                                 |
| \_ \_ \_ Timeout disconnessione codice motivo WLAN \_           | Timeout durante l'attesa della disconnessione del driver.                                                              |
| \_ \_ \_ errore interno codice motivo \_ WLAN             | Un errore interno ha impedito il completamento dell'operazione.                                              |
| \_ \_ \_ timeout richiesta interfaccia utente \_ codice \_ motivo WLAN          | Si è verificato il timeout di una richiesta di interazione utente.                                                                        |
| \_ \_ \_ numero eccessivo di \_ tentativi di \_ sicurezza \_ per il codice WLAN | Roaming troppo spesso. La post-sicurezza non è stata completata dopo 5 tentativi.                                         |
| \_errore di \_ avvio del codice motivo WLAN \_ \_ \_         | Si è verificato un errore interno del sistema operativo che ha generato un errore durante l'avvio della rete ospitata senza fili. |



 

Nella tabella seguente sono elencati i codici di errore di sicurezza MSM.



| Codice motivo                                                             | Significato                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ \_ indice chiave non \_ valido                | L'indice di chiave specificato non è valido.                                                                                                                                                         |
| WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo \_ PSK \_ presente                       | Chiave obbligatoria, PSK presente.                                                                                                                                                                |
| \_lunghezza della \_ \_ chiave del \_ profilo MSMSEC per il codice \_ \_ WLAN                        | Lunghezza della chiave non valida.                                                                                                                                                                       |
| WLAN \_ reason \_ Code \_ MSMSEC \_ profilo \_ PSK \_ lunghezza                        | Lunghezza PSK non valida.                                                                                                                                                                       |
| WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo \_ Nessuna \_ crittografia di autenticazione \_ \_ specificata        | Nessuna coppia di autenticazione/crittografia specificata.                                                                                                                                                           |
| \_codice motivo WLAN MSMSEC è stato \_ \_ \_ \_ specificato un numero eccessivo di \_ \_ \_ crittografie di autenticazione \_ | Troppe coppie di autenticazione/crittografia specificate.                                                                                                                                                     |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ di \_ autenticazione duplicato \_            | Il profilo contiene una coppia di autenticazione/crittografia duplicata.                                                                                                                                              |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ RAWDATA \_ non valido                   | I dati non elaborati del profilo non sono validi.                                                                                                                                                              |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ di \_ autenticazione non valido \_              | Combinazione di autenticazione/crittografia non valida.                                                                                                                                                          |
| WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo \_ Onex \_ disabilitato                     | 802.1 x disabilitato quando è necessario abilitarlo.                                                                                                                                        |
| WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo \_ Onex \_ abilitato                      | 802.1 x abilitato quando è necessario disabilitarlo.                                                                                                                                        |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ \_ modalità PMKCACHE non \_ valida            | Modalità cache PMK non valida.                                                                                                                                                                   |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ non valido \_ PMKCACHE \_ dimensioni            | Dimensioni della cache PMK non valide.                                                                                                                                                                   |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ non valido \_ PMKCACHE \_ TTL             | TTL della cache PMK non valido.                                                                                                                                                                    |
| \_modalità di \_ \_ \_ \_ \_ preautenticazione non valida per il \_ codice motivo WLAN MSMSEC             | Modalità di preautenticazione non valida.                                                                                                                                                                     |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ di \_ limitazione della preautenticazione non valido \_         | Limitazione della preautenticazione non valida.                                                                                                                                                                 |
| \_ \_ il codice motivo WLAN MSMSEC è \_ \_ \_ \_ abilitato solo per la preautenticazione \_             | Preautenticazione abilitata quando la cache PMK è disabilitata.                                                                                                                                               |
| \_rete della \_ \_ funzionalità MSMSEC \_ del codice motivo WLAN \_                         | Corrispondenza funzionalità non riuscita alla rete.                                                                                                                                                    |
| scheda di interfaccia di rete della \_ \_ \_ funzionalità MSMSEC per codice motivo \_ WLAN \_                             | Corrispondenza funzionalità non riuscita nella scheda di interfaccia di rete.                                                                                                                                                        |
| \_ \_ \_ \_ profilo funzionalità MSMSEC del codice motivo WLAN \_                         | Corrispondenza funzionalità non riuscita nel profilo.                                                                                                                                                    |
| \_ \_ MSMSEC codice motivo \_ WLAN \_ \_ individuazione funzionalità                       | La rete non supporta il tipo di funzionalità specificato.                                                                                                                                       |
| WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo \_ passphrase \_ carattere                   | La passphrase contiene un carattere non valido.                                                                                                                                                    |
| WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo codice \_ \_ carattere                  | Il materiale della chiave contiene un carattere non valido.                                                                                                                                                  |
| \_codice motivo \_ WLAN \_ \_ profilo MSMSEC \_ errato \_ tipo di codice                     | Il tipo di chiave specificato non corrisponde al materiale della chiave.                                                                                                                                   |
| \_codice motivo \_ WLAN \_ MSMSEC \_ cella mista \_                                 | Si sospetta una cella mista. Il punto di accesso non segnala che è compatibile con un profilo abilitato per la privacy.                                                                                  |
| \_codice motivo WLAN-timer di autenticazione del \_ \_ \_ profilo MSMSEC \_ \_ \_ non valido              | Il numero di timer di autenticazione o il numero di timeout specificato nel profilo non è valido.                                                                                        |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ non valido \_ GKEY \_ INTV                | L'intervallo di aggiornamento della chiave di gruppo specificato nel profilo non è valido.                                                                                                                        |
| \_codice motivo \_ WLAN \_ MSMSEC \_ rete di transizione \_                         | Si sospetta una "rete di transizione". La sicurezza legacy 802,11 viene usata per il successivo tentativo di autenticazione.                                                                                  |
| \_codice motivo \_ WLAN \_ MSMSEC \_ chiave profilo non \_ \_ mappato \_                | La chiave contiene caratteri non inclusi nel set di caratteri ASCII.                                                                                                                      |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ autenticazione profilo \_ funzionalità                   | Corrispondenza funzionalità non riuscita perché la rete non supporta il metodo di autenticazione nel profilo.                                                                                 |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ crittografia profilo \_ funzionalità                 | Corrispondenza funzionalità non riuscita perché la rete non supporta l'algoritmo di crittografia nel profilo.                                                                                      |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ modalità sicura \_ profilo                         | Il valore della modalità FIPS 140-2 nel profilo non è valido.                                                                                                                                          |
| WLAN \_ \_ codice motivo \_ MSMSEC \_ \_ \_ modalità sicura profilo \_ funzionalità \_        | Il profilo richiede la modalità FIPS 140-2, che non è supportata da NIC (Network Interface Card).                                                                                                 |
| WLAN \_ \_ codice motivo \_ MSMSEC \_ \_ \_ modalità sicura profilo funzionalità \_ \_ NW         | Il profilo richiede la modalità FIPS 140-2, che non è supportata dalla rete.                                                                                                                      |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo di \_ autenticazione non supportato \_                  | Profile specifica un meccanismo di autenticazione non supportato.                                                                                                                               |
| \_codice motivo \_ WLAN \_ MSMSEC \_ profilo di \_ crittografia non supportato \_                | Profile specifica una crittografia non supportata.                                                                                                                                                  |
| \_codice motivo \_ WLAN \_ \_ \_ errore richiesta interfaccia utente MSMSEC \_                        | Non è stato possibile accodare la richiesta dell'interfaccia utente.                                                                                                                                               |
| WLAN \_ \_ codice motivo \_ MSMSEC \_ funzionalità della scheda di rete \_ MFP \_ NW \_                    | La LAN wireless richiede la protezione dei frame di gestione (MFP) e l'interfaccia di rete non supporta MFP. Per ulteriori informazioni, vedere la pagina relativa alla modifica IEEE 802.11 w allo standard 802,11. |



 

Nella tabella seguente sono elencati i codici di errore della connessione CSM.



| Codice motivo                                             | Significato                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ timeout avvio \_ autenticazione        | l'autenticazione 802.1 x non è stata avviata entro il tempo configurato.                                                      |
| \_ \_ MSMSEC codice motivo \_ WLAN \_ \_ timeout autenticazione riuscita \_      | autenticazione 802.1 x non completata entro il tempo configurato.                                                   |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ timeout avvio \_ chiave         | Lo scambio di chiavi dinamiche non è stato avviato entro il tempo configurato.                                                       |
| \_MSMSEC codice motivo rete WLAN- \_ \_ \_ \_ timeout chiave riuscita \_       | Lo scambio di chiavi dinamiche non è stato completato entro il tempo configurato.                                                    |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ M3 \_ - \_ dati chiave mancanti \_      | Il messaggio 3 dell'handshake a 4 vie non contiene dati chiave.                                                                    |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ M3 \_ mancante \_ IE             | Il messaggio 3 dell'handshake a 4 vie non ha IE.                                                                          |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ M3 \_ mancante \_ \_ chiave GRP       | Il messaggio 3 dell'handshake a 4 vie non ha una chiave GRP.                                                                     |
| \_codice motivo \_ WLAN \_ MSMSEC \_ - \_ corrispondenza IE PR \_            | Non è stato possibile abbinare le funzionalità di sicurezza di Internet Explorer in m3.                                                               |
| WLAN \_ \_ codice motivo \_ MSMSEC \_ sec \_ \_ corrispondenza IE           | Non è stato possibile abbinare le funzionalità di sicurezza dell'IE secondario in m3.                                                     |
| \_codice motivo \_ WLAN \_ MSMSEC \_ Nessuna \_ \_ chiave PAIRWISE           | È necessario un tasto pairwise, ma il punto di accesso (AP) ha configurato solo le chiavi di gruppo.                                        |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ G1 \_ \_ dati chiave \_ mancanti      | Il messaggio 1 dell'handshake della chiave di gruppo non contiene dati chiave.                                                                |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ G1 \_ mancante \_ \_ chiave GRP       | Il messaggio 1 dell'handshake della chiave di gruppo non ha una chiave di gruppo.                                                               |
| \_codice motivo \_ WLAN \_ MSMSEC il \_ peer \_ indicato non \_ sicuro   | Il bit di ripristino sicuro dopo la connessione è stato protetto.                                                                |
| \_codice motivo \_ WLAN \_ MSMSEC \_ nessun \_ autenticatore           | 802.1 x indica che non è presente alcun autenticatore, ma il profilo ne richiede uno.                                   |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ errore NIC                | Le impostazioni plumbing per la scheda NIC non è riuscita.                                                                                 |
| \_codice motivo \_ WLAN \_ MSMSEC \_ annullato                   | Operazione annullata da un chiamante.                                                                              |
| \_formato della \_ \_ chiave MSMSEC \_ del codice motivo WLAN \_                 | Il formato della chiave immessa non è valido.                                                                     |
| \_codice motivo \_ WLAN \_ \_ rilevato MSMSEC downgrade \_         | È stato rilevato un downgrade di sicurezza.                                                                               |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ mancata corrispondenza PSK \_ sospetta    | Si sospetta una mancata corrispondenza di PSK.                                                                                     |
| \_codice motivo \_ WLAN \_ MSMSEC \_ errore forzato \_             | Si è verificato un errore forzato perché il metodo di connessione non era protetto.                                         |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ M3 \_ troppi \_ \_ RSNIE        | Il messaggio 3 di handshake a 4 vie contiene troppi RSN IE (RSN).                                                     |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ m2 \_ \_ dati chiave \_ mancanti      | Il messaggio 2 dell'handshake a 4 vie non contiene dati chiave (RSN Adhoc).                                                        |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ m2 \_ mancante \_ IE             | Il messaggio 2 di handshake a 4 vie non ha IE (RSN Adhoc).                                                              |
| \_codice motivo \_ WLAN \_ MSMSEC \_ autenticazione \_ WCN \_ completata        |                                                                                                                  |
| \_codice motivo \_ WLAN \_ MSMSEC \_ \_ errore interfaccia utente sicurezza \_       | La richiesta dell'interfaccia utente di sicurezza non è riuscita perché la richiesta non è stata accodata o perché l'utente ha annullato la richiesta. |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ M3 \_ mancante \_ \_ chiave GRP \_ di MGMT | Il messaggio 3 di handshake a 4 vie non ha una chiave del gruppo MGMT (RSN).                                                        |
| \_Codice motivo \_ WLAN \_ MSMSEC \_ G1 \_ - \_ \_ chiave GRP \_ Mgmt mancante | Il messaggio 1 dell'handshake della chiave di gruppo non ha una chiave di gestione dei gruppi.                                                    |



 

Nella tabella seguente sono elencati i codici motivo 802.1 X. Gli elementi dello schema indicati di seguito sono definiti nello schema OneX e specificati nel profilo WLAN.



| Codice motivo                                         | Significato                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ONEX \_ non è \_ in grado di \_ identificare l' \_ utente                    | Nessun utente è disponibile per l'autenticazione 802.1 X. Questo errore può verificarsi quando l'autenticazione del computer è disabilitata e nessun utente è connesso al computer.                              |
| \_identità Onex \_ non \_ trovata                          | L'identità 802.1 X non è stata trovata.                                                                                                                                            |
| \_interfaccia utente di Onex \_ disabilitata                                  | L'autenticazione può essere completata solo tramite l'interfaccia utente e questa interfaccia non può essere visualizzata.                                                                       |
| \_errore EAP \_ Onex \_ ricevuto                        | Autenticazione EAP non riuscita.                                                                                                                                                     |
| ONEX \_ Authenticator \_ non è \_ più \_ presente            | L'autenticatore 802.1 X è andato fuori dalla rete.                                                                                                                               |
| \_versione del profilo Onex \_ \_ non \_ supportata              | La versione del profilo OneX fornita non è supportata.                                                                                                                         |
| \_lunghezza del profilo Onex \_ non valida \_                      | Lunghezza del profilo OneX non valida.                                                                                                                                            |
| \_ \_ tipo EAP non consentito dal profilo Onex \_ \_                | Il tipo EAP specificato nel profilo OneX (probabilmente fornito dall'elemento EAPType) non è consentito.                                                                               |
| \_il \_ \_ \_ tipo \_ o il \_ flag EAP del profilo Onex non è valido         | Il tipo EAP specificato nel profilo OneX (probabilmente fornito dall'elemento EAPType) non è valido o uno dei flag EAP (probabilmente forniti nell'elemento EAPConfig) non è valido. |
| \_flag Onex del profilo Onex \_ non validi \_ \_                 | I flag di supplicant (eventualmente forniti nell'elemento EAPConfig) nel profilo OneX non sono validi.                                                                                 |
| \_valore timer del profilo Onex \_ non valido \_ \_                | Un timer specificato nel profilo OneX (probabilmente fornito dall'elemento heldPeriod, authPeriod o startPeriod) non è valido.                                                        |
| \_ \_ \_ modalità supplicant del profilo Onex non valida \_            | La modalità supplicant specificata nel profilo OneX (probabilmente fornita dall'elemento supplicantMode) non è valida.                                                                    |
| \_modalità di autenticazione del profilo Onex \_ non valida \_ \_                  | La modalità di autenticazione specificata nel profilo OneX (probabilmente fornita dall'elemento authMode) non è valida.                                                                      |
| \_proprietà di \_ \_ connessione EAP \_ non valide del profilo Onex \_ | Le proprietà di connessione specificate nel profilo OneX (probabilmente fornito dall'elemento EAPConfig) non sono valide.                                                                  |



 

## <a name="remarks"></a>Commenti

Un set limitato di codici motivo è supportato in Windows XP con Service Pack 3 (SP3) e nell'API LAN wireless per Windows XP con Service Pack 2 (SP2). I codici di errore di convalida del profilo supportati in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2 sono i seguenti:

-   \_schema del \_ \_ profilo non valido per \_ il codice motivo \_ WLAN
-   \_ \_ profilo codice motivo \_ WLAN \_ mancante
-   \_ \_ SSID profilo codice motivo WLAN \_ \_ \_ non valido

I codici di errore di sicurezza MSM supportati in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2 sono i seguenti:

-   \_codice motivo \_ WLAN \_ MSMSEC \_ \_ \_ indice chiave non \_ valido
-   \_lunghezza della \_ \_ chiave del \_ profilo MSMSEC per il codice \_ \_ WLAN
-   WLAN \_ reason \_ Code \_ MSMSEC \_ profilo \_ PSK \_ lunghezza
-   \_codice motivo \_ WLAN \_ MSMSEC \_ profilo \_ di \_ autenticazione non valido \_
-   WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo \_ Onex \_ disabilitato
-   WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo \_ Onex \_ abilitato
-   \_rete della \_ \_ funzionalità MSMSEC \_ del codice motivo WLAN \_
-   scheda di interfaccia di rete della \_ \_ \_ funzionalità MSMSEC per codice motivo \_ WLAN \_
-   WLAN \_ motivo \_ codice \_ MSMSEC \_ profilo codice \_ \_ carattere
-   \_codice motivo \_ WLAN \_ \_ profilo MSMSEC \_ errato \_ tipo di codice

I codici di errore 802.1 x supportati in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2 sono i seguenti:

-   \_lunghezza del profilo Onex \_ non valida \_
-   \_il \_ \_ \_ tipo \_ o il \_ flag EAP del profilo Onex non è valido
-   \_modalità di autenticazione del profilo Onex \_ non valida \_ \_
-   \_proprietà di \_ \_ connessione EAP \_ non valide del profilo Onex \_

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wlanapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
