---
description: La natura interattiva della telefonia richiede che TAPI sia un ambiente operativo in tempo reale.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Modello sincrono/asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354bc8e32cdd1bb2bcefac0fe3e4d77361f3be9e37cd6a1549aa157d4b997f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975521"
---
# <a name="synchronousasynchronous-model"></a>Modello sincrono/asincrono

La natura interattiva della telefonia richiede che TAPI sia un ambiente operativo in tempo reale. Molte delle funzioni TAPI sono necessarie per completare rapidamente e restituire i risultati all'applicazione in modo sincrono. Altre funzioni, ad esempio la composizione, potrebbero non essere in grado di essere completate con la rapidità e quindi operare in modo asincrono.

Le operazioni di telefonia vengono completate in modo sincrono o asincrono. Questi due modelli differiscono come indicato di seguito. *Le funzioni sincrone* eseguono l'intera richiesta prima che il thread del chiamante sia autorizzato a restituire dalla chiamata di funzione. *Le funzioni asincrone* restituiscono prima che la richiesta sia stata eseguita nella sua interezza. Quando la richiesta asincrona viene completata in un secondo momento, il provider di servizi segnala il completamento chiamando una routine di callback fornita in origine da TAPI nella sequenza di inizializzazione.

-   Le operazioni asincrone hanno un *parametro denominato dwRequestID* del tipo [definito DRV \_ REQUESTID](./drv-requestid.md) come primo parametro. Tale operazione esegue parte dell'elaborazione nella chiamata di funzione e il resto dell'elaborazione in un thread di esecuzione indipendente dopo che la chiamata di funzione è stata restituita. Quando la funzione viene restituita, restituisce un risultato di errore negativo o il *valore dwRequestID* (positivo) passato nella chiamata di funzione. Il risultato negativo dell'errore indica che l'operazione è stata completata (e non riuscita). Il *valore dwRequestID positivo* restituito indica che l'operazione continua nel thread indipendente. In tal caso, il provider di servizi chiama infine la procedura [**ASYNC \_ COMPLETION,**](/windows/win32/api/tspi/nc-tspi-async_completion) passando *dwRequestID* e un codice di risultato per indicare il risultato dell'operazione. Il codice del risultato è zero per l'esito positivo o uno dello stesso set di risultati degli errori (negativi). In ogni caso, il provider di servizi non deve mai restituire zero o qualsiasi valore positivo diverso da *dwRequestID* da una funzione designata come asincrona perché questa operazione può produrre risultati imprevisti. I provider di servizi devono sempre copiare i dati di input dalla memoria dell'applicazione alla memoria del provider di servizi prima di restituire da una funzione asincrona.
-   Le operazioni sincrone non hanno *dwRequestID* come primo parametro. Tale operazione esegue tutta l'elaborazione nel thread di esecuzione del chiamante, restituisce il risultato finale quando viene restituito. Il risultato è zero per l'esito positivo o un codice di errore negativo per l'errore. Il provider di servizi non chiama [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) per le operazioni sincrone.

È interessante considerare la tempistica di un callback di "completamento" rispetto a quando la richiesta originale viene restituita. Una richiesta asincrona tipica verrà implementata dal provider di servizi come nello pseudocodice seguente:

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

Se l'operazione viene completata molto rapidamente (o la richiesta originale viene restituita molto lentamente), è possibile che il gestore di interrupt eseguito al completamento di un'operazione fisica venga attivato prima che la richiesta originale restituisca all'applicazione o anche a TAPI. Questo comportamento è consentito. TAPI garantisce che la notifica di completamento finale all'applicazione viene recapitata dopo la restituita della richiesta originale.

**TAPI 2.x:** Elenca lo stato che indica se ogni funzione viene completata in modo sincrono o asincrono in [Riferimento alle funzioni rapide TAPI.](./tapi-quick-function-reference.md)

 

 
