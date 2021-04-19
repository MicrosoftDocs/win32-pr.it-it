---
description: Questa sezione contiene un elenco dei messaggi nell'interfaccia TSPI (telefonia Service Provider Interface).
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: Messaggi TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5772a1ccb0c07f03b2a17348ecf5e4834bb97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317632"
---
# <a name="tspi-messages"></a>Messaggi TSPI

Questa sezione contiene un elenco dei messaggi nell'interfaccia TSPI (telefonia Service Provider Interface). Questi messaggi vengono utilizzati per notificare a TAPI l'occorrenza di eventi asincroni che si verificano spontaneamente all'interno del provider di servizi. Il provider di servizi passa questi eventi a TAPI chiamando una funzione di callback [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) o [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) , a seconda che il provider di servizi stia segnalando un evento su una riga, una chiamata o un dispositivo telefonico. La procedura **LineEvent** per la creazione di report sugli eventi che si verificano su una riga o una chiamata viene fornita al provider di servizi al momento dell'apertura della riga con la funzione [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) . La procedura **PHONEEVENT** per la creazione di report sugli eventi che si verificano in un telefono viene fornita con la funzione [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen) .

Questi eventi spontanei non vengono richiesti da TAPI nel senso che non sono una risposta diretta a qualsiasi richiesta. Questi eventi si differenziano con quelli che segnalano il completamento delle richieste effettuate da TAPI. Tali eventi di completamento vengono segnalati tramite la funzione di callback di [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) .

I profili di parametro per le procedure di evento spontaneo includono parametri che identificano l'oggetto pertinente per il quale viene segnalato l'evento (telefono, riga o chiamata). L'identificazione è sotto forma di handle opaco la cui interpretazione esatta non è pubblicata da TSPI. TAPI internamente determina la relazione tra questi handle opachi e tutte le strutture di dati usate per rappresentare i dispositivi.

Il profilo del parametro per le procedure di evento spontaneo include anche un parametro del messaggio che identifica il tipo del messaggio. Ogni tipo di messaggio ha una definizione corrispondente che determina gli handle inclusi, insieme ad altri parametri e ai relativi significati. Esiste una corrispondenza molto forte tra i messaggi visualizzati a livello di TSPI e quelli visualizzati a livello di TAPI. Queste sono le regole generali di corrispondenza:

-   Il set di messaggi è quasi identico. Quando i messaggi corrispondono, lo stesso nome e valore del messaggio viene usato a livello di TSPI.
-   Gli handle visualizzati a livello di TSPI sono i tipi opachi definiti dalla specifica TSPI. Questi tipi (e le relative interpretazioni) differiscono da quelli a livello di TAPI, sebbene facciano riferimento alla stessa classe di dispositivo. Se, ad esempio, un messaggio TAPI include un handle HLINE, il messaggio TSPI corrispondente include in genere un handle [**HTAPILINE**](htapiline.md) .
-   Nessun dato *dwCallbackInstance* passato al callback.
-   I parametri *dwParam1*, *dwParam2* e *dwParam3* sono in genere identici ai parametri corrispondenti per il messaggio TAPI.
-   I messaggi orientati alle righe e orientati alle chiamate vengono passati a una procedura di callback diversa rispetto ai messaggi orientati al telefono.

Per ogni messaggio, in questa sezione sono elencati gli elementi seguenti:

-   Scopo del messaggio
-   Procedura di callback a cui viene passato questo messaggio
-   Descrizione dei parametri del messaggio
-   Commenti facoltativi sull'utilizzo del messaggio
-   Riferimenti facoltativi ad altre funzioni, messaggi e strutture di dati
-   Commenti facoltativi che confrontano questo messaggio con l'interfaccia TAPI

Alcuni messaggi vengono utilizzati per notificare a TAPI informazioni su una modifica nello stato di un oggetto. Questi messaggi forniscono l'handle dell'oggetto opaco TAPI e un'indicazione dell'elemento di stato modificato. In seguito, TAPI può chiamare una funzione "Get status" appropriata dell'oggetto per ottenere lo stato completo dell'oggetto.

Quando si verifica un evento, un messaggio può essere inviato o meno a TAPI. Per alcuni tipi di evento, ad esempio le modifiche dello stato, TAPI specifica un set di modifiche dello stato a cui è interessato. Il provider di servizi è consigliato per limitare gli eventi del messaggio di modifica dello stato segnalati a quelli inclusi in questo set. Non è necessario che il provider di servizi rispetti questo limite. In altre parole, può segnalare un numero maggiore di modifiche rispetto a quelle strettamente necessarie. Tuttavia, deve tentare di osservare il limite per motivi di prestazioni.

Il \_ messaggio di risposta di riga non viene utilizzato a livello di TSPI. Il completamento di una richiesta asincrona viene segnalato utilizzando il callback di [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Il \_ messaggio di risposta telefonica non viene usato a livello di TSPI. Il completamento di una richiesta asincrona viene segnalato utilizzando il callback di [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Per altre informazioni, vedere gli argomenti seguenti:

-   [Messaggi di dispositivo linea TSPI](tspi-line-device-messages.md)
-   [Messaggi di TSPI Phone Device](tspi-phone-device-messages.md)

 

 
