---
description: Il corretto funzionamento dei componenti TAPI richiede la configurazione dell'ambiente di comunicazione in un computer.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: Inizializzazione TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f9062f8440cdec6597d21a2141a24b12f69bc9e940e189965d9e73880c54c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659901"
---
# <a name="tapi-initialization"></a>Inizializzazione TAPI

Il corretto funzionamento dei componenti TAPI richiede la configurazione dell'ambiente di comunicazione in un computer come indicato di seguito:

-   [L'installazione](installation.md) viene eseguita quando il software o l'hardware viene aggiunto per la prima volta al computer. Le procedure dettagliate dipendono dal sistema operativo e dal software stesso.
-   [L'inizializzazione](primary-initialization.md) primaria crea gli oggetti e i percorsi di comunicazione.
-   [La negoziazione](version-negotiation.md) della versione garantisce che i componenti TAPI siano in grado di scambiare dati.
-   [L'inventario](resource-inventory.md) delle risorse recupera le informazioni relative ai dispositivi disponibili per l'uso da parte di un'applicazione TAPI.
-   [La notifica degli](event-notification.md) eventi specifica il modo in cui TAPI e i provider di servizi passano all'applicazione i risultati dell'operazione asincrona e le informazioni sulla modifica dello stato.

## <a name="summary-of-related-reference-pages"></a>Riepilogo delle pagine di riferimento correlate



| Funzioni TAPI 2.x                                        | Descrizione                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Configura l'ambiente di telefonia, restituisce l'handle dell'applicazione e il numero di dispositivi.                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Ottiene le funzionalità del dispositivo, ad esempio la versione TAPI o i tipi di supporti supportati.                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Ottiene le funzionalità degli indirizzi, ad esempio se il parcheggio di chiamata è supportato.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Notifica a TAPI che l'applicazione usa la riga e in che modo.                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Restituisce il messaggio TAPI successivo accodato per il recapito a un'applicazione che usa il meccanismo di notifica dell'handle di evento |



 



| Interfacce o metodi TAPI 3.x                                                | Descrizione                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Configura l'ambiente di telefonia.                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Enumera gli indirizzi attualmente disponibili.                                                                                                  |
| [**INDIRIZZI ITTAPI::get \_**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Crea una raccolta di indirizzi attualmente disponibili. Fornito per le applicazioni client di Automazione, ad esempio quelle scritte in Visual Basic. |
| [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Determina la risposta a una notifica di evento asincrona. Implementato dall'applicazione, richiamato da TAPI.                                |
| [**ITTAPI::put \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Imposta la maschera filtro eventi, che notifica a TAPI gli eventi necessari per l'applicazione.                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Indica a TAPI di passare le sessioni in ingresso dell'applicazione per un indirizzo e un set di tipi di supporti specificati.                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Consente a un'applicazione di individuare le funzionalità di supporto multimediale per un indirizzo.                                                           |



 

 

 
