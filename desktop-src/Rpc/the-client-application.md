---
title: Applicazione client
description: Visualizzare la parte dell'applicazione client di un esempio RPC (Remote Procedure Call). L'esempio seguente deriva dall'applicazione "Hello World" in Platform SDK.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e0b798543cd70e61f3ff1161503fa64710e53e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405014"
---
# <a name="the-client-application"></a><span data-ttu-id="44163-104">Applicazione client</span><span class="sxs-lookup"><span data-stu-id="44163-104">The Client Application</span></span>

<span data-ttu-id="44163-105">L'esempio seguente deriva dall'applicazione "Hello World" nella directory RPC \\ Hello di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="44163-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="44163-106">Il file di origine Helloc.c contiene una direttiva per includere il file di intestazione generato da MIDL, Hello.h.</span><span class="sxs-lookup"><span data-stu-id="44163-106">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="44163-107">All'interno di Hello.h sono presenti direttive per includere Rpc.h e rpcndr.h, che contengono le definizioni per le routine di run-time RPC, **HelloProc** e **Shutdown** e i tipi di dati utilizzati dalle applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="44163-107">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="44163-108">Il compilatore MIDL deve essere usato con l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="44163-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="44163-109">Poiché il client gestisce la connessione al server, l'applicazione client chiama le funzioni di run-time per stabilire un handle per il server e rilasciare questo handle al termine delle chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="44163-109">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="44163-110">La funzione [**RpcStringBindingCompose combina**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) i componenti dell'handle di associazione in una rappresentazione di stringa di tale handle e alloca memoria per l'associazione di stringhe.</span><span class="sxs-lookup"><span data-stu-id="44163-110">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="44163-111">La funzione [**RpcBindingFromStringBinding crea**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) un handle di associazione server, **hello \_ ClientIfHandle,** per l'applicazione client da tale rappresentazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="44163-111">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="44163-112">Nella chiamata a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)i parametri non specificano l'UUID perché questa esercitazione presuppone che sia presente una sola implementazione dell'interfaccia "hello".</span><span class="sxs-lookup"><span data-stu-id="44163-112">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="44163-113">Inoltre, la chiamata non specifica un indirizzo di rete perché l'applicazione userà l'impostazione predefinita, ovvero il computer host locale.</span><span class="sxs-lookup"><span data-stu-id="44163-113">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="44163-114">La sequenza di protocollo è una stringa di caratteri che rappresenta il trasporto di rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="44163-114">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="44163-115">L'endpoint è un nome specifico della sequenza di protocollo.</span><span class="sxs-lookup"><span data-stu-id="44163-115">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="44163-116">In questo esempio vengono utilizzate named pipe per il trasporto di rete, quindi la sequenza del protocollo è "ncacn \_ np".</span><span class="sxs-lookup"><span data-stu-id="44163-116">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="44163-117">Il nome dell'endpoint è \\ \\ "pipe hello".</span><span class="sxs-lookup"><span data-stu-id="44163-117">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="44163-118">Le chiamate di procedura remota effettive, **HelloProc** e **Shutdown,** vengono eseguite all'interno del gestore di eccezioni RPC, un set di macro che consentono di controllare le eccezioni che si verificano all'esterno del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44163-118">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="44163-119">Se il modulo di run-time RPC segnala un'eccezione, il controllo passa al [**blocco RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)</span><span class="sxs-lookup"><span data-stu-id="44163-119">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="44163-120">Qui è possibile inserire il codice per eseguire la pulizia necessaria e quindi uscire normalmente.</span><span class="sxs-lookup"><span data-stu-id="44163-120">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="44163-121">Questo programma di esempio informa semplicemente l'utente che si è verificata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="44163-121">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="44163-122">Se non si desidera utilizzare le eccezioni, è possibile utilizzare gli attributi ACF [stato comm \_ ](/windows/desktop/Midl/comm-status) e lo stato [di \_ errore](/windows/desktop/Midl/fault-status) per segnalare gli errori.</span><span class="sxs-lookup"><span data-stu-id="44163-122">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="44163-123">Al termine delle chiamate di procedura remota, il client chiama [**innanzitutto RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per liberare la memoria allocata per l'associazione di stringhe.</span><span class="sxs-lookup"><span data-stu-id="44163-123">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="44163-124">Si noti che dopo aver creato l'handle di associazione, un programma client può liberare un'associazione di stringhe in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="44163-124">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="44163-125">Il client chiama quindi [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) per rilasciare l'handle.</span><span class="sxs-lookup"><span data-stu-id="44163-125">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
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



 

 