---
title: Utilizzo di handle di associazione e esecuzione di chiamate RPC
description: Un errore comune tra i programmatori RPC è la gestione di tutte le eccezioni.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728850"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a><span data-ttu-id="3304d-103">Utilizzo di handle di associazione e esecuzione di chiamate RPC</span><span class="sxs-lookup"><span data-stu-id="3304d-103">Using Binding Handles and Making RPC Calls</span></span>

<span data-ttu-id="3304d-104">Un errore comune tra i programmatori RPC è la gestione di tutte le eccezioni.</span><span class="sxs-lookup"><span data-stu-id="3304d-104">A common mistake among RPC programmers is handling all exceptions.</span></span> <span data-ttu-id="3304d-105">Molti programmatori strutturano gli handle di eccezione come i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3304d-105">Many programmers structure their exception handles like the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="3304d-106">Il problema di questo gestore è che intercetta tutti gli errori, inclusi quelli nel programma client.</span><span class="sxs-lookup"><span data-stu-id="3304d-106">The problem with this handler is that it catches all errors, including errors in the client program.</span></span> <span data-ttu-id="3304d-107">La rilevazione degli errori nel programma client rende più difficile il debug.</span><span class="sxs-lookup"><span data-stu-id="3304d-107">Catching errors in the client program makes debugging more difficult.</span></span> <span data-ttu-id="3304d-108">Il modo corretto per strutturare un gestore di eccezioni è il seguente:</span><span class="sxs-lookup"><span data-stu-id="3304d-108">The proper way to structure an exception handler is the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="3304d-109">Questo gestore di eccezioni ha il vantaggio di consentire un certo intervallo di errori tramite.</span><span class="sxs-lookup"><span data-stu-id="3304d-109">This exception handler has the advantage of letting a certain range of errors through.</span></span> <span data-ttu-id="3304d-110">Questi errori non verranno mai restituiti dal server, perché indicano un problema lato client.</span><span class="sxs-lookup"><span data-stu-id="3304d-110">These errors will never be returned by the server, because they indicate a client side problem.</span></span>

<span data-ttu-id="3304d-111">Inoltre, è consigliabile utilizzare gli **\[** [attributi \_ strict \_ context](/windows/desktop/Midl/strict-context-handle) handle **\]** e **\[** [ \_ strict \_ Context \_ handle](/windows/desktop/Midl/type-strict-context-handle) **\]** per garantire che il runtime RPC crei un handle di contesto in un'interfaccia che può essere passata come argomento solo ai metodi di tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3304d-111">Additionally, the use of the **\[**[strict\_context\_handle](/windows/desktop/Midl/strict-context-handle)**\]** and **\[**[type\_strict\_context\_handle](/windows/desktop/Midl/type-strict-context-handle)**\]** attributes are recommended to ensure the RPC run time creates a context handle on one interface that can be passed as an argument only to methods of that interface.</span></span> <span data-ttu-id="3304d-112">In questo modo si eviteranno errori del server che si verificano quando gli handle di contesto vengono aperti e passati tra interfacce diverse presenti nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="3304d-112">Doing so will prevent server failures that occur when context handles are opened and passed between different interfaces that exist within the same process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3304d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3304d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3304d-114">\_handle di contesto Strict \_</span><span class="sxs-lookup"><span data-stu-id="3304d-114">strict\_context\_handle</span></span>](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[<span data-ttu-id="3304d-115">tipo \_ strict \_ handle di contesto \_</span><span class="sxs-lookup"><span data-stu-id="3304d-115">type\_strict\_context\_handle</span></span>](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 