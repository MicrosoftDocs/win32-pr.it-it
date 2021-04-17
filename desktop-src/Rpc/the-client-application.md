---
title: Applicazione client
description: L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK).
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474038"
---
# <a name="the-client-application"></a><span data-ttu-id="0b08f-103">Applicazione client</span><span class="sxs-lookup"><span data-stu-id="0b08f-103">The Client Application</span></span>

<span data-ttu-id="0b08f-104">L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0b08f-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="0b08f-105">Il file di origine Helloc. c contiene una direttiva per includere il file di intestazione generato da MIDL, Hello. h.</span><span class="sxs-lookup"><span data-stu-id="0b08f-105">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="0b08f-106">All'interno di Hello. h sono presenti direttive che includono RPC. h e Rpcndr. h, che contengono le definizioni per le routine della fase di esecuzione RPC, **HelloProc** e **Shutdown** e i tipi di dati utilizzati dalle applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="0b08f-106">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="0b08f-107">Il compilatore MIDL deve essere usato con l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="0b08f-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="0b08f-108">Poiché il client gestisce la connessione al server, l'applicazione client chiama le funzioni di runtime per stabilire un handle per il server e per rilasciare questo handle dopo il completamento delle chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="0b08f-108">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="0b08f-109">La funzione [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combina i componenti dell'handle di associazione in una rappresentazione di stringa di tale handle e alloca memoria per l'associazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="0b08f-109">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="0b08f-110">La funzione [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) crea un handle di associazione server, **Hello \_ ClientIfHandle**, per l'applicazione client da tale rappresentazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="0b08f-110">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="0b08f-111">Nella chiamata a [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), i parametri non specificano l'UUID perché in questa esercitazione si presuppone che esista una sola implementazione dell'interfaccia "Hello".</span><span class="sxs-lookup"><span data-stu-id="0b08f-111">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="0b08f-112">Inoltre, la chiamata non specifica un indirizzo di rete perché l'applicazione utilizzerà il valore predefinito, ovvero il computer host locale.</span><span class="sxs-lookup"><span data-stu-id="0b08f-112">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="0b08f-113">La sequenza di protocollo è una stringa di caratteri che rappresenta il trasporto di rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="0b08f-113">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="0b08f-114">L'endpoint è un nome specifico della sequenza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="0b08f-114">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="0b08f-115">Questo esempio USA named pipe per il trasporto di rete, quindi la sequenza di protocollo è "ncacn \_ NP".</span><span class="sxs-lookup"><span data-stu-id="0b08f-115">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="0b08f-116">Il nome dell'endpoint è " \\ pipe \\ Hello".</span><span class="sxs-lookup"><span data-stu-id="0b08f-116">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="0b08f-117">Le chiamate a procedure remote effettive, **HelloProc** e **Shutdown**, avvengono all'interno del gestore di eccezioni RPC, ovvero un set di macro che consentono di controllare le eccezioni che si verificano all'esterno del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b08f-117">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="0b08f-118">Se il modulo della fase di esecuzione RPC segnala un'eccezione, il controllo passa al blocco [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) .</span><span class="sxs-lookup"><span data-stu-id="0b08f-118">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="0b08f-119">Qui è possibile inserire il codice per eseguire tutte le operazioni di pulizia necessarie, quindi uscire normalmente.</span><span class="sxs-lookup"><span data-stu-id="0b08f-119">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="0b08f-120">Questo programma di esempio informa semplicemente l'utente che si è verificata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="0b08f-120">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="0b08f-121">Se non si desidera utilizzare le eccezioni, è possibile utilizzare lo [ \_ stato di comunicazione](/windows/desktop/Midl/comm-status) degli attributi ACF [e \_ lo stato di errore](/windows/desktop/Midl/fault-status) per segnalare gli errori.</span><span class="sxs-lookup"><span data-stu-id="0b08f-121">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="0b08f-122">Una volta completate le chiamate di procedura remota, il client chiama prima [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per liberare la memoria allocata per l'associazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="0b08f-122">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="0b08f-123">Si noti che dopo aver creato l'handle di binding, un programma client può liberare un'associazione di stringa in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="0b08f-123">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="0b08f-124">Il client chiama quindi [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) per rilasciare l'handle.</span><span class="sxs-lookup"><span data-stu-id="0b08f-124">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


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



 

 