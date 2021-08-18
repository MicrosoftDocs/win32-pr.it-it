---
title: Uso di handle di associazione ed esecuzione di chiamate RPC
description: Un errore comune tra i programmatori RPC è la gestione di tutte le eccezioni.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1350e29344d09f42417a30fa3d32729d7ddd02247b17f80bccd0ae537c6c8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010809"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a>Uso di handle di associazione ed esecuzione di chiamate RPC

Un errore comune tra i programmatori RPC è la gestione di tutte le eccezioni. Molti programmatori strutturano gli handle di eccezione come segue:

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

Il problema con questo gestore è che intercetta tutti gli errori, inclusi gli errori nel programma client. L'intercettazione degli errori nel programma client rende più difficile il debug. Il modo corretto per strutturare un gestore eccezioni è il seguente:

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

Questo gestore di eccezioni ha il vantaggio di consentire l'esecuzione di un determinato intervallo di errori. Questi errori non verranno mai restituiti dal server, perché indicano un problema sul lato client.

Inoltre, è consigliabile usare gli attributi handle di contesto strict e type strict per garantire che la fase di esecuzione RPC crei un handle di contesto in un'interfaccia che può essere passata come argomento solo ai metodi di tale **\[** [ \_ \_](/windows/desktop/Midl/strict-context-handle) **\]** **\[** [ \_ \_ \_](/windows/desktop/Midl/type-strict-context-handle) **\]** interfaccia. In questo modo si eviteranno gli errori del server che si verificano quando gli handle di contesto vengono aperti e passati tra interfacce diverse presenti all'interno dello stesso processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[handle \_ di contesto \_ strict](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[handle \_ di contesto type strict \_ \_](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 