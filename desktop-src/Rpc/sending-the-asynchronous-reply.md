---
title: Invio della risposta asincrona
description: Quando la chiamata asincrona è completa, il server invia una risposta al client chiamando la funzione RpcAsyncCompleteCall e passando l'handle asincrono.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045165"
---
# <a name="sending-the-asynchronous-reply"></a><span data-ttu-id="9eb3e-103">Invio della risposta asincrona</span><span class="sxs-lookup"><span data-stu-id="9eb3e-103">Sending the Asynchronous Reply</span></span>

<span data-ttu-id="9eb3e-104">Quando la chiamata asincrona è completa, il server invia una risposta al client chiamando la funzione [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e passando l'handle asincrono.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-104">When the asynchronous call is complete, the server sends a reply to the client by calling the [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) function and passing it the asynchronous handle.</span></span> <span data-ttu-id="9eb3e-105">Questa chiamata è necessaria anche se la chiamata asincrona ha un valore restituito void e nessun \[ \] parametro out.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-105">This call is necessary even if the asynchronous call has a void return value and no \[out\] parameters.</span></span> <span data-ttu-id="9eb3e-106">Se la funzione ha un valore restituito, viene passata per riferimento a **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-106">If the function has a return value, it is passed by reference to **RpcAsyncCompleteCall**.</span></span>

<span data-ttu-id="9eb3e-107">Quando il server chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) o **RpcAsyncAbortCall** oppure una chiamata viene completata perché è stata generata un'eccezione nella routine Server-Manager, la libreria di runtime RPC Elimina automaticamente l'handle asincrono del server.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-107">When the server calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) or **RpcAsyncAbortCall**, or a call completes because an exception was raised in the server-manager routine, the RPC run-time library automatically destroys the server's asynchronous handle.</span></span>

> [!Note]  
> <span data-ttu-id="9eb3e-108">Il server deve completare l'aggiornamento dei \[ parametri in, out \] e \[ out \] prima di chiamare **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-108">The server must finish updating the \[in, out\] and \[out\] parameters before calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="9eb3e-109">Non è possibile apportare modifiche a tali parametri o all'handle asincrono dopo aver chiamato **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-109">No changes can be made to those parameters or to the asynchronous handle after calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="9eb3e-110">Se la chiamata alla funzione **RpcAsyncCompleteCall** ha esito negativo, il runtime RPC libera i parametri.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-110">If the **RpcAsyncCompleteCall** function call fails, the RPC runtime frees the parameters.</span></span>

 

<span data-ttu-id="9eb3e-111">Nell'esempio seguente viene illustrata una semplice chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-111">The following example demonstrates a simple asynchronous procedure call.</span></span>


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



<span data-ttu-id="9eb3e-112">Per semplicità, questa routine del server asincrona non elabora i dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-112">For the sake of simplicity, this asynchronous server routine does not process actual data.</span></span> <span data-ttu-id="9eb3e-113">Si limita a dormire per un po'.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-113">It simply puts itself to sleep for awhile.</span></span>

> [!Note]  
> <span data-ttu-id="9eb3e-114">La funzione **RpcAsyncCompleteCall** può essere chiamata sul thread che ha ricevuto la chiamata o su qualsiasi altro thread nel processo.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-114">The **RpcAsyncCompleteCall** function can be called either on the thread that received the call, or on any other thread in the process.</span></span> <span data-ttu-id="9eb3e-115">Se tutti i dati necessari per completare la chiamata sono immediatamente disponibili, il server può riempirli nello stesso thread e chiamare **RpcAsyncCompleteCall** sullo stesso thread.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-115">If all the data necessary to complete the call are readily available, the server may fill them in on the same thread, and call the **RpcAsyncCompleteCall** on the same thread.</span></span> <span data-ttu-id="9eb3e-116">Questo approccio consente di risparmiare un cambio di contesto e migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-116">This approach saves some context switching and improves performance.</span></span> <span data-ttu-id="9eb3e-117">Tali chiamate sono denominate opportunisticamente asincrono.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-117">Such calls are called opportunistically asynchronous.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9eb3e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9eb3e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eb3e-119">**\_stato asincrono \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="9eb3e-119">**RPC\_ASYNC\_STATE**</span></span>](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[<span data-ttu-id="9eb3e-120">**RpcAsyncCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="9eb3e-120">**RpcAsyncCompleteCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[<span data-ttu-id="9eb3e-121">**RpcAsyncAbortCall**</span><span class="sxs-lookup"><span data-stu-id="9eb3e-121">**RpcAsyncAbortCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[<span data-ttu-id="9eb3e-122">**RpcServerTestCancel**</span><span class="sxs-lookup"><span data-stu-id="9eb3e-122">**RpcServerTestCancel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




