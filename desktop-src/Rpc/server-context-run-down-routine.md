---
title: Routine di esecuzione del contesto del server
description: Se la comunicazione si interrompe mentre il server mantiene il contesto per conto del client, potrebbe essere necessaria una routine di pulitura per pulire lo stato gestito dal server per conto di un determinato client.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045159"
---
# <a name="server-context-run-down-routine"></a><span data-ttu-id="4ab1e-103">Routine di esecuzione del contesto del server</span><span class="sxs-lookup"><span data-stu-id="4ab1e-103">Server Context Run-down Routine</span></span>

<span data-ttu-id="4ab1e-104">Se la comunicazione si interrompe mentre il server mantiene il contesto per conto del client, potrebbe essere necessaria una routine di pulitura per pulire lo stato gestito dal server per conto di un determinato client.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-104">If communication breaks down while the server is maintaining context on behalf of the client, a cleanup routine may be needed to clean up the state maintained by the server on behalf of a given client.</span></span> <span data-ttu-id="4ab1e-105">Questa routine di pulizia è detta *routine di esecuzione del contesto*.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-105">This cleanup routine is called a *context run-down routine*.</span></span> <span data-ttu-id="4ab1e-106">Quando una connessione viene interrotta, lo stub del server e la libreria di runtime chiamerà questa routine a ogni handle di contesto aperto dal client.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-106">When a connection breaks, the server stub and the run-time library will call this routine on every context handle opened by the client.</span></span>

<span data-ttu-id="4ab1e-107">La routine di esecuzione del contesto è obbligatoria ed è dichiarata in modo implicito e viene denominata quando si applica l'attributo dell' \[ **\_ handle di contesto** \] a una definizione di tipo.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-107">The context run-down routine is required, and is implicitly declared and named, when you apply the \[**context\_handle**\] attribute to a type definition.</span></span> <span data-ttu-id="4ab1e-108">Il server non chiamerà la routine di esecuzione del contesto se l'attributo dell' \[ **\_ handle di contesto** \] è stato applicato direttamente a un parametro.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-108">The server will not call the context run-down routine if the \[**context\_handle**\] attribute was applied directly to a parameter.</span></span>

<span data-ttu-id="4ab1e-109">La sintassi di routine di esecuzione del contesto è:</span><span class="sxs-lookup"><span data-stu-id="4ab1e-109">The context run-down routine syntax is:</span></span>

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

<span data-ttu-id="4ab1e-110">Si noti che il nome del tipo determina il nome della routine di esecuzione del contesto.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-110">Note that the type name determines the name of the context run-down routine.</span></span>

<span data-ttu-id="4ab1e-111">Il frammento di codice che segue presenta una routine di esecuzione del contesto di esempio.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-111">The code fragment that follows presents a sample context run-down routine.</span></span> <span data-ttu-id="4ab1e-112">che chiama la stored procedure RemoteClose usata nell'esempio nello [sviluppo di interfacce usando handle di contesto](interface-development-using-context-handles.md), [lo sviluppo di server con handle di contesto](server-development-using-context-handles.md)e [lo sviluppo di client con handle di contesto](client-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="4ab1e-112">that calls the RemoteClose procedure used in the example in [Interface Development Using Context Handles](interface-development-using-context-handles.md), [Server Development Using Context Handles](server-development-using-context-handles.md), and [Client Development Using Context Handles](client-development-using-context-handles.md).</span></span> <span data-ttu-id="4ab1e-113">Questa procedura chiude l'handle di file, libera la memoria associata al file e assegna **null** all'handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-113">This procedure closes the file handle, frees the memory associated with the file, and assigns **NULL** to the context handle.</span></span> <span data-ttu-id="4ab1e-114">L'assegnazione di **valori null** è il risultato della chiamata alla funzione RemoteClose e non è necessario in uno scenario di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-114">Assigning **NULL** is a result of calling the RemoteClose function, and is not necessary in a run-down scenario.</span></span> <span data-ttu-id="4ab1e-115">Il tempo di esecuzione RPC pulisce lo stato indipendentemente dal fatto che l'handle di contesto sia impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-115">The RPC run time cleans up its state regardless of whether the context handle is set to **NULL**.</span></span>

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




