---
title: Applicazione server
description: L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK).
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856197"
---
# <a name="the-server-application"></a><span data-ttu-id="9524f-103">Applicazione server</span><span class="sxs-lookup"><span data-stu-id="9524f-103">The Server Application</span></span>

<span data-ttu-id="9524f-104">L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9524f-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="9524f-105">Il lato server dell'applicazione distribuita informa il sistema che i servizi sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="9524f-105">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="9524f-106">Attende quindi le richieste del client.</span><span class="sxs-lookup"><span data-stu-id="9524f-106">It then waits for client requests.</span></span> <span data-ttu-id="9524f-107">Il compilatore MIDL deve essere usato con l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="9524f-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="9524f-108">A seconda delle dimensioni dell'applicazione e delle preferenze di codifica, è possibile scegliere di implementare procedure remote in uno o più file distinti.</span><span class="sxs-lookup"><span data-stu-id="9524f-108">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="9524f-109">In questo programma di esercitazione, il file di origine Hells. c contiene la routine del server principale.</span><span class="sxs-lookup"><span data-stu-id="9524f-109">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="9524f-110">Il file ciau. c contiene la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="9524f-110">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="9524f-111">Il vantaggio di organizzare le procedure remote in file distinti è che le procedure possono essere collegate a un programma autonomo per eseguire il debug del codice prima che venga convertito in un'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="9524f-111">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="9524f-112">Una volta che le procedure funzionano nel programma autonomo, è possibile compilare e collegare i file di origine contenenti le procedure remote con l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="9524f-112">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="9524f-113">Come per il file di origine dell'applicazione client, il file di origine dell'applicazione server deve includere il file di intestazione Hello. h.</span><span class="sxs-lookup"><span data-stu-id="9524f-113">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="9524f-114">Il server chiama le funzioni di runtime RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) per rendere disponibili al client le informazioni di binding.</span><span class="sxs-lookup"><span data-stu-id="9524f-114">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="9524f-115">Questo programma di esempio passa il nome dell'handle dell'interfaccia a **RpcServerRegisterIf**.</span><span class="sxs-lookup"><span data-stu-id="9524f-115">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="9524f-116">Gli altri parametri sono impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="9524f-116">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="9524f-117">Il server chiama quindi la funzione [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) per indicare che è in attesa di richieste client.</span><span class="sxs-lookup"><span data-stu-id="9524f-117">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="9524f-118">L'applicazione server deve includere anche le due funzioni di gestione della memoria chiamate dallo stub del server: [**MIDL \_ User \_ allocate**](the-midl-user-allocate-function.md) e [**MIDL \_ User \_ Free**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="9524f-118">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="9524f-119">Queste funzioni allocano e liberano memoria sul server quando una procedura remota passa parametri al server.</span><span class="sxs-lookup"><span data-stu-id="9524f-119">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="9524f-120">In questo programma di esempio **, MIDL \_ User \_ allocate** e **MIDL \_ User \_ Free** sono semplicemente wrapper per le funzioni C-Library [**malloc**](pointers-and-memory-allocation.md) e **Free**.</span><span class="sxs-lookup"><span data-stu-id="9524f-120">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="9524f-121">Si noti che nelle dichiarazioni con estensione generate dal compilatore MIDL, "MIDL" è maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="9524f-121">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="9524f-122">Il file di intestazione Rpcndr. h definisce l'utente MIDL \_ \_ Free e MIDL \_ User \_ ALLOCAte per essere MIDL user \_ \_ Free e MIDL user \_ \_ allocate, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="9524f-122">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


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



 

 




