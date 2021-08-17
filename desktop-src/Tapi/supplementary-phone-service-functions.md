---
description: Le funzioni supplementari del servizio telefonico sono elencate per categoria negli argomenti seguenti.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funzioni supplementari Telefono service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ee0e32260ac3821fd06e7e8962ab2a6186fb42f1140eb6cd8f705709f2dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861419"
---
# <a name="supplementary-phone-service-functions"></a>Funzioni supplementari Telefono service

Le funzioni supplementari del servizio telefonico sono elencate per categoria negli argomenti seguenti. Una funzione viene identificata [*come asincrona*](a-tapgloss.md) se indicherà il completamento in un messaggio REPLY all'applicazione. Se la funzione restituisce sempre immediatamente il risultato all'applicazione, la funzione viene considerata [*sincrona.*](s-tapgloss.md)

Di seguito è riportato un raggruppamento funzionale delle funzioni supplementari del servizio telefonico:

-   [Pulsanti](#buttons)
-   [Aree dati](#data-areas)
-   [Schermo](#display)
-   [Dispositivi hookswitch](#hookswitch-devices)
-   [Lampade](#lamps)
-   [Apertura e chiusura di dispositivi telefonici](#opening-and-closing-phone-devices)
-   [Telefono inizializzazione e arresto](#phone-initialization-and-shutdown)
-   [Telefono stato e funzionalità](#phone-status-and-capabilities)
-   [Telefono della versione](#phone-version-negotiation)
-   [Anello](#ring)
-   [Status](#status)

## <a name="phone-initialization-and-shutdown"></a>Telefono Inizializzazione e arresto



| Funzione                                       | Descrizione                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Inizializza l'astrazione del telefono TAPI per l'uso da parte dell'applicazione che richiama. Synchronous. |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Arresta l'uso dell'astrazione del telefono di TAPI da parte di un'applicazione. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Telefono Negoziazione della versione



| Funzione                                                     | Descrizione                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Consente a un'applicazione di negoziare una versione TAPI da usare. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Apertura e chiusura di Telefono dispositivi



| Funzione                         | Descrizione                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Apre il dispositivo telefonico specificato, con privilegi di proprietario o di monitoraggio per l'applicazione. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Chiude un dispositivo telefono aperto specificato. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Telefono Stato e funzionalità



| Funzione                                       | Descrizione                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Restituisce le funzionalità di un dispositivo telefonico specificato. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Restituisce un ID dispositivo per la classe di dispositivi specificata associata al dispositivo telefonico specificato. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Consente a un'applicazione di recuperare un'icona da visualizzare all'utente. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Fa in modo che il provider del dispositivo telefonico specificato visualizza una finestra di dialogo che consente all'utente di configurare i parametri correlati al dispositivo telefonico. Synchronous. |



 

## <a name="hookswitch-devices"></a>Dispositivi hookswitch



| Funzione                                         | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Imposta lo stato hook dei dispositivi hookswitch di un telefono aperto su una modalità specificata. Asincrona.      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Esegue una query sulla modalità hookswitch di un dispositivo hookswitch di un dispositivo telefonico aperto. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Imposta il volume dell'altoparlante di un dispositivo hookswitch di un dispositivo telefono aperto. Asincrona.           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Restituisce l'impostazione del volume dell'altoparlante di un dispositivo hookswitch di un dispositivo telefonico aperto. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Imposta il guadagno del microfono di un dispositivo hookswitch di un dispositivo telefono aperto. Asincrona.                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Restituisce l'impostazione del guadagno del microfono di un dispositivo hookswitch di un telefono aperto. Synchronous.              |



 

## <a name="display"></a>Visualizza



| Funzione                                   | Descrizione                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Scrive informazioni sulla visualizzazione di un dispositivo telefonico aperto. Asincrona. |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Restituisce il contenuto corrente dello schermo di un telefono. Synchronous.          |



 

## <a name="ring"></a>Anello



| Funzione                             | Descrizione                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Chiama un dispositivo telefonico aperto in base a una modalità anello specificata. Asincrona. |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Restituisce la modalità anello corrente di un dispositivo telefonico aperto. Synchronous.    |



 

## <a name="buttons"></a>Pulsanti



| Funzione                                         | Descrizione                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Imposta le informazioni associate a un pulsante in un dispositivo telefono. Asincrona. |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Restituisce informazioni associate a un pulsante in un dispositivo telefono. Synchronous.   |



 

## <a name="lamps"></a>Lampade



| Funzione                             | Descrizione                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Accende una lampadina su un dispositivo telefonico aperto specificato in una determinata modalità di illuminazione della lampadina. Asincrona. |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Restituisce la modalità della lampadina corrente della lampadina specificata. Synchronous.                           |



 

## <a name="data-areas"></a>Aree dati



| Funzione                             | Descrizione                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Scarica un buffer di dati in una determinata area dati nel dispositivo telefonico. Asincrona.      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Carica il contenuto di una determinata area dati nel dispositivo telefonico in un buffer. Synchronous. |



 

## <a name="status"></a>Stato



| Funzione                                                 | Descrizione                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Specifica le modifiche di stato per cui l'applicazione vuole ricevere una notifica. Synchronous. |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Restituisce le modifiche di stato per cui l'applicazione vuole ricevere una notifica. Synchronous.   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Restituisce lo stato completo di un dispositivo telefono aperto. Synchronous.                         |



 

 

 



