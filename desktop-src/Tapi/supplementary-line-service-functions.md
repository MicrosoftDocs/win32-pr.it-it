---
description: Le funzioni di servizio linea supplementare sono elencate per categoria negli argomenti seguenti.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funzioni di servizio linea supplementare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311869"
---
# <a name="supplementary-line-service-functions"></a>Funzioni di servizio linea supplementare

Le funzioni di servizio linea supplementare sono elencate per categoria negli argomenti seguenti. Una funzione viene identificata come [*asincrona*](a-tapgloss.md) se indicherà il completamento di un messaggio di risposta all'applicazione. Se la funzione restituisce sempre il risultato all'applicazione immediatamente, la funzione viene considerata [*sincrona*](s-tapgloss.md).

Di seguito è riportato un raggruppamento funzionale delle funzioni di servizio di linea supplementare:

-   [Agenti](#agents)
-   [Priorità applicazione](#application-priority)
-   [Modalità di Bearer e frequenza](#bearer-mode-and-rate)
-   [Chiama Accept e reindirizza](#call-accept-and-redirect)
-   [Completamento chiamata](#call-completion)
-   [Conference Call](#call-conference)
-   [Invio di chiamate](#call-forwarding)
-   [Attesa chiamata](#call-hold)
-   [Call Park](#call-park)
-   [Pickup chiamata](#call-pickup)
-   [Rifiuto chiamata](#call-reject)
-   [Trasferimento chiamate](#call-transfer)
-   [Monitoraggio e raccolta dei numeri](#digit-monitoring-and-gathering)
-   [Generazione di cifre e toni inband](#generating-inband-digits-and-tones)
-   [Esecuzione di chiamate](basic-telephony-services-reference.md)
-   [Controllo multimediale](#media-control)
-   [Monitoraggio dei supporti](#media-monitoring)
-   [Proxy](#proxies)
-   [QoS (Quality of Service)](#quality-of-service)
-   [Invio di informazioni a un'entità remota](#sending-information-to-remote-party)
-   [Gestione provider di servizi](#service-provider-management)
-   [Impostazione di un terminale per le conversazioni telefoniche](#setting-a-terminal-for-phone-conversations)
-   [Monitoraggio del tono](#tone-monitoring)

Sono disponibili anche [varie](#miscellaneous) funzioni di servizio di linea supplementari.

## <a name="bearer-mode-and-rate"></a>Modalità di Bearer e frequenza



| Funzione                                       | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Richiede una modifica nei parametri di chiamata di una chiamata esistente. Synchronous. |



 

## <a name="media-monitoring"></a>Monitoraggio dei supporti



| Funzione                                     | Descrizione                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Abilita o Disabilita la notifica in modalità supporto per una chiamata specificata. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Monitoraggio e raccolta dei numeri



| Funzione                                       | Descrizione                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Abilita o Disabilita la notifica di rilevamento digit per una chiamata specificata. Synchronous. |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Esegue la raccolta memorizzata nel buffer di cifre in una chiamata. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Monitoraggio del tono



| Funzione                                     | Descrizione                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Specifica i toni da rilevare in una chiamata specificata. Synchronous. |



 

## <a name="media-control"></a>Controllo multimediale



| Funzione                                           | Descrizione                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Imposta un flusso multimediale della chiamata per il controllo multimediale. Synchronous.                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Imposta la modalità multimediale della chiamata specificata nella relativa struttura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) . Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Generazione di cifre e toni inband



| Funzione                                         | Descrizione                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Genera cifre inband in una chiamata. Synchronous.               |
| [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Genera un set di toni specificato in una chiamata. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Chiama Accept e reindirizza



| Funzione                             | Descrizione                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Accetta una chiamata offerta e avvia avvisi sia del chiamante (richiamabile) che del chiamante (anello). Asincrona. |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Reindirizza una chiamata di offerta a un altro indirizzo. Asincrona.                                              |



 

## <a name="call-reject"></a>Rifiuto chiamata



| Funzione                     | Descrizione                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Disconnette una chiamata o abbandona un tentativo di chiamata in corso. Asincrona. |



 

## <a name="call-hold"></a>Attesa chiamata



| Funzione                         | Descrizione                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Inserisce la chiamata specificata sul disco rigido. Asincrona. |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Recupera una chiamata mantenuta. Asincrona.                  |



 

## <a name="securing-calls"></a>Protezione delle chiamate



| Funzione                                 | Descrizione                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Protegge una chiamata esistente da interferenze da altri eventi, ad esempio segnali acustici in attesa di chiamate sulle connessioni dati. Asincrona. |



 

## <a name="call-transfer"></a>Trasferimento chiamate



| Funzione                                             | Descrizione                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Prepara una chiamata specificata per il trasferimento a un altro indirizzo. Asincrona.                                       |
| [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Trasferisce una chiamata impostata per il trasferimento a un'altra chiamata o entra in una conferenza a tre vie. Asincrona. |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Trasferisce una chiamata a un'altra entità. Asincrona.                                                               |
| [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Scambia la chiamata attiva con la chiamata attualmente in attesa di consultazione. Asincrona.                              |



 

## <a name="call-conference"></a>Conference Call



| Funzione                                                         | Descrizione                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Prepara una determinata chiamata per l'aggiunta di un'altra parte. Asincrona.                                                                                                                               |
| [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Prepara l'aggiunta di un'entità a una chiamata di conferenza esistente posizionando la chiamata di conferenza in uno stato di attesa e creando una chiamata di consultazione che può essere aggiunta successivamente alla chiamata di conferenza. Asincrona. |
| [**lineAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Aggiunge una chiamata di consultazione a una chiamata di conferenza esistente. Asincrona.                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Rimuove un'entità da una chiamata di conferenza. Asincrona.                                                                                                                                                |



 

## <a name="call-park"></a>Call Park



| Funzione                         | Descrizione                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | Parcheggia una determinata chiamata a un altro indirizzo. Asincrona. |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Recupera una chiamata parcheggiata. Asincrona.               |



 

## <a name="call-forwarding"></a>Invio di chiamate



| Funzione                           | Descrizione                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Imposta o Annulla le richieste di invio della chiamata. Asincrona. |



 

## <a name="call-pickup"></a>Pickup chiamata



| Funzione                         | Descrizione                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Preleva un avviso di chiamata a un indirizzo di destinazione specificato e restituisce un handle di chiamata per la chiamata selezionata ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usato anche per la chiamata in attesa). Asincrona. |



 

## <a name="sending-information-to-remote-party"></a>Invio di informazioni a un'entità remota



| Funzione                                                   | Descrizione                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Rilascia informazioni utente utente, consentendo al sistema di sovrascrivere questa risorsa di archiviazione con nuove informazioni. Asincrona. |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Invia le informazioni utente utente alla parte remota sulla chiamata specificata. Asincrona.                                |



 

## <a name="call-completion"></a>Completamento chiamata



| Funzione                                         | Descrizione                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Inserisce una richiesta di completamento della chiamata. Asincrona.  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Annulla una richiesta di completamento della chiamata. Asincrona. |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Impostazione di un terminale per le conversazioni telefoniche



| Funzione                                   | Descrizione                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Specifica il dispositivo terminal a cui vengono indirizzati gli eventi di riga, di indirizzo o di chiamata del flusso multimediale specificati. Asincrona. |



 

## <a name="application-priority"></a>Priorità applicazione



| Funzione                                         | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Recupera le informazioni sulla priorità di telefonia uniforme e/o assistita per un'applicazione. Synchronous. |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Imposta la priorità di consegna e/o di telefonia assistita per un'applicazione. Synchronous.              |



 

## <a name="service-provider-management"></a>Gestione provider di servizi



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
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Ottiene le funzionalità correlate all'agente supportate nel dispositivo a linee specificato. Asincrona.                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Ottiene l'elenco dei gruppi di agenti in cui un agente può accedere al server di distribuzione chiamate automatico. Asincrona.                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Ottiene lo stato relativo all'agente nell'indirizzo specificato. Asincrona.                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Imposta il codice dell'attività dell'agente associato a un indirizzo specifico. Asincrona.                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Imposta i gruppi di agenti a cui l'agente è connesso in un determinato indirizzo. Asincrona.                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Imposta lo stato dell'agente associato a un determinato indirizzo. Asincrona.                                                                |



 

## <a name="proxies"></a>Proxy



| Funzione                                       | Descrizione                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Utilizzato da un gestore di richieste proxy registrato per generare messaggi TAPI. Synchronous.  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Indica il completamento di una richiesta proxy da un gestore proxy registrato. Synchronous. |



 

## <a name="quality-of-service"></a>QoS (Quality of Service)



| Funzione                                                           | Descrizione                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Richiede una modifica dei parametri di qualità del servizio per una chiamata esistente. Asincrona. |



 

## <a name="miscellaneous"></a>Varie



| Funzione                                             | Descrizione                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Imposta il membro **CallData** della struttura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) . Asincrona. |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Imposta i suoni che l'utente avverte quando una chiamata non risponde o è in attesa. Asincrona.               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Imposta lo stato del dispositivo di linea. Asincrona.                                                            |



 

 

 



