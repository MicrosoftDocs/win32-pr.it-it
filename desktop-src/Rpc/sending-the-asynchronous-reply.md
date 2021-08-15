---
title: Invio della risposta asincrona
description: Al termine della chiamata asincrona, il server invia una risposta al client chiamando la funzione RpcAsyncCompleteCall e passando l'handle asincrono.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdcaf4db4a27a49a8025596668893518c6b6c577a0d81d91189a44ec81df4de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925579"
---
# <a name="sending-the-asynchronous-reply"></a>Invio della risposta asincrona

Al termine della chiamata asincrona, il server invia una risposta al client chiamando la [**funzione RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e passando l'handle asincrono. Questa chiamata è necessaria anche se la chiamata asincrona ha un valore restituito void e nessun \[ parametro \] out. Se la funzione ha un valore restituito, viene passata per riferimento a **RpcAsyncCompleteCall**.

Quando il server chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) o **RpcAsyncAbortCall** o una chiamata viene completata perché è stata generata un'eccezione nella routine di gestione server, la libreria di runtime RPC elimina automaticamente l'handle asincrono del server.

> [!Note]  
> Il server deve completare l'aggiornamento dei \[ parametri in, out \] e out prima di chiamare \[ \] **RpcAsyncCompleteCall**. Non è possibile apportare modifiche a tali parametri o all'handle asincrono dopo la chiamata **a RpcAsyncCompleteCall.** Se la **chiamata di funzione RpcAsyncCompleteCall** ha esito negativo, il runtime RPC libera i parametri.

 

Nell'esempio seguente viene illustrata una semplice chiamata di procedura asincrona.


```C++
#define DEFAULT_ASYNC_DELAY 20;
#define ASYNC_CANCEL_CHECK 100;

void AsyncFunc(IN PRPC_ASYNC_STATE pAsync,
               IN RPC_BINDING_HANDLE hBinding,
               IN OUT unsigned long nAsychDelay)
{
    int nReply = 1;
    RPC_STATUS status;
    unsigned long nTmpAsychDelay;
    int i;
 
    if (nAsychDelay < 0){
        nAsychDelay = DEFAULT_ASYNC_DELAY;
    }else if (nAsychDelay < 100){
        nAsychDelay = 100;
    }

    // We only call RpcServerTestCancel if the call
    // takes longer than ASYNC_CANCEL_CHECK ms
    if(nAsychDelay > ASYNC_CANCEL_CHECK){
        
        nTmpAsychDelay = nAsychDelay/100;
 
        for (i = 0; i < 100; i++){
            Sleep(nTmpAsychDelay);
 
            if (i%5 == 0){
                fprintf(stderr, 
                        "\rRunning AsyncFunc (%lu ms) (%d%c) ... ",
                        nAsychDelay, i+5, PERCENT);
 
                status = 
                    RpcServerTestCancel(
                        RpcAsyncGetCallHandle(pAsync));
                if (status == RPC_S_OK){
                    fprintf(stderr, 
                            "\nAsyncFunc has been canceled!!!\n");
                    break;
                }else if (status != RPC_S_CALL_IN_PROGRESS){
                    printf(
                        "RpcAsyncInitializeHandle returned 0x%x\n", 
                        status);
                    exit(status); 
                }
            }
        }
    }else{
        Sleep(nAsychDelay);
    }
 
    printf("\nCalling RpcAsyncCompleteCall\n");
    status = RpcAsyncCompleteCall(pAsync, &nReply);
    printf("RpcAsyncCompleteCall returned 0x%x\n", status);
    if (status){
        exit(status);
    }
}
```



Per motivi di semplicità, questa routine server asincrona non elabora i dati effettivi. Si limita a mettere in sospensione per un po'.

> [!Note]  
> La **funzione RpcAsyncCompleteCall** può essere chiamata sul thread che ha ricevuto la chiamata o su qualsiasi altro thread del processo. Se tutti i dati necessari per completare la chiamata sono immediatamente disponibili, il server può compilarli nello stesso thread e chiamare **RpcAsyncCompleteCall** nello stesso thread. Questo approccio consente di risparmiare un certo cambio di contesto e migliora le prestazioni. Tali chiamate vengono chiamate in modo opportunistico asincrono.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**STATO \_ ASINCRONO \_ RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




