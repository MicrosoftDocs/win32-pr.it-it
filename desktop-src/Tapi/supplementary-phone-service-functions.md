---
description: Le funzioni del servizio telefonico supplementare sono elencate per categoria negli argomenti seguenti.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funzioni del servizio telefonico supplementare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311868"
---
# <a name="supplementary-phone-service-functions"></a>Funzioni del servizio telefonico supplementare

Le funzioni del servizio telefonico supplementare sono elencate per categoria negli argomenti seguenti. Una funzione viene identificata come [*asincrona*](a-tapgloss.md) se indicherà il completamento di un messaggio di risposta all'applicazione. Se la funzione restituisce sempre il risultato all'applicazione immediatamente, la funzione viene considerata [*sincrona*](s-tapgloss.md).

Di seguito è riportato un raggruppamento funzionale delle funzioni del servizio telefonico supplementare:

-   [Pulsanti](#buttons)
-   [Aree dati](#data-areas)
-   [Schermo](#display)
-   [Dispositivi hookswitch](#hookswitch-devices)
-   [Lampade](#lamps)
-   [Apertura e chiusura di dispositivi telefonici](#opening-and-closing-phone-devices)
-   [Inizializzazione e arresto del telefono](#phone-initialization-and-shutdown)
-   [Funzionalità e stato del telefono](#phone-status-and-capabilities)
-   [Negoziazione della versione del telefono](#phone-version-negotiation)
-   [Anello](#ring)
-   [Status](#status)

## <a name="phone-initialization-and-shutdown"></a>Inizializzazione e arresto del telefono



| Funzione                                       | Descrizione                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Inizializza l'astrazione del telefono TAPI per l'uso da parte dell'applicazione chiamante. Synchronous. |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Arresta l'uso dell'astrazione telefonica di TAPI da un'applicazione. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Negoziazione della versione del telefono



| Funzione                                                     | Descrizione                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Consente a un'applicazione di negoziare una versione TAPI da usare. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Apertura e chiusura di dispositivi telefonici



| Funzione                         | Descrizione                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Apre il dispositivo telefonico specificato, assegnando all'applicazione i privilegi di proprietario o di monitoraggio. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Chiude un dispositivo telefonico aperto specificato. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Funzionalità e stato del telefono



| Funzione                                       | Descrizione                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Restituisce le funzionalità di un determinato dispositivo telefonico. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Restituisce un ID dispositivo per la classe di dispositivo specificata associata al dispositivo telefonico specificato. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Consente a un'applicazione di recuperare un'icona da visualizzare all'utente. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Fa in modo che il provider del dispositivo telefonico specificato visualizzi una finestra di dialogo che consenta all'utente di configurare i parametri relativi al dispositivo telefonico. Synchronous. |



 

## <a name="hookswitch-devices"></a>Dispositivi hookswitch



| Funzione                                         | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Imposta lo stato di hook dei dispositivi hookswitch del telefono aperto su una modalità specificata. Asincrona.      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Esegue una query sulla modalità hookswitch di un dispositivo hookswitch di un dispositivo telefonico aperto. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Imposta il volume dell'altoparlante di un dispositivo hookswitch di un dispositivo telefonico aperto. Asincrona.           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Restituisce l'impostazione del volume dell'altoparlante di un dispositivo hookswitch di un dispositivo telefonico aperto. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Imposta il guadagno del MIC di un dispositivo hookswitch di un dispositivo telefonico aperto. Asincrona.                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Restituisce l'impostazione di guadagno del MIC di un dispositivo hookswitch di un telefono aperto. Synchronous.              |



 

## <a name="display"></a>Visualizza



| Funzione                                   | Descrizione                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Scrive le informazioni nella visualizzazione di un dispositivo telefonico aperto. Asincrona. |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Restituisce il contenuto corrente della visualizzazione di un telefono. Synchronous.          |



 

## <a name="ring"></a>Anello



| Funzione                             | Descrizione                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Squilla un dispositivo telefonico aperto in base a una modalità anello specificata. Asincrona. |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Restituisce la modalità corrente della suoneria di un dispositivo telefonico aperto. Synchronous.    |



 

## <a name="buttons"></a>Pulsanti



| Funzione                                         | Descrizione                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Imposta le informazioni associate a un pulsante in un dispositivo telefonico. Asincrona. |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Restituisce le informazioni associate a un pulsante in un dispositivo telefonico. Synchronous.   |



 

## <a name="lamps"></a>Lampade



| Funzione                             | Descrizione                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Illumina una lampada su un dispositivo telefonico aperto specificato in una determinata modalità di illuminazione lamp. Asincrona. |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Restituisce la modalità lampada corrente della lampada specificata. Synchronous.                           |



 

## <a name="data-areas"></a>Aree dati



| Funzione                             | Descrizione                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Scarica un buffer di dati in un'area dati specificata nel dispositivo telefonico. Asincrona.      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Carica il contenuto di una determinata area dati del dispositivo telefonico in un buffer. Synchronous. |



 

## <a name="status"></a>Stato



| Funzione                                                 | Descrizione                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Specifica le modifiche dello stato per cui l'applicazione vuole ricevere una notifica. Synchronous. |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Restituisce le modifiche dello stato per le quali l'applicazione desidera ricevere una notifica. Synchronous.   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Restituisce lo stato completo di un dispositivo telefonico aperto. Synchronous.                         |



 

 

 



