---
title: Sviluppo di client con handle di contesto
description: L'unico utilizzo di un programma client per un handle di contesto consiste nel passarlo al server ogni volta che il client esegue una chiamata di procedura remota.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515982"
---
# <a name="client-development-using-context-handles"></a><span data-ttu-id="f2f62-103">Sviluppo di client con handle di contesto</span><span class="sxs-lookup"><span data-stu-id="f2f62-103">Client Development Using Context Handles</span></span>

<span data-ttu-id="f2f62-104">L'unico utilizzo di un programma client per un handle di contesto consiste nel passarlo al server ogni volta che il client esegue una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f2f62-104">The only use a client program has for a context handle is to pass it to the server each time the client makes a remote procedure call.</span></span> <span data-ttu-id="f2f62-105">Non è necessario che l'applicazione client acceda al contenuto dell'handle.</span><span class="sxs-lookup"><span data-stu-id="f2f62-105">The client application does not need to access the contents of the handle.</span></span> <span data-ttu-id="f2f62-106">Non deve tentare di modificare i dati di gestione del contesto in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="f2f62-106">It should not try to change the context handle data in any way.</span></span> <span data-ttu-id="f2f62-107">Le procedure remote richiamate dal client eseguono tutte le operazioni necessarie sul contesto del server.</span><span class="sxs-lookup"><span data-stu-id="f2f62-107">The remote procedures that the client invokes perform all necessary operations on the server's context.</span></span>

<span data-ttu-id="f2f62-108">Prima di richiedere un handle di contesto da un server, i client devono stabilire un'associazione con il server.</span><span class="sxs-lookup"><span data-stu-id="f2f62-108">Prior to requesting a context handle from a server, clients must establish a binding with the server.</span></span> <span data-ttu-id="f2f62-109">Il client può utilizzare un handle di binding automatico, implicito o esplicito.</span><span class="sxs-lookup"><span data-stu-id="f2f62-109">The client may use an automatic, implicit, or explicit binding handle.</span></span> <span data-ttu-id="f2f62-110">Con un handle di associazione valido, il client può chiamare una procedura remota sul server che restituisce un handle di contesto aperto (non **null**) o passa uno tramite un parametro **\[ out \]** nell'elenco di parametri della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f2f62-110">With a valid binding handle, the client can call a remote procedure on the server that either returns an opened (non-**NULL**) context handle or passes one through an **\[out\]** parameter in the remote procedure's parameter list.</span></span>

<span data-ttu-id="f2f62-111">I client possono utilizzare handle di contesto aperti in qualsiasi modo.</span><span class="sxs-lookup"><span data-stu-id="f2f62-111">Clients may use opened context handles in any way they require.</span></span> <span data-ttu-id="f2f62-112">Devono, tuttavia, invalidare il punto di gestione quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="f2f62-112">They should, however, invalidate the handle when they no longer need it.</span></span> <span data-ttu-id="f2f62-113">Esistono due modi per eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="f2f62-113">There are two way to do this:</span></span>

-   <span data-ttu-id="f2f62-114">Per richiamare una procedura remota offerta dal programma server che libera il contesto e chiude l'handle del contesto (lo imposta su **null**).</span><span class="sxs-lookup"><span data-stu-id="f2f62-114">To invoke a remote procedure offered by the server program that frees the context and closes the context handle (sets it to **NULL**).</span></span>
-   <span data-ttu-id="f2f62-115">Quando il server non è raggiungibile, chiamare la funzione [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="f2f62-115">When the server is unreachable, call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="f2f62-116">Il secondo approccio pulisce solo lo stato lato client e non esegue la pulizia dello stato sul lato server, quindi deve essere utilizzato solo quando si sospetta la partizione di rete e il client e il server eseguiranno una pulizia indipendente.</span><span class="sxs-lookup"><span data-stu-id="f2f62-116">The second approach only cleans up the client side state, and does not clean up the server-side state, so it should be used only when network partition is suspected, and the client and the server will do an independent cleanup.</span></span> <span data-ttu-id="f2f62-117">Il server esegue la pulizia indipendente tramite la routine di esecuzione, il client esegue questa operazione utilizzando la funzione [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="f2f62-117">The server performs independent cleanup through the run-down routine, the client does so using the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="f2f62-118">Il frammento di codice seguente presenta un esempio di come un client può utilizzare un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="f2f62-118">The following code fragment presents an example of how a client might use a context handle.</span></span> <span data-ttu-id="f2f62-119">Per visualizzare la definizione dell'interfaccia utilizzata in questo esempio, vedere [sviluppo di interfacce mediante handle di contesto](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="f2f62-119">To view the definition of the interface that this example uses, see [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span> <span data-ttu-id="f2f62-120">Per l'implementazione del server, vedere [sviluppo di server con handle di contesto](server-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="f2f62-120">For the server implementation, see [Server Development Using Context Handles](server-development-using-context-handles.md).</span></span>

<span data-ttu-id="f2f62-121">In questo esempio, il client chiama RemoteOpen per ottenere un handle di contesto che contiene dati validi.</span><span class="sxs-lookup"><span data-stu-id="f2f62-121">In this example, the client calls RemoteOpen to obtain a context handle that contains valid data.</span></span> <span data-ttu-id="f2f62-122">Il client può quindi utilizzare l'handle di contesto nelle chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="f2f62-122">The client can then use the context handle in remote procedure calls.</span></span> <span data-ttu-id="f2f62-123">Poiché non necessita più dell'handle di associazione, il client può liberare l'handle esplicito utilizzato per creare l'handle del contesto:</span><span class="sxs-lookup"><span data-stu-id="f2f62-123">Because it no longer needs the binding handle, the client can free the explicit handle it used to create the context handle:</span></span>


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



<span data-ttu-id="f2f62-124">Nell'applicazione client di questo esempio viene utilizzata una stored procedure denominata RemoteRead per leggere un file di dati nel server fino a quando non viene rilevata una fine del file.</span><span class="sxs-lookup"><span data-stu-id="f2f62-124">The client application in this example uses a procedure called RemoteRead to read a data file on the server until it encounters an end of file.</span></span> <span data-ttu-id="f2f62-125">Chiude quindi il file chiamando RemoteClose.</span><span class="sxs-lookup"><span data-stu-id="f2f62-125">It then closes the file by calling RemoteClose.</span></span> <span data-ttu-id="f2f62-126">L'handle del contesto viene visualizzato come parametro nelle funzioni RemoteRead e RemoteClose come:</span><span class="sxs-lookup"><span data-stu-id="f2f62-126">The context handle appears as a parameter in the RemoteRead and RemoteClose functions as:</span></span>


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




