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
# <a name="indicate-errors-by-exceptions"></a><span data-ttu-id="9b7a3-103">Indica errori per eccezioni</span><span class="sxs-lookup"><span data-stu-id="9b7a3-103">Indicate Errors by Exceptions</span></span>

<span data-ttu-id="9b7a3-104">Per i programmatori C tradizionali, gli errori vengono comunemente restituiti tramite valori restituiti o un \[ parametro out speciale \] che restituisce il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-104">For traditional C programmers, errors are commonly returned through return values, or a special \[out\] parameter that returns the error code.</span></span> <span data-ttu-id="9b7a3-105">In questo modo, le interfacce vengono implementate nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="9b7a3-105">This leads to interfaces implemented the following way:</span></span>

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

<span data-ttu-id="9b7a3-106">Il problema di questo approccio è che i valori restituiti RPC sono semplicemente Long Integer.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-106">The problem with this approach is that RPC return values are simply long integers.</span></span> <span data-ttu-id="9b7a3-107">Non hanno un significato speciale come errori (si noti [**che \_ lo \_ stato di errore t**](/windows/desktop/Midl/error-status-t) non ha alcuna semantica speciale sul lato server), che ha implicazioni importanti.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-107">They have no special meaning as errors (note that [**error\_status\_t**](/windows/desktop/Midl/error-status-t) has no special semantics on the server side), which carries important implications.</span></span>

<span data-ttu-id="9b7a3-108">Per prima cosa, RPC non viene avvisato dell'esito negativo dell'operazione. tenta di annullare il marshalling \[ di tutti gli argomenti in, out \] e \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="9b7a3-108">First, RPC is not alerted that the operation failed; it attempts to unmarshal all \[in, out\] and \[out\] arguments.</span></span> <span data-ttu-id="9b7a3-109">Anche la semantica di errore degli handle di contesto è diversa.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-109">The failure semantics of context handles are also different.</span></span> <span data-ttu-id="9b7a3-110">Il pacchetto restituito al client è essenzialmente un pacchetto con esito positivo, con il codice di errore nascosto nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-110">The packet returned to the client is essentially a success packet, with the error code buried deep in the packet.</span></span> <span data-ttu-id="9b7a3-111">Questo significa anche che RPC non usa le informazioni estese sugli errori, quindi il software client spesso non riesce a discernere il punto in cui la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-111">This also means RPC does not use extended error information, so client software often is unable to discern where the call failed.</span></span>

<span data-ttu-id="9b7a3-112">Un approccio molto migliore è quello di indicare gli errori nelle routine del server RPC generando eccezioni di gestione delle eccezioni strutturate (non C++).</span><span class="sxs-lookup"><span data-stu-id="9b7a3-112">Indicating errors in RPC server routines by throwing Structured Exception Handling (SEH) exceptions (not C++) is a much better approach.</span></span> <span data-ttu-id="9b7a3-113">Quando viene generata un'eccezione SEH, il controllo passa direttamente alla fase di esecuzione RPC.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-113">When an SEH exception is thrown, control goes directly to the RPC run time.</span></span> <span data-ttu-id="9b7a3-114">Un errore si verifica talvolta in modo approfondito in una routine che non può essere pulita correttamente ed è necessario indicare un errore al chiamante.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-114">An error sometimes occurs deep in a routine that cannot properly clean up, and it needs to indicate an error to its caller.</span></span> <span data-ttu-id="9b7a3-115">La routine deve restituire un errore al chiamante, che a sua volta può restituire un errore al chiamante e così via.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-115">The routine should return an error to its caller, which in turn can return an error to its caller and so on.</span></span> <span data-ttu-id="9b7a3-116">Tuttavia, l'ultima routine del server nello stack deve generare un'eccezione prima che venga restituito a RPC per indicare a RPC che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="9b7a3-116">However, the last server routine on the stack should throw an exception before it returns to RPC to indicate to RPC that an error occurred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b7a3-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b7a3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b7a3-118">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="9b7a3-118">Exception Handling</span></span>](exception-handling.md)
</dt> </dl>

 

 