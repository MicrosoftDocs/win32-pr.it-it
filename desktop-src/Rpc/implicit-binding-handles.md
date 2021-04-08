---
title: Handle di binding impliciti
description: Gli handle di binding impliciti consentono all'applicazione di selezionare un server specifico per eseguire le chiamate di procedura remota.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046854"
---
# <a name="implicit-binding-handles"></a><span data-ttu-id="3efc3-103">Handle di binding impliciti</span><span class="sxs-lookup"><span data-stu-id="3efc3-103">Implicit Binding Handles</span></span>

<span data-ttu-id="3efc3-104">Gli handle di binding impliciti consentono all'applicazione di selezionare un server specifico per eseguire le chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="3efc3-104">Implicit binding handles allow your application to select a specific server to execute its remote procedure calls.</span></span> <span data-ttu-id="3efc3-105">Per informazioni dettagliate, vedere [Binding lato client](client-side-binding.md).</span><span class="sxs-lookup"><span data-stu-id="3efc3-105">For details, see [Client-Side Binding](client-side-binding.md).</span></span> <span data-ttu-id="3efc3-106">Consentono inoltre al programma client/server di utilizzare binding autenticati.</span><span class="sxs-lookup"><span data-stu-id="3efc3-106">They also enable your client/server program to use authenticated bindings.</span></span> <span data-ttu-id="3efc3-107">Ovvero il client può specificare le informazioni di autenticazione in un handle di binding implicito.</span><span class="sxs-lookup"><span data-stu-id="3efc3-107">That is, the client can specify authentication information in an implicit binding handle.</span></span> <span data-ttu-id="3efc3-108">La libreria di runtime RPC utilizza le informazioni di autenticazione per stabilire una sessione RPC autenticata tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="3efc3-108">The RPC run-time library uses the authentication information to establish an authenticated RPC session between the client and the server.</span></span> <span data-ttu-id="3efc3-109">Per altre informazioni, vedere [Sicurezza](security.md).</span><span class="sxs-lookup"><span data-stu-id="3efc3-109">For more information, see [Security](security.md).</span></span>

> [!Note]  
> <span data-ttu-id="3efc3-110">Gli handle di binding impliciti non sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="3efc3-110">Implicit binding handles are not thread safe.</span></span> <span data-ttu-id="3efc3-111">Le applicazioni multithread devono pertanto evitare di utilizzare handle di binding impliciti.</span><span class="sxs-lookup"><span data-stu-id="3efc3-111">Multi-threaded applications therefore should avoid using implicit binding handles.</span></span>

 

<span data-ttu-id="3efc3-112">Quando nell'applicazione vengono utilizzate associazioni implicite, il client deve impostare le informazioni di binding in modo che sia possibile creare l'associazione.</span><span class="sxs-lookup"><span data-stu-id="3efc3-112">When your application uses implicit bindings, the client must set the binding information so that it can create the binding.</span></span> <span data-ttu-id="3efc3-113">Dopo che il client ha creato un'associazione implicita, non è necessario passare gli handle di associazione alle procedure remote.</span><span class="sxs-lookup"><span data-stu-id="3efc3-113">After the client creates an implicit binding, it does not need to pass any binding handles to remote procedures.</span></span> <span data-ttu-id="3efc3-114">La libreria RPC gestisce il resto dei meccanismi della sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="3efc3-114">The RPC library handles the rest of the mechanics of the communication session.</span></span>

<span data-ttu-id="3efc3-115">Il client archivia le informazioni di binding per un handle implicito in una variabile globale.</span><span class="sxs-lookup"><span data-stu-id="3efc3-115">The client stores the binding information for an implicit handle in a global variable.</span></span> <span data-ttu-id="3efc3-116">Quando il compilatore MIDL genera lo stub e il file di intestazione del client dalla specifica dell'interfaccia nel file MIDL, genera anche il codice per una variabile di handle di binding globale.</span><span class="sxs-lookup"><span data-stu-id="3efc3-116">When the MIDL compiler generates the client stub and header file from the interface specification in your MIDL file, it also generates code for a global binding handle variable.</span></span> <span data-ttu-id="3efc3-117">Il programma client Inizializza l'handle e quindi non vi fa riferimento finché non elimina l'associazione.</span><span class="sxs-lookup"><span data-stu-id="3efc3-117">Your client program initializes the handle and then does not refer to it again until it destroys the binding.</span></span>

<span data-ttu-id="3efc3-118">Per creare un handle implicito, è necessario specificare l' \[ attributo [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) \] in ACF per un'interfaccia, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="3efc3-118">You create an implicit handle by specifying the \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] attribute in the ACF for an interface as follows:</span></span>

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

<span data-ttu-id="3efc3-119">Il tipo di **handle \_ t** , usato nell'esempio precedente, è un tipo di dati MIDL usato per la definizione degli handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="3efc3-119">The **handle\_t** type, which is used in the preceding example, is a MIDL data type used for defining binding handles.</span></span>

<span data-ttu-id="3efc3-120">Dopo aver creato l'handle implicito, l'applicazione deve utilizzarla come parametro per le funzioni della libreria di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="3efc3-120">After creating the implicit handle, the application needs to use it as a parameter to the RPC run-time library functions.</span></span> <span data-ttu-id="3efc3-121">Non usare l'handle implicito come parametro per le chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="3efc3-121">Do not use the implicit handle as a parameter to remote procedure calls.</span></span> <span data-ttu-id="3efc3-122">Nell'esempio di codice riportato di seguito viene illustrato l'utilizzo degli handle di associazione impliciti.</span><span class="sxs-lookup"><span data-stu-id="3efc3-122">The following code sample demonstrates the use of implicit binding handles.</span></span>

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

<span data-ttu-id="3efc3-123">Nell'esempio precedente, le funzioni della libreria run-time RPC [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) e [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) richiedono entrambi l'handle di binding implicito da passare nei rispettivi elenchi di parametri.</span><span class="sxs-lookup"><span data-stu-id="3efc3-123">In the preceding example, the RPC run-time library functions [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) and [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) both required the implicit binding handle to be passed in their parameter lists.</span></span> <span data-ttu-id="3efc3-124">Tuttavia, la procedura remota MyRemoteProcedure non è stata eseguita perché non è una funzione della libreria di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="3efc3-124">However, the remote procedure MyRemoteProcedure did not, since it is not an RPC run-time library function.</span></span>

 

 