---
description: Le funzioni supplementari del servizio di riga sono elencate per categoria negli argomenti seguenti.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funzioni supplementari del servizio di riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f2bdd609f092adebd5270a4cc8a3fe35bedce17ad57d8e4e85b5875001255f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476344"
---
# <a name="supplementary-line-service-functions"></a>Funzioni supplementari del servizio di riga

Le funzioni supplementari del servizio di riga sono elencate per categoria negli argomenti seguenti. Una funzione viene identificata [*come asincrona*](a-tapgloss.md) se indicherà il completamento in un messaggio REPLY all'applicazione. Se la funzione restituisce sempre immediatamente il risultato all'applicazione, la funzione viene considerata [*sincrona.*](s-tapgloss.md)

Di seguito è riportato un raggruppamento funzionale delle funzioni di line service supplementari:

-   [Agenti](#agents)
-   [Priorità dell'applicazione](#application-priority)
-   [Modalità di bearer e velocità](#bearer-mode-and-rate)
-   [Accettare e reindirizzare le chiamate](#call-accept-and-redirect)
-   [Completamento della chiamata](#call-completion)
-   [Conferenza telefonica](#call-conference)
-   [Inoltro delle chiamate](#call-forwarding)
-   [Blocco chiamate](#call-hold)
-   [Call park](#call-park)
-   [Chiamare il ritiro](#call-pickup)
-   [Rifiutare la chiamata](#call-reject)
-   [Trasferimento di chiamate](#call-transfer)
-   [Monitoraggio e raccolta di cifre](#digit-monitoring-and-gathering)
-   [Generazione di cifre e toni inband](#generating-inband-digits-and-tones)
-   [Effettuare chiamate](basic-telephony-services-reference.md)
-   [Controllo elementi multimediali](#media-control)
-   [Monitoraggio dei supporti](#media-monitoring)
-   [Proxy](#proxies)
-   [QoS (Quality of Service)](#quality-of-service)
-   [Invio di informazioni a un'entità remota](#sending-information-to-remote-party)
-   [Gestione dei provider di servizi](#service-provider-management)
-   [Impostazione di un terminale per le conversazioni telefoniche](#setting-a-terminal-for-phone-conversations)
-   [Monitoraggio del tono](#tone-monitoring)

Sono inoltre [disponibili varie funzioni di](#miscellaneous) line service supplementari.

## <a name="bearer-mode-and-rate"></a>Modalità di bearer e velocità



| Funzione                                       | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Richiede una modifica nei parametri di chiamata di una chiamata esistente. Synchronous. |



 

## <a name="media-monitoring"></a>Monitoraggio dei supporti



| Funzione                                     | Descrizione                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Abilita o disabilita la notifica in modalità multimediale in una chiamata specificata. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Monitoraggio e raccolta delle cifre



| Funzione                                       | Descrizione                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Abilita o disabilita la notifica di rilevamento delle cifre in una chiamata specificata. Synchronous. |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Esegue la raccolta di cifre memorizzate nel buffer in una chiamata. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Monitoraggio del tono



| Funzione                                     | Descrizione                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Specifica i toni da rilevare in una chiamata specificata. Synchronous. |



 

## <a name="media-control"></a>Controllo supporti



| Funzione                                           | Descrizione                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Configura il flusso multimediale di una chiamata per il controllo multimediale. Synchronous.                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Imposta le modalità multimediali della chiamata specificata nella relativa [**struttura LINECALLINFO.**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Generazione di cifre e toni inband



| Funzione                                         | Descrizione                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Genera cifre inband su una chiamata. Synchronous.               |
| [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Genera un set specificato di toni inband in una chiamata. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Accettare e reindirizzare le chiamate



| Funzione                             | Descrizione                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Accetta una chiamata offerta e avvia l'avviso sia del chiamante (ringback) che della parte chiamata (anello). Asincrona. |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Reindirizza una chiamata di offerta a un altro indirizzo. Asincrona.                                              |



 

## <a name="call-reject"></a>Call Reject



| Funzione                     | Descrizione                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Disconnette una chiamata o abbandona un tentativo di chiamata in corso. Asincrona. |



 

## <a name="call-hold"></a>Chiamata in attesa



| Funzione                         | Descrizione                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Posiziona la chiamata specificata su un blocco rigido. Asincrona. |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Recupera una chiamata mantenuta. Asincrona.                  |



 

## <a name="securing-calls"></a>Protezione delle chiamate



| Funzione                                 | Descrizione                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Protegge una chiamata esistente dall'interferenza da parte di altri eventi, ad esempio i besp di attesa delle chiamate nelle connessioni dati. Asincrona. |



 

## <a name="call-transfer"></a>Trasferimento di chiamate



| Funzione                                             | Descrizione                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Prepara una chiamata specificata per il trasferimento a un altro indirizzo. Asincrona.                                       |
| [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Trasferisce una chiamata impostata per il trasferimento a un'altra chiamata o entra in una conferenza a tre modi. Asincrona. |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Trasferisce una chiamata a un'altra parte. Asincrona.                                                               |
| [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Scambia la chiamata attiva con la chiamata attualmente in attesa di consulenza. Asincrona.                              |



 

## <a name="call-conference"></a>Call Conference



| Funzione                                                         | Descrizione                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Prepara una chiamata specificata per l'aggiunta di un'altra parte. Asincrona.                                                                                                                               |
| [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Prepara l'aggiunta di un'entità a una conferenza telefonica esistente inserendo la conferenza in uno stato di attesa e creando una chiamata di consulenza che può essere aggiunta in un secondo momento alla conferenza telefonica. Asincrona. |
| [**lineAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Aggiunge una chiamata di consulenza a una conferenza telefonica esistente. Asincrona.                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Rimuove un'entità da una conferenza telefonica. Asincrona.                                                                                                                                                |



 

## <a name="call-park"></a>Call Park



| Funzione                         | Descrizione                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | Chiamare una determinata chiamata a un altro indirizzo. Asincrona. |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Recupera una chiamata di tipo "parked". Asincrona.               |



 

## <a name="call-forwarding"></a>Inoltro delle chiamate



| Funzione                           | Descrizione                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Imposta o annulla le richieste di inoltro delle chiamate. Asincrona. |



 

## <a name="call-pickup"></a>Call Pickup



| Funzione                         | Descrizione                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Preleva un avviso di chiamata a un indirizzo di destinazione specificato e restituisce un handle di chiamata per la chiamata prelevata ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usato anche per l'attesa di chiamata). Asincrona. |



 

## <a name="sending-information-to-remote-party"></a>Invio di informazioni a un'entità remota



| Funzione                                                   | Descrizione                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Rilascia le informazioni utente, permettendo al sistema di sovrascrivere questa archiviazione con nuove informazioni. Asincrona. |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Invia le informazioni utente-utente all'entità remota nella chiamata specificata. Asincrona.                                |



 

## <a name="call-completion"></a>Completamento chiamata



| Funzione                                         | Descrizione                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Inserisce una richiesta di completamento della chiamata. Asincrona.  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Annulla una richiesta di completamento della chiamata. Asincrona. |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Impostazione di un terminale per Telefono conversazioni



| Funzione                                   | Descrizione                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Specifica il dispositivo terminale a cui vengono indirizzati gli eventi di riga, di indirizzo o di chiamata del flusso multimediale specificati. Asincrona. |



 

## <a name="application-priority"></a>Priorità dell'applicazione



| Funzione                                         | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Recupera le informazioni sulla priorità di consegna e/o di telefonia assistita per un'applicazione. Synchronous. |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Imposta la priorità di consegna e/o di telefonia assistita per un'applicazione. Synchronous.              |



 

## <a name="service-provider-management"></a>Gestione dei provider di servizi



| Funzione                                           | Descrizione                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineAddProvider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | Installa un provider di servizi di telefonia. Synchronous.                   |
| [**lineConfigProvider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | Visualizza la finestra di dialogo di configurazione di un provider di servizi. Synchronous. |
| [**lineRemoveProvider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | Rimuove un provider di servizi di telefonia esistente. Synchronous.          |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | Recupera un elenco di provider di servizi installati. Synchronous.         |



 

## <a name="agents"></a>Agenti



| Funzione                                                     | Descrizione                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | Consente all'applicazione di accedere alle funzioni proprietarie specifiche del gestore dell'agente associato all'indirizzo. Asincrona. |
| [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | Ottiene l'elenco delle attività da cui un'applicazione seleziona le funzioni eseguite da un agente. Asincrona.                    |
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Ottiene le funzionalità correlate all'agente supportate nel dispositivo line specificato. Asincrona.                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Ottiene l'elenco dei gruppi di agenti a cui un agente può accedere nel server di distribuzione delle chiamate automatiche. Asincrona.                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Ottiene lo stato correlato all'agente nell'indirizzo specificato. Asincrona.                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Imposta il codice dell'attività dell'agente associato a un indirizzo specifico. Asincrona.                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Imposta i gruppi di agenti a cui l'agente è connesso in un indirizzo specifico. Asincrona.                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Imposta lo stato dell'agente associato a un indirizzo specifico. Asincrona.                                                                |



 

## <a name="proxies"></a>Proxy



| Funzione                                       | Descrizione                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Usato da un gestore di richieste proxy registrato per generare messaggi TAPI. Synchronous.  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Indica il completamento di una richiesta proxy da parte di un gestore proxy registrato. Synchronous. |



 

## <a name="quality-of-service"></a>QoS (Quality of Service)



| Funzione                                                           | Descrizione                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Richiede una modifica dei parametri di qualità del servizio per una chiamata esistente. Asincrona. |



 

## <a name="miscellaneous"></a>Varie



| Funzione                                             | Descrizione                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Imposta il **membro CallData** della [**struttura LINECALLINFO.**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) Asincrona. |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Imposta i suoni che l'utente ascolta quando una chiamata non ha risposta o è in attesa. Asincrona.               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Imposta lo stato del dispositivo linea. Asincrona.                                                            |



 

 

 



