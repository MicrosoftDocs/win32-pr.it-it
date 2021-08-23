---
description: Indica il motivo per cui un'operazione WLAN non è riuscita.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (Wlanapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f24b0ab902610408eb7b80b4a962fcc81d4598244714b8f30f0ebf350a7e628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064561"
---
# <a name="wlan_reason_code"></a>CODICE MOTIVO \_ \_ WLAN

Il **tipo WLAN \_ REASON \_ CODE** indica il motivo per cui un'operazione WLAN non è riuscita.

È possibile usare la [**funzione WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) per eseguire il mapping di un codice motivo numerico (ad esempio, 0x00050007) al significato del testo. È inoltre possibile utilizzare la tabella di ricerca per interpretare il valore numerico del codice motivo. Per visualizzare la tabella di ricerca, vedere Appendice E: Mapping dei codici motivo ai messaggi di evento nel documento Risoluzione dei problemi Windows [Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



Nella tabella seguente sono elencati i codici di errore generali.



| Codice motivo                 | Significato                            |
|-----------------------------|------------------------------------|
| CODICE MOTIVO WLAN \_ \_ \_ RIUSCITO | L'operazione ha esito positivo.            |
| CODICE MOTIVO WLAN \_ \_ \_ SCONOSCIUTO | Il motivo dell'errore è sconosciuto. |



 

Nella tabella seguente sono elencati i codici di errore di configurazione automatica.



| Codice motivo                                  | Significato                                         |
|----------------------------------------------|-------------------------------------------------|
| RETE DI CODICI MOTIVO WLAN \_ \_ NON \_ \_ \_ COMPATIBILE | La rete wireless non è compatibile.         |
| PROFILO DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ COMPATIBILE | Il profilo di rete wireless non è compatibile. |



 

Nella tabella seguente sono elencati i codici di errore di connessione automatica.



| Codice motivo                                                | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODICE MOTIVO WLAN \_ \_ NESSUNA CONNESSIONE \_ \_ \_ AUTOMATICA                   | Il profilo non specifica alcuna connessione automatica.                                                                                                                                                                                                                                                                                                                                                                                                               |
| CODICE MOTIVO WLAN \_ \_ NON \_ \_ VISIBILE                           | La rete wireless non è visibile.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ GP \_ DENIED                             | La rete wireless è bloccata da Criteri di gruppo.                                                                                                                                                                                                                                                                                                                                                                                                        |
| CODICE MOTIVO WLAN \_ \_ NEGATO \_ \_ DALL'UTENTE                           | La rete wireless è bloccata dall'utente.                                                                                                                                                                                                                                                                                                                                                                                                            |
| TIPO DI \_ CODICE MOTIVO \_ \_ WLAN BSS \_ NON \_ \_ CONSENTITO                | Il tipo di set di servizi di base (BSS) non è consentito in questa scheda wireless.                                                                                                                                                                                                                                                                                                                                                                               |
| CODICE MOTIVO WLAN \_ \_ \_ \_ NELL'ELENCO DEGLI ELEMENTI NON \_ RIUSCITI                       | La rete wireless si trova nell'elenco degli elementi non riusciti.                                                                                                                                                                                                                                                                                                                                                                                                             |
| CODICE MOTIVO WLAN \_ \_ \_ \_ NELL'ELENCO ELEMENTI \_ BLOCCATI                      | La rete wireless è in elenco elementi bloccati.                                                                                                                                                                                                                                                                                                                                                                                                            |
| ELENCO \_ \_ \_ SSID CODICE MOTIVO WLAN \_ TROPPO \_ \_ LUNGO                  | Le dimensioni dell'elenco degli identificatori del set di servizi (SSID) superano le dimensioni massime supportate dall'adapter.                                                                                                                                                                                                                                                                                                                                                  |
| CHIAMATA CONNECT DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ RIUSCITA                    | La chiamata di connessione di Media Specific Module (MSM) non riesce.                                                                                                                                                                                                                                                                                                                                                                                                     |
| CHIAMATA DI ANALISI DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ RIUSCITA                       | La chiamata di analisi MSM ha esito negativo.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| RETE DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ DISPONIBILE                | La rete specificata non è disponibile. Questo codice motivo viene usato anche in caso di mancata corrispondenza tra le funzionalità specificate in un profilo XML e le funzionalità di interfaccia e/o di rete. Ad esempio, se un profilo specifica l'uso di WPA2 quando la scheda di interfaccia di rete supporta solo WPA, viene restituito questo codice di errore. Inoltre, se un profilo specifica l'uso della modalità FIPS quando la scheda di interfaccia di rete non supporta la modalità FIPS, viene restituito questo codice di errore.<br/> |
| PROFILO DEL CODICE MOTIVO WLAN \_ \_ MODIFICATO O \_ \_ \_ \_ ELIMINATO          | Il profilo è stato modificato o eliminato prima che venga stabilita la connessione.                                                                                                                                                                                                                                                                                                                                                                               |
| CHIAVE DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ CORRISPONDENTE                          | La chiave del profilo non corrisponde alla chiave di rete.                                                                                                                                                                                                                                                                                                                                                                                                         |
| L'UTENTE DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ RISPONDE                     | L'utente non risponde.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| PROFILO AP DEL CODICE MOTIVO WLAN \_ NON CONSENTITO PER IL \_ \_ \_ \_ \_ \_ \_ CLIENT | Un'applicazione ha tentato di applicare un profilo di rete ospitata wireless a una scheda di rete wireless fisica utilizzando la funzione [**WlanSetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) anziché a un dispositivo virtuale.                                                                                                                                                                                                                                                    |
| PROFILO AP DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ \_ CONSENTITO              | Un'applicazione ha tentato di applicare un profilo di rete ospitata wireless a una scheda di rete wireless fisica utilizzando la funzione [**WlanSetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) anziché a un dispositivo virtuale.                                                                                                                                                                                                                                                    |



 

Nella tabella seguente sono elencati i codici di errore di convalida del profilo.



| Codice motivo                                                    | Significato                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCHEMA DEL PROFILO \_ NON VALIDO PER IL CODICE \_ \_ \_ MOTIVO \_ WLAN                   | Profilo non valido in base allo schema.                                                                                                                                                                                                  |
| PROFILO DEL CODICE MOTIVO WLAN \_ \_ \_ \_ MANCANTE                           | Elemento WLANProfile mancante.                                                                                                                                                                                                           |
| NOME PROFILO \_ NON VALIDO NEL CODICE \_ \_ \_ MOTIVO \_ WLAN                     | Il nome del profilo non è valido.                                                                                                                                                                                                           |
| TIPO DI PROFILO \_ NON VALIDO PER IL CODICE \_ \_ \_ MOTIVO \_ WLAN                     | Il tipo di profilo non è valido.                                                                                                                                                                                                           |
| TIPO DI \_ FISICO NON VALIDO PER IL CODICE \_ \_ \_ MOTIVO \_ WLAN                         | Il tipo PHY non è valido.                                                                                                                                                                                                                      |
| SICUREZZA \_ \_ MSM DEL CODICE \_ MOTIVO WLAN \_ \_ MANCANTE                     | Le impostazioni di sicurezza MSM non sono presenti.                                                                                                                                                                                                        |
| SICUREZZA \_ \_ \_ IHV DEL CODICE MOTIVO WLAN \_ NON \_ \_ SUPPORTATA              | Le impostazioni di sicurezza del fornitore di hardware indipendente (IHV) non sono presenti.                                                                                                                                                                          |
| MANCATA \_ CORRISPONDENZA \_ \_ OUI IHV DEL CODICE \_ MOTIVO WLAN \_                         | L'OUI del profilo IHV non corrisponde all'interfaccia OUI della scheda.                                                                                                                                                                                       |
| CODICE MOTIVO WLAN \_ \_ \_ IHV \_ OUI \_ MANCANTE                          | Le impostazioni OUI IHV non sono presenti.                                                                                                                                                                                                             |
| IMPOSTAZIONI \_ \_ \_ IHV DEL CODICE MOTIVO \_ WLAN \_ MANCANTI                     | Le impostazioni di sicurezza IHV sono mancanti.                                                                                                                                                                                                        |
| CONNETTIVITÀ \_ \_ \_ IHV DEL CODICE MOTIVO WLAN \_ \_ NON \_ SUPPORTATA          | Un'applicazione ha tentato di applicare un profilo IHV a una scheda che non supporta le impostazioni di connettività IHV.                                                                                                                                   |
| SICUREZZA DEI CONFLITTI \_ \_ DEL CODICE MOTIVO \_ WLAN \_                         | Le impostazioni di sicurezza sono in conflitto.                                                                                                                                                                                                               |
| SICUREZZA DEL CODICE MOTIVO WLAN \_ \_ \_ \_ MANCANTE                          | Impostazioni di sicurezza mancanti.                                                                                                                                                                                                            |
| CODICE MOTIVO WLAN \_ \_ TIPO \_ \_ BSS NON \_ VALIDO                         | Il tipo BSS non è valido.                                                                                                                                                                                                                    |
| MODALITÀ DI CONNESSIONE \_ \_ \_ \_ ADHOC NON VALIDA NEL CODICE MOTIVO \_ \_ WLAN           | Impossibile impostare la connessione automatica per una rete ad hoc.                                                                                                                                                                                     |
| CODICE MOTIVO WLAN \_ NON BROADCAST IMPOSTATO PER \_ \_ \_ \_ \_ \_ ADHOC            | Non è possibile impostare la non trasmissione per una rete ad hoc.                                                                                                                                                                                            |
| IMPOSTAZIONE DEL COMMUTATORE AUTOMATICO DEL CODICE MOTIVO WLAN \_ \_ PER \_ \_ \_ \_ \_ ADHOC              | Non è possibile impostare il commutatore automatico per una rete ad hoc.                                                                                                                                                                                              |
| IMPOSTAZIONE DEL COMMUTATORE AUTOMATICO DEL CODICE MOTIVO WLAN \_ \_ PER LA CONNESSIONE \_ \_ \_ \_ \_ \_ MANUALE | Non è possibile impostare il cambio automatico per un profilo di connessione manuale.                                                                                                                                                                                    |
| CODICE MOTIVO WLAN \_ \_ \_ IHV \_ SECURITY \_ ONEX \_ MANCANTE               | Le impostazioni di sicurezza IHV 802.1X sono mancanti.                                                                                                                                                                                                 |
| \_SSID DEL PROFILO DEL CODICE MOTIVO \_ \_ \_ WLAN NON \_ VALIDO                     | SSID nel profilo non valido o mancante.                                                                                                                                                                                                |
| CODICE MOTIVO WLAN \_ \_ TROPPI \_ \_ \_ SSID                            | Sono stati specificati troppi SSID nel profilo.                                                                                                                                                                                                 |
| LA \_ CONNETTIVITÀ \_ \_ IHV DEL CODICE MOTIVO WLAN \_ \_ NON È \_ SUPPORTATA          |                                                                                                                                                                                                                                               |
| CODICE MOTIVO WLAN \_ NUMERO MASSIMO DI CLIENT NON VALIDO \_ PER \_ \_ \_ \_ \_ \_ AP \_     | Un'applicazione ha provato ad applicare un profilo di rete ospitata wireless a una scheda di rete fisica usando la funzione [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) e ha specificato un valore inaccettabile per il numero massimo di client consentiti. |
| CODICE MOTIVO WLAN \_ \_ CANALE NON \_ \_ VALIDO                           | Il canale specificato non è valido.                                                                                                                                                                                                             |
| MODALITÀ DI FUNZIONAMENTO DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ \_ SUPPORTATA            |                                                                                                                                                                                                                                               |
| PROFILO AP AUTOMATICO DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ \_ \_ CONSENTITO            | Si è verificato un errore interno del sistema operativo con la rete ospitata wireless.                                                                                                                                                                 |
| CONNESSIONE AUTOMATICA DEL CODICE MOTIVO WLAN \_ \_ NON \_ \_ \_ \_ CONSENTITA             |                                                                                                                                                                                                                                               |



 

Nella tabella seguente sono elencati i codici di errore di incompatibilità di rete MSM.



| Codice motivo                                            | Significato                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| CODICE MOTIVO WLAN \_ \_ SICUREZZA NON SUPPORTATA \_ \_ \_ \_ IMPOSTATA DAL SISTEMA \_ OPERATIVO | Le impostazioni di sicurezza non sono supportate dal sistema operativo. |
| CODICE MOTIVO WLAN \_ SET DI SICUREZZA NON \_ \_ \_ \_ SUPPORTATO         | Le impostazioni di sicurezza non sono supportate.                         |
| CODICE MOTIVO WLAN \_ \_ \_ BSS \_ TYPE \_ UNMATCH                 | Il tipo BSS non corrisponde.                                     |
| WLAN \_ REASON \_ CODE \_ PHY \_ TYPE \_ UNMATCH                 | Il tipo PHY non corrisponde.                                     |
| CODICE MOTIVO WLAN \_ \_ : \_ DATARATE \_ UNMATCH                  | La frequenza dei dati non corrisponde.                                    |



 

Nella tabella seguente sono elencati i codici di errore di connessione MSM.



| Codice motivo                                       | Significato                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| CODICE MOTIVO WLAN \_ \_ \_ \_ ANNULLATO DALL'UTENTE               | L'utente ha annullato l'operazione.                                                                             |
| ERRORE DI ASSOCIAZIONE \_ \_ DEL CODICE MOTIVO \_ \_ WLAN          | Driver disconnesso durante l'associazione.                                                                       |
| TIMEOUT ASSOCIAZIONE \_ \_ CODICE MOTIVO \_ WLAN \_          | Timeout dell'associazione.                                                                                       |
| ERRORE DI SICUREZZA \_ \_ PRELIMINARE DEL CODICE MOTIVO \_ \_ \_ WLAN        | Errore di sicurezza pre-associazione.                                                                            |
| ERRORE DI SICUREZZA \_ \_ DI AVVIO CODICE MOTIVO \_ \_ WLAN \_      | Impossibile avviare la sicurezza dopo l'associazione.                                                                  |
| ERRORE DI \_ SICUREZZA DEL CODICE MOTIVO \_ \_ \_ WLAN             | La sicurezza finisce con un errore.                                                                               |
| TIMEOUT DI \_ SICUREZZA \_ DEL CODICE MOTIVO \_ WLAN \_             | Timeout dell'operazione di sicurezza.                                                                                |
| ERRORE DI ROAMING \_ \_ DEL CODICE MOTIVO \_ WLAN \_              | Driver disconnesso durante il roaming.                                                                           |
| ERRORE DI SICUREZZA \_ DEL ROAMING DEL CODICE \_ MOTIVO \_ \_ WLAN \_    | Impossibile avviare la sicurezza per il roaming.                                                                        |
| ERRORE DI \_ SICUREZZA \_ \_ ADHOC DEL CODICE \_ \_ MOTIVO WLAN      | Impossibile avviare la sicurezza per il peer ad hoc.                                                                    |
| DRIVER DEL \_ CODICE MOTIVO \_ WLAN \_ \_ DISCONNESSO          | Driver disconnesso.                                                                                         |
| ERRORE DELL'OPERAZIONE \_ DEL DRIVER DEL CODICE MOTIVO \_ \_ \_ \_ WLAN    | Il driver non è riuscito a eseguire alcune operazioni.                                                                    |
| CODICE MOTIVO WLAN \_ \_ \_ IHV \_ NON \_ DISPONIBILE           | Il servizio IHV non è disponibile.                                                                            |
| IL CODICE MOTIVO WLAN \_ \_ \_ IHV \_ NON \_ RISPONDE          | Timeout della risposta dal servizio IHV.                                                                 |
| TIMEOUT \_ DISCONNESSIONE \_ CODICE MOTIVO \_ WLAN \_           | Timeout in attesa della disconnessione del driver.                                                              |
| ERRORE INTERNO \_ DEL \_ CODICE MOTIVO \_ \_ WLAN             | Un errore interno ha impedito il completamento dell'operazione.                                              |
| TIMEOUT DELLA RICHIESTA \_ \_ DELL'INTERFACCIA UTENTE DEL CODICE \_ MOTIVO \_ \_ WLAN          | Timeout di una richiesta di interazione dell'utente.                                                                        |
| CODICE MOTIVO WLAN \_ \_ TROPPI \_ \_ TENTATIVI DI \_ \_ SICUREZZA | Roaming troppo spesso. La post-sicurezza non è stata completata dopo 5 tentativi.                                         |
| ERRORE DI AVVIO \_ DEL \_ CODICE MOTIVO \_ \_ \_ WLAN         | Si è verificato un errore interno del sistema operativo che ha comportato un errore di avvio della rete ospitata wireless. |



 

Nella tabella seguente sono elencati i codici di errore di sicurezza MSM.



| Codice motivo                                                             | Significato                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INDICE DI \_ CHIAVE NON VALIDO DEL PROFILO \_ \_ MSMSEC \_ \_ \_ \_ DEL CODICE MOTIVO WLAN                | L'indice della chiave specificato non è valido.                                                                                                                                                         |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PSK \_ PRESENT                       | Chiave obbligatoria, PSK presente.                                                                                                                                                                |
| LUNGHEZZA CHIAVE DEL \_ \_ PROFILO \_ MSMSEC \_ \_ \_ DEL CODICE MOTIVO WLAN                        | Lunghezza della chiave non valida.                                                                                                                                                                       |
| LUNGHEZZA PSK DEL PROFILO \_ \_ \_ MSMSEC \_ DEL \_ \_ CODICE MOTIVO WLAN                        | Lunghezza PSK non valida.                                                                                                                                                                       |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ NO \_ AUTH \_ CIPHER \_ SPECIFIED        | Nessuna coppia di autenticazione/crittografia specificata.                                                                                                                                                           |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ TOO \_ MANY \_ AUTH \_ CIPHER \_ SPECIFIED | Troppe coppie di autenticazione/crittografia specificate.                                                                                                                                                     |
| CODICE MOTIVO \_ \_ WLAN: CRITTOGRAFIA \_ \_ DUPLICATA \_ \_ DELL'AUTENTICAZIONE \_ DEL PROFILO MSMSEC            | Il profilo contiene una coppia di autenticazione/crittografia duplicata.                                                                                                                                              |
| CODICE MOTIVO \_ \_ WLAN: IL PROFILO \_ MSMSEC \_ \_ RAWDATA NON \_ È VALIDO                   | I dati non elaborati del profilo non sono validi.                                                                                                                                                              |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ AUTH \_ CIPHER              | Combinazione di autenticazione/crittografia non valida.                                                                                                                                                          |
| CODICE MOTIVO WLAN \_ \_ PROFILO \_ MSMSEC \_ \_ ONEX \_ DISABILITATO                     | 802.1X disabilitato quando è necessario attivarlo.                                                                                                                                        |
| CODICE MOTIVO WLAN \_ \_ PROFILO \_ MSMSEC \_ \_ ONEX \_ ABILITATO                      | 802.1X abilitato quando è necessario che sia disabilitato.                                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE INVALID \_ \_ PMKCACHE MODE (MODALITÀ PMKCACHE NON VALIDA PER IL PROFILO \_ MSMSEC)            | Modalità cache PMK non valida.                                                                                                                                                                   |
| DIMENSIONI \_ \_ \_ \_ \_ \_ PMKCACHE NON VALIDE DEL PROFILO MSMSEC \_ DEL CODICE MOTIVO WLAN            | Dimensioni della cache PMK non valide.                                                                                                                                                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PMKCACHE \_ TTL             | TTL della cache PMK non valida.                                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PREAUTH \_ MODE             | Modalità di preautentura non valida.                                                                                                                                                                     |
| LIMITAZIONE PREAUTENTICAZIONE \_ \_ \_ PREAUTENTICAZIONE PROFILO MSMSEC \_ \_ \_ \_ NON VALIDA PER IL CODICE MOTIVO WLAN         | Limitazione di preautenticazione non valida.                                                                                                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PREAUTH \_ ONLY \_ ENABLED             | Preautentura abilitata quando la cache PMK è disabilitata.                                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NETWORK                         | La corrispondenza delle funzionalità non è riuscita in rete.                                                                                                                                                    |
| SCHEDA DI INTERFACCIA DI RETE \_ \_ DELLA FUNZIONALITÀ \_ MSMSEC DEL \_ \_ CODICE MOTIVO WLAN                             | Corrispondenza delle funzionalità non riuscita nella scheda di interfaccia di rete.                                                                                                                                                        |
| PROFILO FUNZIONALITÀ \_ \_ MSMSEC DEL CODICE MOTIVO \_ WLAN \_ \_                         | Corrispondenza delle funzionalità non riuscita nel profilo.                                                                                                                                                    |
| INDIVIDUAZIONE FUNZIONALITÀ \_ \_ MSMSEC DEL CODICE MOTIVO \_ WLAN \_ \_                       | La rete non supporta il tipo di funzionalità specificato.                                                                                                                                       |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ PASSPHRASE \_ CHAR                   | La passphrase contiene un carattere non valido.                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR                  | Il materiale della chiave contiene un carattere non valido.                                                                                                                                                  |
| CODICE MOTIVO WLAN: TIPO DI \_ \_ CHIAVE \_ ERRATO DEL \_ \_ PROFILO MSMSEC \_                     | Il tipo di chiave specificato non corrisponde al materiale della chiave.                                                                                                                                   |
| CELLA MISTA MSMSEC DEL CODICE MOTIVO \_ \_ \_ WLAN \_ \_                                 | Si sospetta una cella mista. Il punto di accesso non segnala che è compatibile con un profilo abilitato per la privacy.                                                                                  |
| IL CODICE \_ MOTIVO WLAN \_ \_ MSMSEC \_ PROFILE \_ AUTH \_ TIMERS INVALID (TIMER \_ DI AUTENTICAZIONE PROFILO MSMSEC NON VALIDI)              | Il numero di timer di autenticazione o il numero di timeout specificati nel profilo non è valido.                                                                                        |
| CODICE MOTIVO \_ \_ WLAN: PROFILO \_ MSMSEC \_ NON VALIDO \_ \_ \_ INTV                | L'intervallo di aggiornamento della chiave di gruppo specificato nel profilo non è valido.                                                                                                                        |
| CODICE MOTIVO WLAN \_ \_ RETE DI TRANSIZIONE \_ MSMSEC \_ \_                         | Si sospetta una "rete di transizione". La sicurezza legacy 802.11 viene usata per il tentativo di autenticazione successivo.                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEY \_ UNMAPPED \_ CHAR                | La chiave contiene caratteri non presenti nel set di caratteri ASCII.                                                                                                                      |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ AUTH                   | La corrispondenza delle funzionalità non è riuscita perché la rete non supporta il metodo di autenticazione nel profilo.                                                                                 |
| CRITTOGRAFIA DEL \_ PROFILO \_ DI FUNZIONALITÀ \_ MSMSEC \_ DEL \_ \_ CODICE MOTIVO WLAN                 | La corrispondenza delle funzionalità non è riuscita perché la rete non supporta l'algoritmo di crittografia nel profilo.                                                                                      |
| WLAN REASON CODE MSMSEC PROFILE SAFE MODE (MODALITÀ SICURA \_ \_ PROFILO \_ MSMSEC CON CODICE MOTIVO \_ WLAN) \_ \_                         | Il valore della modalità FIPS 140-2 nel profilo non è valido.                                                                                                                                          |
| SCHEDA DI INTERFACCIA DI RETE IN MODALITÀ \_ \_ SICURA PROFILO FUNZIONALITÀ \_ MSMSEC \_ \_ DEL \_ \_ \_ CODICE MOTIVO WLAN        | Il profilo richiede la modalità FIPS 140-2, che non è supportata dalla scheda di interfaccia di rete (NIC).                                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ SAFE \_ MODE \_ NW         | Il profilo richiede la modalità FIPS 140-2, che non è supportata dalla rete.                                                                                                                      |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ UNSUPPORTED \_ AUTH                  | Il profilo specifica un meccanismo di autenticazione non supportato.                                                                                                                               |
| CRITTOGRAFIA NON \_ \_ SUPPORTATA DEL PROFILO \_ MSMSEC \_ DEL \_ \_ CODICE MOTIVO WLAN                | Il profilo specifica una crittografia non supportata.                                                                                                                                                  |
| ERRORE DI RICHIESTA \_ \_ \_ DELL'INTERFACCIA UTENTE MSMSEC \_ CON CODICE MOTIVO \_ \_ WLAN                        | Impossibile accodare la richiesta dell'interfaccia utente.                                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ MFP \_ NW \_ NIC                    | La rete LAN wireless richiede Protezione frame di gestione (MFP) e l'interfaccia di rete non supporta MFP. Per altre informazioni, vedere la modifica IEEE 802.11w dello standard 802.11. |



 

Nella tabella seguente sono elencati i codici di errore di connessione MSM.



| Codice motivo                                             | Significato                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ START \_ TIMEOUT        | L'autenticazione 802.1X non è stata avviata entro il tempo configurato.                                                      |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ SUCCESS \_ TIMEOUT      | L'autenticazione 802.1X non è stata completata entro il tempo configurato.                                                   |
| TIMEOUT DI \_ AVVIO \_ CHIAVE \_ MSMSEC DEL CODICE MOTIVO WLAN \_ \_ \_         | Lo scambio dinamico delle chiavi non è stato avviato entro il tempo configurato.                                                       |
| TIMEOUT CHIAVE \_ \_ \_ MSMSEC CHIAVE MSMSEC \_ CON \_ \_ CODICE MOTIVO WLAN       | Lo scambio dinamico delle chiavi non è stato completato entro il tempo configurato.                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M3 \_ MISSING \_ KEY \_ DATA      | Il messaggio 3 dell'handshake a 4 way non contiene dati di chiave.                                                                    |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ M3 \_ \_ MANCANTE IE             | Il messaggio 3 dell'handshake a 4 way non ha IE.                                                                          |
| CHIAVE \_ \_ \_ GRP MANCANTE MSMSEC \_ M3 \_ \_ CON CODICE MOTIVO \_ WLAN       | Il messaggio 3 dell'handshake a 4 way non ha una chiave GRP.                                                                     |
| CORRISPONDENZA \_ \_ \_ MSMSEC \_ PR \_ IE CON \_ CODICE MOTIVO WLAN            | La corrispondenza delle funzionalità di sicurezza di Internet Intelligence in M3 non è riuscita.                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ SEC \_ IE \_ MATCHING           | La corrispondenza delle funzionalità di sicurezza di Internet Intelligence secondario in M3 non è riuscita.                                                     |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ NO \_ PAIRWISE \_ KEY           | È necessaria una chiave pairwise, ma il punto di accesso (AP) ha configurato solo le chiavi di gruppo.                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC G1 MISSING KEY DATA (DATI CHIAVE MANCANTI MSMSEC G1 PER IL \_ CODICE MOTIVO \_ \_ \_ WLAN)      | Il messaggio 1 dell'handshake della chiave di gruppo non contiene dati di chiave.                                                                |
| CHIAVE \_ \_ \_ GRP MANCANTE NEL CODICE MOTIVO WLAN MSMSEC \_ G1 \_ \_ \_       | Il messaggio 1 dell'handshake della chiave di gruppo non ha una chiave di gruppo.                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PEER \_ INDICATED \_ INSECURE   | Ap reset secure bit after connection was secured.                                                                |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ NO \_ AUTHENTICATOR           | 802.1X indica che non è presente alcun autenticatore, ma il profilo ne richiede uno.                                   |
| ERRORE DELLA \_ SCHEDA DI INTERFACCIA DI RETE \_ \_ MSMSEC DEL CODICE MOTIVO WLAN \_ \_                | L'esecuzione del plumbing delle impostazioni sulla scheda di interfaccia di rete non è riuscita.                                                                                 |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ ANNULLATO                   | Operazione annullata da un chiamante.                                                                              |
| FORMATO DELLA \_ CHIAVE \_ MSMSEC DEL CODICE MOTIVO \_ WLAN \_ \_                 | Il formato della chiave immesso non è valido.                                                                     |
| RILEVATO \_ \_ \_ DOWNGRADE MSMSEC \_ DEL \_ CODICE MOTIVO WLAN         | È stato rilevato un downgrade della sicurezza.                                                                               |
| SOSPETTA \_ MANCATA \_ CORRISPONDENZA DEL CODICE MOTIVO \_ WLAN \_ MSMSEC PSK \_ \_    | Si sospetta una mancata corrispondenza PSK.                                                                                     |
| ERRORE \_ FORZATO \_ MSMSEC DEL CODICE MOTIVO \_ WLAN \_ \_             | Si è verificato un errore forzato perché il metodo di connessione non era sicuro.                                         |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ M3 \_ TOO MANY \_ \_ RSNIE        | Il messaggio 3 di 4 way handshake contiene troppi RSN IE (RSN).                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ M2 \_ MISSING \_ KEY \_ DATA      | Il messaggio 2 dell'handshake a 4 modalità non contiene dati di chiave (adhoc RSN).                                                        |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ M2 \_ \_ MANCANTE IE             | Il messaggio 2 di 4 way handshake non ha IE (RSN Adhoc).                                                              |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ WCN \_ COMPLETED        |                                                                                                                  |
| ERRORE \_ DELL'INTERFACCIA \_ UTENTE DI SICUREZZA \_ MSMSEC DEL CODICE MOTIVO WLAN \_ \_ \_       | La richiesta dell'interfaccia utente di sicurezza non è riuscita perché non è stato possibile accodarlo o perché l'utente ha annullato la richiesta. |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ M3 \_ MANCANTE \_ CHIAVE \_ GRP MGMT \_ | Il messaggio 3 di 4 way handshake non ha una chiave di gruppo Mgmt (RSN).                                                        |
| CODICE MOTIVO WLAN \_ \_ \_ MSMSEC \_ G1 \_ MANCANTE \_ CHIAVE \_ GRP MGMT \_ | Il messaggio 1 dell'handshake della chiave di gruppo non ha una chiave di gestione del gruppo.                                                    |



 

Nella tabella seguente sono elencati i codici motivo 802.1X. Gli elementi dello schema denominati di seguito sono definiti nello schema OneX e specificati nel profilo WLAN.



| Codice motivo                                         | Significato                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ONEX \_ NON È IN GRADO DI IDENTIFICARE \_ \_ \_ L'UTENTE                    | Nessun utente è disponibile per l'autenticazione 802.1X. Questo errore può verificarsi quando l'autenticazione del computer è disabilitata e nessun utente è connesso al computer.                              |
| IDENTITÀ ONEX \_ \_ NON \_ TROVATA                          | Impossibile trovare l'identità 802.1X.                                                                                                                                            |
| INTERFACCIA UTENTE ONEX \_ \_ DISABILITATA                                  | L'autenticazione può essere completata solo tramite l'interfaccia utente e questa interfaccia non può essere visualizzata.                                                                       |
| ERRORE \_ ONEX EAP \_ \_ RICEVUTO                        | L'autenticazione EAP non è riuscita.                                                                                                                                                     |
| ONEX \_ AUTHENTICATOR \_ NON È PIÙ \_ \_ PRESENTE            | L'autenticatore 802.1X è stato rimosso dalla rete.                                                                                                                               |
| VERSIONE DEL PROFILO ONEX \_ \_ NON \_ \_ SUPPORTATA              | La versione del profilo OneX fornita non è supportata.                                                                                                                         |
| LUNGHEZZA DEL PROFILO ONEX \_ \_ NON \_ VALIDA                      | La lunghezza del profilo OneX non è valida.                                                                                                                                            |
| TIPO EAP ONEX \_ PROFILE \_ NON \_ \_ CONSENTITO                | Il tipo EAP specificato nel profilo OneX (possibilmente fornito dall'elemento EAPType) non è consentito.                                                                               |
| TIPO \_ \_ EAP O FLAG ONEX PROFILE NON \_ \_ \_ \_ VALIDO         | Il tipo EAP specificato nel profilo OneX (possibilmente fornito dall'elemento EAPType) non è valido oppure uno dei flag EAP (eventualmente forniti nell'elemento EAPConfig) non è valido. |
| FLAG ONEX \_ ONEX PROFILE \_ INVALID \_ ONEX \_                 | I flag supplicant (eventualmente forniti nell'elemento EAPConfig) nel profilo OneX non sono validi.                                                                                 |
| VALORE DEL \_ TIMER NON VALIDO DEL PROFILO \_ \_ \_ ONEX                | Un timer specificato nel profilo OneX (possibilmente fornito dall'elemento heldPeriod, authPeriod o startPeriod) non è valido.                                                        |
| MODALITÀ \_ \_ \_ SUPPLICANT NON VALIDA DEL \_ PROFILO ONEX            | La modalità supplicant specificata nel profilo OneX (possibilmente fornita dall'elemento supplicantMode) non è valida.                                                                    |
| MODALITÀ DI AUTENTICAZIONE \_ \_ NON VALIDA DEL \_ PROFILO \_ ONEX                  | La modalità di autenticazione specificata nel profilo OneX (possibilmente fornita dall'elemento authMode) non è valida.                                                                      |
| PROPRIETÀ DI \_ CONNESSIONE \_ \_ EAP NON VALIDE DEL PROFILO \_ \_ ONEX | Le proprietà di connessione specificate nel profilo OneX (possibilmente fornite dall'elemento EAPConfig) non sono valide.                                                                  |



 

## <a name="remarks"></a>Commenti

Un set limitato di codici motivo è supportato in Windows XP con Service Pack 3 (SP3) e nell'API LAN wireless per Windows XP con Service Pack 2 (SP2). I codici di errore di convalida del profilo supportati in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2 sono i seguenti:

-   SCHEMA DEL PROFILO \_ NON VALIDO DEL CODICE \_ \_ \_ MOTIVO \_ WLAN
-   PROFILO DEL CODICE MOTIVO WLAN \_ \_ \_ \_ MANCANTE
-   SSID DEL \_ PROFILO DEL CODICE MOTIVO \_ \_ \_ WLAN NON \_ VALIDO

I codici di errore di sicurezza MSM supportati in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2 sono i seguenti:

-   INDICE DI \_ CHIAVE NON VALIDO DEL PROFILO \_ \_ MSMSEC \_ \_ \_ \_ DEL CODICE MOTIVO WLAN
-   LUNGHEZZA CHIAVE DEL \_ \_ PROFILO \_ MSMSEC \_ \_ \_ DEL CODICE MOTIVO WLAN
-   LUNGHEZZA PSK DEL PROFILO \_ \_ \_ MSMSEC \_ DEL \_ \_ CODICE MOTIVO WLAN
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ AUTH \_ CIPHER
-   CODICE MOTIVO WLAN \_ \_ PROFILO \_ MSMSEC \_ \_ ONEX \_ DISABILITATO
-   CODICE MOTIVO WLAN \_ \_ PROFILO \_ MSMSEC \_ \_ ONEX \_ ABILITATO
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NETWORK
-   SCHEDA DI INTERFACCIA DI RETE \_ \_ DELLA FUNZIONALITÀ MSMSEC DEL CODICE \_ MOTIVO WLAN \_ \_
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR
-   CODICE MOTIVO WLAN: TIPO DI CHIAVE ERRATO DEL PROFILO \_ \_ \_ MSMSEC \_ \_ \_

I codici di errore 802.1x supportati in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2 sono i seguenti:

-   LUNGHEZZA DEL PROFILO ONEX \_ \_ NON \_ VALIDA
-   TIPO \_ \_ EAP O FLAG ONEX PROFILE NON \_ \_ \_ \_ VALIDO
-   MODALITÀ DI AUTENTICAZIONE \_ \_ NON VALIDA DEL \_ PROFILO \_ ONEX
-   PROPRIETÀ DI \_ CONNESSIONE \_ \_ EAP NON VALIDE DEL PROFILO \_ \_ ONEX

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/>                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wlanapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
