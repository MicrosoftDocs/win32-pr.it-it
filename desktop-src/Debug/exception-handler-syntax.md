---
description: Le \_ \_ \_ \_ parole chiave try e except vengono usate per costruire un gestore di eccezioni basato su frame. Nell'esempio seguente viene illustrata la struttura di un gestore di eccezioni.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Sintassi Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522874"
---
# <a name="exception-handler-syntax"></a>Sintassi Exception-Handler

Le parole chiave **\_ \_ try** e **\_ \_ except** vengono usate per costruire un gestore di eccezioni basato su frame. Nell'esempio seguente viene illustrata la struttura di un gestore di eccezioni.


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



Si noti che il blocco **\_ \_ try** e il blocco del gestore di eccezioni richiedono le parentesi graffe ( {} ). Non è consentito usare un'istruzione **goto** per passare al corpo di un blocco **\_ \_ try** o in un blocco del gestore di eccezioni. Questa regola si applica sia ai gestori di eccezioni che ai gestori di terminazione.

Il blocco **\_ \_ try** contiene il corpo sorvegliato del codice protetto dal gestore di eccezioni. Una funzione può avere un numero qualsiasi di gestori di eccezioni e queste istruzioni di gestione delle eccezioni possono essere annidate all'interno della stessa funzione o in funzioni diverse. Se si verifica un'eccezione all'interno del blocco **\_ \_ try** , il sistema acquisisce il controllo e inizia la ricerca di un gestore di eccezioni. Per una descrizione dettagliata di questa ricerca, vedere [gestione delle eccezioni](exception-handling.md).

Il gestore di eccezioni riceve solo le eccezioni che si verificano all'interno di un singolo thread. Ciò significa che se un blocco **\_ \_ try** contiene una chiamata alla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , le eccezioni che si verificano all'interno del nuovo processo o del nuovo thread non vengono inviate a questo gestore.

Il sistema valuta l'espressione di filtro di ogni gestore di eccezioni che protegge il codice in cui si è verificata l'eccezione fino a quando l'eccezione non viene gestita o non sono presenti altri gestori. Un'espressione di filtro deve essere valutata come uno dei tre valori seguenti.



| Valore                              | Significato                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_gestore di esecuzione eccezioni \_**    | Il sistema trasferisce il controllo al gestore di eccezioni e l'esecuzione continua nel stack frame in cui viene individuato il gestore.                                                                                       |
| **\_continua \_ ricerca eccezione**    | Il sistema continua la ricerca di un gestore.                                                                                                                                                                          |
| **esecuzione dell'eccezione \_ continua \_** | Il sistema arresta la ricerca di un gestore e restituisce il controllo al punto in cui si è verificata l'eccezione. Se l'eccezione è non continuabile, viene generata un'eccezione di eccezione non **\_ continuabile \_** . |



 

L'espressione di filtro viene valutata nel contesto della funzione in cui si trova il gestore eccezioni, anche se l'eccezione potrebbe essersi verificata in una funzione diversa. Ciò significa che l'espressione di filtro può accedere alle variabili locali della funzione. Analogamente, il blocco del gestore di eccezioni può accedere alle variabili locali della funzione in cui si trova.

Per altri esempi, vedere [uso di un gestore di eccezioni](using-an-exception-handler.md).

Per ulteriori informazioni sulle espressioni di filtro e sulle funzioni di filtro, vedere [gestione delle eccezioni basata su frame](frame-based-exception-handling.md).

 

 
