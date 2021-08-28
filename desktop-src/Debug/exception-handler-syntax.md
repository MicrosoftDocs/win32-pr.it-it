---
description: Le \_ \_ parole chiave try e except vengono \_ \_ usate per costruire un gestore eccezioni basato su frame. Nell'esempio seguente viene illustrata la struttura di un gestore di eccezioni.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Exception-Handler sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd24b3ffc84a3469c7c8d97ce505a0292ee538ea8f0b9c1d604bf34f65203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912741"
---
# <a name="exception-handler-syntax"></a>Exception-Handler sintassi

Le **\_ \_ parole chiave try** e **\_ \_ except** vengono usate per costruire un gestore eccezioni basato su frame. Nell'esempio seguente viene illustrata la struttura di un gestore di eccezioni.


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



Si noti che il **\_ \_ blocco try** e il blocco del gestore eccezioni richiedono parentesi graffe ( {} ). **L'uso di un'istruzione goto** per passare al corpo di un blocco **\_ \_ try** o a un blocco del gestore di eccezioni non è consentito. Questa regola si applica sia ai gestori di eccezioni che ai gestori di terminazione.

Il **\_ \_ blocco try** contiene il corpo sorvegliato del codice protetto dal gestore di eccezioni. Una funzione può avere un numero qualsiasi di gestori di eccezioni e queste istruzioni di gestione delle eccezioni possono essere annidate all'interno della stessa funzione o in funzioni diverse. Se si verifica un'eccezione all'interno del **\_ \_ blocco try,** il sistema assume il controllo e avvia la ricerca di un gestore eccezioni. Per una descrizione dettagliata di questa ricerca, vedere [Gestione delle eccezioni](exception-handling.md).

Il gestore eccezioni riceve solo le eccezioni che si verificano all'interno di un singolo thread. Ciò significa che se un blocco **\_ \_ try** contiene una chiamata alla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) le eccezioni che si verificano all'interno del nuovo processo o thread non vengono inviati a questo gestore.

Il sistema valuta l'espressione di filtro di ogni gestore di eccezioni proteggendo il codice in cui si è verificata l'eccezione fino a quando l'eccezione non viene gestita o non sono presenti altri gestori. Un'espressione di filtro deve essere valutata come uno dei tre valori seguenti.



| Valore                              | Significato                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GESTORE \_ DI ESECUZIONE DELLE \_ ECCEZIONI**    | Il sistema trasferisce il controllo al gestore eccezioni e l'esecuzione continua nel stack frame in cui si trova il gestore.                                                                                       |
| **RICERCA CONTINUA \_ \_ ECCEZIONI**    | Il sistema continua a cercare un gestore.                                                                                                                                                                          |
| **ESECUZIONE DI EXCEPTION \_ CONTINUE \_** | Il sistema arresta la ricerca di un gestore e restituisce il controllo fino al punto in cui si è verificata l'eccezione. Se l'eccezione non è concisa, viene generata un'eccezione **EXCEPTION \_ NONCONTINUABLE \_ EXCEPTION.** |



 

L'espressione di filtro viene valutata nel contesto della funzione in cui si trova il gestore eccezioni, anche se l'eccezione può essere stata generata in una funzione diversa. Ciò significa che l'espressione di filtro può accedere alle variabili locali della funzione. Analogamente, il blocco del gestore eccezioni può accedere alle variabili locali della funzione in cui si trova.

Per altri esempi, vedere [Uso di un gestore eccezioni](using-an-exception-handler.md).

Per altre informazioni sulle espressioni di filtro e sulle funzioni di filtro, vedere [Gestione delle eccezioni](frame-based-exception-handling.md)basata su frame.

 

 
