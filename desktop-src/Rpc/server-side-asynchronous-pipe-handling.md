---
title: Gestione della pipe asincrona sul lato server
description: La routine Manager di una funzione asincrona riceve sempre l'handle asincrono come primo parametro.
ms.assetid: ddf9c319-6c4d-4de1-ab29-0ef9b76531ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b0f11372090f1fd181c0d7272aa1446e5e3d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046853"
---
# <a name="server-side-asynchronous-pipe-handling"></a>Gestione della pipe asincrona sul lato server

La routine Manager di una funzione asincrona riceve sempre l'handle asincrono come primo parametro. Il server utilizza questo handle per inviare la risposta e inviare i dati della pipe non appena diventano disponibili. L'handle rimane valido fino a quando non viene chiamato [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) , la chiamata viene interrotta da [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)oppure si verifica un'eccezione nella routine Manager. L'applicazione deve tenere traccia di tutti i puntatori di primo livello per \[ **i** \] parametri out e out \[  \] , per poterli aggiornare prima di completare la chiamata. L'applicazione deve inoltre tenere traccia delle pipe \[ [**in**](/windows/desktop/Midl/in) \] e \[ [**out**](/windows/desktop/Midl/out-idl) \] .

Il server invia i dati della pipe asincrona allo stesso modo del client. Vedere [gestione della pipe asincrona sul lato client](client-side-asynchronous-pipe-handling.md).

Il server riceve i dati della pipe asincrona nello stesso modo del client. Se il meccanismo Receive è una chiamata di procedura asincrona (APC), il server deve specificare un handle di thread (in pAsync->u. APC. hThread) e registrare l'handle asincrono con la libreria di Runtime.

## <a name="example"></a>Esempio

In questo esempio, la routine di Server Manager, MyAsyncPipeFunc, gestisce la chiamata di procedura remota dal client.


```C++
typedef struct 
{
    PRPC_ASYNC_STATE pAsync;
    ASYNC_INTPIPE *inpipe;
    ASYNC_INTPIPE *outpipe;
    int i;
    int *b;
    int PipeBuffer[ASYNC_CHUNK_SIZE];
} PIPE_CALL_COOKIE;
 
void MyAsyncPipeFunc(
    IN PRPC_ASYNC_STATE pAsync,
    IN RPC_BINDING_HANDLE hBinding,
    IN int a,
    IN ASYNC_INTPIPE *inpipe,
    OUT ASYNC_INTPIPE *outpipe,
    OUT int *b)
{
    unsigned long ThreadIdentifier;
    HANDLE HandleToThread;
    PIPE_CALL_COOKIE *PipeCallCookie;
 
    PipeCallCookie = new PIPE_CALL_COOKIE;
    PipeCallCookie->pAsync = pAsync;
    PipeCallCookie->inpipe = inpipe;
    PipeCallCookie->outpipe = outpipe;
    PipeCallCookie->b = b;
 
    pAsync->u.APC.hThread = 0;
    pAsync->u.APC.hThread = CreateThread(
                                0, DefaultThreadStackSize,
                                (LPTHREAD_START_ROUTINE)   
                                ThreadProcPipes,
                                PipeCallCookie, 0,
                                &ThreadIdentifier);
}// endMyAsyncPipeFunc
 
//Sending pipe data
//This APC routine is called when a pipe send completes, 
//or when an asynchronous call completes. 
 
//This thread routine receives pipe data, processes the call, 
//sends the reply back to the client, and 
//completes the asynchronous call.
 
void ThreadProcPipes(IN PIPE_CALL_COOKIE  *Cookie)
{
    int *ptr ;
    int  n ;
    int retval ;
 
    while (pAsync->u.APC.hThread == 0)
    {
        Sleep(10);
    }
 
    pAsync->Flags = RPC_C_NOTIFY_ON_SEND_COMPLETE;
    pAsync->UserInfo = (void *) PipeCallCookie;
    pAsync->NotificationType = RpcNotificationTypeApc;
    pAsync->u.APC.NotificationRoutine = MyAsyncPipeAPCRoutine;
    pAsync->u.APC.hThread = HandleToThread;
 
    RpcAsyncRegisterHandle(pAsync);
 
    while (!fDone)
    {
        Cookie->inpipe->pull(
            Cookie->inpipe.state,
            (int *) Cookie->PipeBuffer,
            ASYNC_CHUNK_SIZE,
            &num_elements);
        switch (Status)
        {
            case RPC_S_ASYNC_CALL_PENDING:
                if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
                {
                    RpcRaiseException(APP_ERROR) ;
                }
            break;
 
            case RPC_S_OK:
                if (num_elements == 0)
                {
                    fDone = 1;
                }
                else
                {
                    // process the received data
                }
            break;
 
            default:
                fDone = 1;
            break;
        }
    }
 
    Cookie->i = 1;
    Cookie->outpipe->push(
        Cookie->outpipe.state,
        0,
        Cookie->PipeBuffer,
        ASYNC_CHUNK_SIZE) ;
 
    while (Cookie->i < ASYNC_NUM_CHUNKS+1)
    {
        if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
        {
            RpcRaiseException (APP_ERROR);
        }
    }
    // sending non pipe reply
    *(Cookie->b) = 10;
    Status = RpcAsyncCompleteCall (Cookie->pAsync, &retval);
}
 
void MyAsyncPipeAPCRoutine (
    IN PRPC_ASYNC_STATE pAsync,
    IN void *Context,
    IN unsigned int Flags)
{
    PIPE_CALL_COOKIE *Cookie = (PIPE_CALL_COOKIE *) pAsync->UserInfo;
 
    if (Flags & RPC_ASYNC_PIPE_SEND_COMPLETE)
    {
        if (Cookie->i & ASYNC_NUM_CHUNKS)
        {
            Cookie->outpipe->push(
                Cookie->outpipe.state,
                0,
                (int *) Cookie->PipeBuffer,
                ASYNC_CHUNK_SIZE);
            Cookie->i++ ;
        }
        else
        {
            pAsync->Flags = 0;
            Cookie->outpipe->push(Cookie->outpipe.state, 0, 0, 0);
            Cookie->i++;
        }
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipe](pipes.md)
</dt> <dt>

[MIDL asincrono](/windows/desktop/Midl/async)
</dt> <dt>

[RPC asincrona sul lato server](server-side-asynchronous-rpc.md)
</dt> </dl>

 

 