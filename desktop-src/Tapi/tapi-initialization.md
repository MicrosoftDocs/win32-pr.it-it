---
description: Per il corretto funzionamento dei componenti TAPI è necessario configurare l'ambiente di comunicazione in un computer.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: Inizializzazione TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973d67931fb9f33751fedc638ab77021d3d3d34c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317034"
---
# <a name="tapi-initialization"></a>Inizializzazione TAPI

Per il corretto funzionamento dei componenti TAPI è necessario configurare l'ambiente di comunicazione in un computer, come indicato di seguito:

-   L' [installazione](installation.md) viene eseguita quando il software o l'hardware viene inizialmente aggiunto al computer. Le procedure dettagliate dipendono dal sistema operativo e dal software stesso.
-   L' [inizializzazione primaria](primary-initialization.md) crea gli oggetti e i percorsi di comunicazione.
-   La [negoziazione della versione](version-negotiation.md) garantisce che i componenti TAPI saranno in grado di scambiare dati.
-   [Inventario risorse](resource-inventory.md) recupera le informazioni relative ai dispositivi disponibili per l'uso da un'applicazione TAPI.
-   La [notifica degli eventi](event-notification.md) specifica il modo in cui TAPI e i provider di servizi passano i risultati dell'operazione asincrona e le informazioni di modifica dello stato all'applicazione.

## <a name="summary-of-related-reference-pages"></a>Riepilogo delle pagine di riferimento correlate



| Funzioni di TAPI 2. x                                        | Descrizione                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Configura l'ambiente di telefonia, restituisce l'handle dell'applicazione e il numero di dispositivi.                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Ottiene le funzionalità del dispositivo, ad esempio la versione TAPI o i tipi di supporto supportati.                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Ottiene le funzionalità di indirizzo, ad esempio se Call Park è supportato.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Notifica a TAPI che l'applicazione utilizzerà la riga e in che modo.                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Restituisce il successivo messaggio TAPI accodato per il recapito a un'applicazione che utilizza il meccanismo di notifica dell'handle di evento |



 



| Interfacce o metodi di TAPI 3. x                                                | Descrizione                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Imposta l'ambiente di telefonia.                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Enumera gli indirizzi attualmente disponibili.                                                                                                  |
| [**Indirizzi ITTAPI:: Get \_**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Crea una raccolta di indirizzi attualmente disponibili. Fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic. |
| [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Determina la risposta a una notifica di evento asincrono. Implementato dall'applicazione, richiamato da TAPI.                                |
| [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Imposta la maschera di filtro eventi, che notifica a TAPI gli eventi richiesti dall'applicazione.                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Indica a TAPI di passare le sessioni in ingresso dell'applicazione per un indirizzo e un set di tipi di supporto specificati.                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Consente a un'applicazione di individuare le funzionalità di supporto multimediale per un indirizzo.                                                           |



 

 

 
