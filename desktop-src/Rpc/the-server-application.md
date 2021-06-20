---
title: Applicazione server
description: Visualizzare la parte dell'applicazione server di un esempio RPC (Remote Procedure Call). L'esempio deriva dall'applicazione "Hello World" in Platform SDK.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406064"
---
# <a name="the-server-application"></a><span data-ttu-id="335bd-104">Applicazione server</span><span class="sxs-lookup"><span data-stu-id="335bd-104">The Server Application</span></span>

<span data-ttu-id="335bd-105">L'esempio seguente deriva dall'applicazione "Hello World" nella directory RPC \\ Hello di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="335bd-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="335bd-106">Il lato server dell'applicazione distribuita informa il sistema che i relativi servizi sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="335bd-106">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="335bd-107">Attende quindi le richieste del client.</span><span class="sxs-lookup"><span data-stu-id="335bd-107">It then waits for client requests.</span></span> <span data-ttu-id="335bd-108">Il compilatore MIDL deve essere usato con l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="335bd-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="335bd-109">A seconda delle dimensioni dell'applicazione e delle preferenze di scrittura del codice, è possibile scegliere di implementare procedure remote in uno o più file separati.</span><span class="sxs-lookup"><span data-stu-id="335bd-109">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="335bd-110">In questo programma di esercitazione il file di origine Hellos.c contiene la routine del server principale.</span><span class="sxs-lookup"><span data-stu-id="335bd-110">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="335bd-111">Il file Hellop.c contiene la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="335bd-111">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="335bd-112">Il vantaggio di organizzare le procedure remote in file separati è che le procedure possono essere collegate a un programma autonomo per eseguire il debug del codice prima della conversione in un'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="335bd-112">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="335bd-113">Quando le procedure funzionano nel programma autonomo, è possibile compilare e collegare i file di origine contenenti le procedure remote all'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="335bd-113">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="335bd-114">Come per il file di origine dell'applicazione client, il file di origine dell'applicazione server deve includere il file di intestazione Hello.h.</span><span class="sxs-lookup"><span data-stu-id="335bd-114">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="335bd-115">Il server chiama le funzioni di run-time RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) per rendere disponibili al client le informazioni di associazione.</span><span class="sxs-lookup"><span data-stu-id="335bd-115">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="335bd-116">Questo programma di esempio passa il nome dell'handle di interfaccia **a RpcServerRegisterIf.**</span><span class="sxs-lookup"><span data-stu-id="335bd-116">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="335bd-117">Gli altri parametri sono impostati su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="335bd-117">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="335bd-118">Il server chiama quindi la [**funzione RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) per indicare che è in attesa di richieste client.</span><span class="sxs-lookup"><span data-stu-id="335bd-118">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="335bd-119">L'applicazione server deve includere anche le due funzioni di gestione della memoria chiamate dal server stub: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) e [**midl \_ user \_ free.**](the-midl-user-free-function.md)</span><span class="sxs-lookup"><span data-stu-id="335bd-119">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="335bd-120">Queste funzioni allocano e liberano memoria nel server quando una procedura remota passa parametri al server.</span><span class="sxs-lookup"><span data-stu-id="335bd-120">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="335bd-121">In questo programma di esempio **midl \_ user \_ allocate** e **midl \_ user \_ free** sono semplicemente wrapper per le funzioni della libreria C [**malloc**](pointers-and-memory-allocation.md) e **free.**</span><span class="sxs-lookup"><span data-stu-id="335bd-121">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="335bd-122">Si noti che, nelle dichiarazioni con inoltro generate dal compilatore MIDL, "MIDL" è in maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="335bd-122">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="335bd-123">Il file di intestazione Rpcndr.h definisce midl user free e midl user allocate rispettivamente come MIDL user free e \_ \_ \_ \_ \_ \_ MIDL \_ user \_ allocate.</span><span class="sxs-lookup"><span data-stu-id="335bd-123">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




