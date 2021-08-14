---
title: Indicare gli errori in base alle eccezioni
description: Per i programmatori C tradizionali, gli errori vengono in genere restituiti tramite valori restituiti o un parametro speciale \ out\ che restituisce il codice di errore.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 816f63f9378c3f2338c7bed6f6a9b5f785d3e138e4762c355aa1932887fd14c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928917"
---
# <a name="indicate-errors-by-exceptions"></a>Indicare gli errori in base alle eccezioni

Per i programmatori C tradizionali, gli errori vengono in genere restituiti tramite valori restituiti o uno speciale \[ parametro out che restituisce il codice di \] errore. Ciò comporta l'implementazione delle interfacce nel modo seguente:

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

Il problema con questo approccio è che i valori restituiti rpc sono semplicemente valori interi lunghi. Non hanno un significato speciale come errori (si noti che lo stato di errore [**\_ \_ t**](/windows/desktop/Midl/error-status-t) non ha una semantica speciale sul lato server), con implicazioni importanti.

In primo luogo, RPC non viene avvisato che l'operazione non è riuscita. tenta di eseguire l'unmarshaling di tutti gli argomenti \[ in ingresso, \] in uscita e in \[ \] uscita. Anche la semantica di errore degli handle di contesto è diversa. Il pacchetto restituito al client è essenzialmente un pacchetto con esito positivo, con il codice di errore nascosto nel pacchetto. Ciò significa anche che RPC non usa informazioni estese sugli errori, pertanto il software client spesso non è in grado di individuare la posizione in cui la chiamata non è riuscita.

L'indicazione di errori nelle routine del server RPC generando eccezioni SEH (Structured Exception Handling) (non C++) è un approccio molto migliore. Quando viene generata un'eccezione SEH, il controllo passa direttamente alla fase di esecuzione RPC. A volte si verifica un errore in una routine che non è in grado di eseguire correttamente la pulizia e deve indicare un errore al chiamante. La routine deve restituire un errore al chiamante, che a sua volta può restituire un errore al chiamante e così via. Tuttavia, l'ultima routine del server nello stack deve generare un'eccezione prima di essere restituita a RPC per indicare a RPC che si è verificato un errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle eccezioni](exception-handling.md)
</dt> </dl>

 

 