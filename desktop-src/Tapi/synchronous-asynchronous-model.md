---
description: La natura interattiva della telefonia richiede che TAPI sia un ambiente operativo in tempo reale.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Modello sincrono/asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b3d3b58e9704719e502fa3efc11bc4dc216479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311866"
---
# <a name="synchronousasynchronous-model"></a>Modello sincrono/asincrono

La natura interattiva della telefonia richiede che TAPI sia un ambiente operativo in tempo reale. Molte delle funzioni TAPI sono necessarie per il completamento rapido e la restituzione dei risultati all'applicazione in modo sincrono. Altre funzioni (ad esempio, la composizione) potrebbero non essere in grado di essere completate in modo rapido e pertanto funzionare in modo asincrono.

Le operazioni di telefonia vengono completate in modo sincrono o asincrono. Questi due modelli sono diversi da quelli indicati di seguito. Le *funzioni sincrone* eseguono l'intera richiesta prima che il thread del chiamante possa restituire dalla chiamata di funzione. Le *funzioni asincrone* restituiscono prima che la richiesta venga eseguita completamente. Quando la richiesta asincrona viene completata in un secondo momento, il provider di servizi segnala il completamento chiamando una routine di callback inizialmente fornita da TAPI all'inizio della sequenza di inizializzazione.

-   Le operazioni asincrone hanno un parametro denominato *dwRequestID* del tipo definito [drv \_ RequestId](./drv-requestid.md) come primo parametro. Tale operazione esegue parte dell'elaborazione nella chiamata di funzione e il resto della relativa elaborazione in un thread di esecuzione indipendente dopo che è stata restituita la chiamata di funzione. Quando la funzione restituisce, restituisce un risultato di errore negativo o il *dwRequestID* (positivo) passato nella chiamata di funzione. Il risultato dell'errore negativo indica che l'operazione è stata completata e non è riuscita. Il *dwRequestID* positivo restituito indica che l'operazione continua nel thread indipendente. In tal caso, il provider di servizi chiama infine la procedura di [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) , passando *dwRequestID* e un codice risultato per indicare il risultato dell'operazione. Il codice risultato è zero per l'esito positivo o uno dello stesso set di risultati di errore (negativo). In ogni caso, il provider di servizi non deve mai restituire zero o un valore positivo diverso da *dwRequestID* da una funzione designata come asincrona perché questa operazione può produrre risultati imprevisti. I provider di servizi devono copiare sempre i dati di input dalla memoria dell'applicazione nella memoria del provider di servizi prima di restituire una funzione asincrona.
-   Le operazioni sincrone non hanno *dwRequestID* come primo parametro. Tale operazione esegue tutta la relativa elaborazione nel thread di esecuzione del chiamante, restituendo il risultato finale quando restituisce. Il risultato è zero per l'esito positivo o un codice di errore negativo per l'errore. Il provider di servizi non chiama [**il \_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) per le operazioni sincrone.

È interessante considerare la tempistica di un callback di completamento rispetto a quando la richiesta originale restituisce. Una tipica richiesta asincrona viene implementata dal provider di servizi come nel seguente pseudocodice:

``` syntax
Some_request(Request_ID, ...) {
  check parameters for validity
  check device state for validity
  store Request_ID for Completion Interrupt Handler's use
  manipulate device registers to start physical operation
  return Request_ID  // to indicate asynch operation
}
Operation Completion Interrupt Handler: {
  if operation was successful then
    call "completion" callback passing Request_ID and "success"
  else
    call "completion" callback passing Request_ID and "error num"
  endif
}
```

Se l'operazione viene completata molto rapidamente (o la richiesta originale restituisce molto lentamente), è possibile che il gestore di interrupt eseguito al termine di un'operazione fisica venga attivato prima che la richiesta originale venga restituita all'applicazione o anche a TAPI. Questo comportamento è consentito. TAPI garantisce che la notifica di completamento finale per l'applicazione venga recapitata dopo la restituzione della richiesta originale.

**TAPI 2. x:** Elenca lo stato che indica se ogni funzione viene completata in modo sincrono o asincrono nella [Guida di riferimento alle funzioni rapide TAPI](./tapi-quick-function-reference.md).

 

 
