---
title: Indica errori per eccezioni
description: Per i programmatori C tradizionali, gli errori vengono comunemente restituiti tramite valori restituiti o un parametro \ out \ speciale che restituisce il codice di errore.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872761"
---
# <a name="indicate-errors-by-exceptions"></a>Indica errori per eccezioni

Per i programmatori C tradizionali, gli errori vengono comunemente restituiti tramite valori restituiti o un \[ parametro out speciale \] che restituisce il codice di errore. In questo modo, le interfacce vengono implementate nel modo seguente:

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

Il problema di questo approccio è che i valori restituiti RPC sono semplicemente Long Integer. Non hanno un significato speciale come errori (si noti [**che \_ lo \_ stato di errore t**](/windows/desktop/Midl/error-status-t) non ha alcuna semantica speciale sul lato server), che ha implicazioni importanti.

Per prima cosa, RPC non viene avvisato dell'esito negativo dell'operazione. tenta di annullare il marshalling \[ di tutti gli argomenti in, out \] e \[ out \] . Anche la semantica di errore degli handle di contesto è diversa. Il pacchetto restituito al client è essenzialmente un pacchetto con esito positivo, con il codice di errore nascosto nel pacchetto. Questo significa anche che RPC non usa le informazioni estese sugli errori, quindi il software client spesso non riesce a discernere il punto in cui la chiamata non è riuscita.

Un approccio molto migliore è quello di indicare gli errori nelle routine del server RPC generando eccezioni di gestione delle eccezioni strutturate (non C++). Quando viene generata un'eccezione SEH, il controllo passa direttamente alla fase di esecuzione RPC. Un errore si verifica talvolta in modo approfondito in una routine che non può essere pulita correttamente ed è necessario indicare un errore al chiamante. La routine deve restituire un errore al chiamante, che a sua volta può restituire un errore al chiamante e così via. Tuttavia, l'ultima routine del server nello stack deve generare un'eccezione prima che venga restituito a RPC per indicare a RPC che si è verificato un errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle eccezioni](exception-handling.md)
</dt> </dl>

 

 