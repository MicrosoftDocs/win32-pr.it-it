---
description: Le funzioni di telefonia di base sono elencate per categoria nelle tabelle seguenti.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Guida di riferimento ai servizi di telefonia Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309977"
---
# <a name="basic-telephony-services-reference"></a>Guida di riferimento ai servizi di telefonia Basic

Le funzioni di telefonia di base sono elencate per categoria nelle tabelle seguenti. Una funzione viene identificata come [*asincrona*](a-tapgloss.md) se indica il completamento in un messaggio di risposta all'applicazione. Se la funzione restituisce sempre il risultato all'applicazione immediatamente, la funzione viene considerata [*sincrona*](s-tapgloss.md).

Di seguito è riportato un raggruppamento funzionale delle funzioni di base del servizio di telefonia:

-   [Formati di indirizzi](#address-formats)
-   [Indirizzi](#addresses)
-   [Risposta alle chiamate in ingresso](#answering-incoming-calls)
-   [Funzioni drop di chiamata](#call-drop-functions)
-   [Manipolazione dell'handle di chiamata](#call-handle-manipulation)
-   [Controllo dei privilegi di chiamata](#call-privilege-control)
-   [Stati e eventi di chiamata](#call-states-and-events)
-   [Stato e funzionalità della linea](#line-status-and-capabilities)
-   [Negoziazione della versione della linea](#line-version-negotiation)
-   [Informazioni località e paese/area geografica](#location-and-countryregion-information)
-   [Esecuzione di chiamate](#making-calls)
-   [Apertura e chiusura di dispositivi linea](#opening-and-closing-line-devices)
-   [Richiedi servizi destinatari](#request-recipient-services)
-   [Inizializzazione e arresto di TAPI](#tapi-initialization-and-shutdown)
-   [Supporto per Toll saver](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a>Inizializzazione e arresto di TAPI



| Funzione                                     | Descrizione                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | Inizializza l'astrazione della linea TAPI per l'uso da parte dell'applicazione chiamante. Synchronous. |
| [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | Arresta l'uso dell'astrazione di linea di TAPI nell'applicazione. Synchronous.               |



 

## <a name="line-version-negotiation"></a>Negoziazione della versione della linea



| Funzione                                                   | Descrizione                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | Consente a un'applicazione di negoziare una versione TAPI da usare. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Stato e funzionalità della linea



| Funzione                                               | Descrizione                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | Restituisce le funzionalità di una determinata periferica di linea. Synchronous.                                                                                                  |
| [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | Restituisce la configurazione di un dispositivo del flusso multimediale. Synchronous.                                                                                                   |
| [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | Restituisce lo stato corrente del dispositivo a linee aperte specificato. Synchronous.                                                                                         |
| [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | Imposta la configurazione del dispositivo del flusso multimediale specificato. Synchronous.                                                                                      |
| [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | Specifica le modifiche dello stato per le quali l'applicazione deve ricevere una notifica. Synchronous.                                                                      |
| [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | Restituisce le impostazioni correnti dei messaggi di stato della riga e dell'indirizzo dell'applicazione. Synchronous.                                                                       |
| [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | Recupera un ID dispositivo associato alla riga aperta, all'indirizzo o alla chiamata specificata. Synchronous.                                                                  |
| [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | Consente a un'applicazione di recuperare un'icona da visualizzare all'utente. Synchronous.                                                                                |
| [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | Fa in modo che il provider del dispositivo a linee specificato visualizzi una finestra di dialogo che consenta all'utente di configurare i parametri correlati al dispositivo della linea. Synchronous. |
| [**lineConfigDialogEdit**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | Visualizza una finestra di dialogo che consente all'utente di modificare le informazioni di configurazione per un dispositivo a linee. Synchronous.                                                    |



 

## <a name="addresses"></a>Indirizzi



| Funzione                                             | Descrizione                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | Restituisce le funzionalità di telefonia di un indirizzo. Synchronous.                           |
| [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | Restituisce lo stato corrente di un indirizzo specificato. Synchronous.                              |
| [**lineGetAddressID**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | Recupera l'ID di un indirizzo specificato utilizzando un formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Apertura e chiusura di dispositivi linea



| Funzione                       | Descrizione                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | Apre un dispositivo a linee specificato per fornire il monitoraggio e/o il controllo successivo della riga. Synchronous. |
| [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) | Chiude un dispositivo a linee aperte specificato. Synchronous.                                                        |



 

## <a name="address-formats"></a>Formati di indirizzi



| Funzione                                                 | Descrizione                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | Trasla tra un indirizzo in formato canonico e un indirizzo in formato di composizione. Synchronous. |
| [**lineSetCurrentLocation**](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | Imposta il percorso utilizzato come contesto per la conversione degli indirizzi. Synchronous.                       |
| [**lineSetTollList**](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | Modifica la lista dei caselli. Synchronous.                                                           |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | Restituisce le funzionalità di traduzione degli indirizzi. Synchronous.                                            |



 

## <a name="call-states-and-events"></a>Stati e eventi di chiamata



| Funzione                                         | Descrizione                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | Restituisce informazioni fisse su una chiamata. Synchronous.                                |
| [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | Restituisce informazioni complete sullo stato della chiamata per la chiamata specificata. Synchronous.       |
| [**lineSetAppSpecific**](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | Imposta il campo specifico dell'applicazione della struttura di informazioni di una chiamata. Synchronous. |



 

## <a name="making-calls"></a>Esecuzione di chiamate



| Funzione                             | Descrizione                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | Esegue una chiamata in uscita e restituisce un handle di chiamata per l'oggetto. Asincrona. |
| [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)         | Dials (parti di uno o più) indirizzi di connessione. Asincrona.         |



 

## <a name="answering-incoming-calls"></a>Risposta alle chiamate in ingresso



| Funzione                         | Descrizione                             |
|----------------------------------|-----------------------------------------|
| [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | Risponde a una chiamata in ingresso. Asincrona. |



 

## <a name="toll-saver-support"></a>Supporto per Toll saver



| Funzione                                   | Descrizione                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | Indica il numero di anelli dopo i quali le chiamate in ingresso devono essere soddisfatte. Synchronous.                   |
| [**lineGetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | Restituisce il numero minimo di anelli richiesti con [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings). Synchronous. |



 

## <a name="call-privilege-control"></a>Controllo dei privilegi di chiamata



| Funzione                                             | Descrizione                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | Imposta il privilegio dell'applicazione sul privilegio specificato. Synchronous. |



 

## <a name="call-drop-functions"></a>Funzioni drop di chiamata



| Funzione                                         | Descrizione                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | Disconnette una chiamata o abbandona un tentativo di chiamata in corso. Asincrona. |
| [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | Dealloca l'handle di chiamata specificato. Synchronous.                       |



 

## <a name="call-handle-manipulation"></a>Manipolazione dell'handle di chiamata



| Funzione                                                   | Descrizione                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | Passa la proprietà della chiamata e/o modifica i privilegi di un'applicazione a una chiamata. Synchronous.                                    |
| [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | Restituisce gli handle di chiamata per le chiamate su una riga o un indirizzo specificato per cui l'applicazione non dispone ancora di handle. Synchronous. |
| [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | Restituisce un elenco di handle di chiamata che fanno parte della stessa chiamata di conferenza della chiamata specificata come parametro. Synchronous.    |



 

## <a name="location-and-countryregion-information"></a>Informazioni località e paese/area geografica



| Funzione                                           | Descrizione                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | Visualizza una finestra di dialogo che consente all'utente di modificare la posizione e le informazioni sulla scheda chiamante. Synchronous. |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | Recupera le regole di composizione e altre informazioni su un determinato paese/area geografica. Synchronous.              |



 

## <a name="request-recipient-services"></a>Richiedi servizi destinatari

Le due funzioni seguenti vengono utilizzate solo per supportare la telefonia assistita.



| Funzione                                                             | Descrizione                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | Registra o Annulla la registrazione dell'applicazione come destinatario della richiesta per la modalità di richiesta specificata. Synchronous. |
| [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | Ottiene la richiesta successiva dalla libreria a collegamento dinamico di telefonia. Synchronous.                                  |



 

 

 



