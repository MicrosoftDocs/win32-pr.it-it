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
# <a name="using-binding-handles-and-making-rpc-calls"></a>Utilizzo di handle di associazione e esecuzione di chiamate RPC

Un errore comune tra i programmatori RPC è la gestione di tutte le eccezioni. Molti programmatori strutturano gli handle di eccezione come i seguenti:

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

Il problema di questo gestore è che intercetta tutti gli errori, inclusi quelli nel programma client. La rilevazione degli errori nel programma client rende più difficile il debug. Il modo corretto per strutturare un gestore di eccezioni è il seguente:

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

Questo gestore di eccezioni ha il vantaggio di consentire un certo intervallo di errori tramite. Questi errori non verranno mai restituiti dal server, perché indicano un problema lato client.

Inoltre, è consigliabile utilizzare gli **\[** [attributi \_ strict \_ context](/windows/desktop/Midl/strict-context-handle) handle **\]** e **\[** [ \_ strict \_ Context \_ handle](/windows/desktop/Midl/type-strict-context-handle) **\]** per garantire che il runtime RPC crei un handle di contesto in un'interfaccia che può essere passata come argomento solo ai metodi di tale interfaccia. In questo modo si eviteranno errori del server che si verificano quando gli handle di contesto vengono aperti e passati tra interfacce diverse presenti nello stesso processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_handle di contesto Strict \_](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[tipo \_ strict \_ handle di contesto \_](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 