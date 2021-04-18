---
title: Esempi (RPC)
description: Esempi che illustrano i concetti di RPC (Remote Procedure Call).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC remote procedure call, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300730"
---
# <a name="examples-rpc"></a><span data-ttu-id="9674f-104">Esempi (RPC)</span><span class="sxs-lookup"><span data-stu-id="9674f-104">Examples (RPC)</span></span>

<span data-ttu-id="9674f-105">Il Software Development Kit (SDK) della piattaforma include esempi che illustrano una varietà di concetti di Remote Procedure Call (RPC), come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9674f-105">The Platform Software Development Kit (SDK) includes examples that demonstrate a variety of Remote Procedure Call (RPC) concepts, as follows:</span></span>

-   <span data-ttu-id="9674f-106">ASYNCRPC illustra la struttura di un'applicazione RPC che utilizza chiamate asincrone a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="9674f-106">ASYNCRPC illustrates the structure of an RPC application that uses asynchronous remote procedure calls.</span></span> <span data-ttu-id="9674f-107">Vengono inoltre illustrati i vari metodi di notifica del completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="9674f-107">It also demonstrates various methods of notification of the call's completion.</span></span>
-   <span data-ttu-id="9674f-108">CLUUID illustra l'uso dell'UUID dell'oggetto client per consentire a un client di effettuare la selezione da più implementazioni di una procedura remota.</span><span class="sxs-lookup"><span data-stu-id="9674f-108">CLUUID demonstrates use of the client-object UUID to enable a client to select from multiple implementations of a remote procedure.</span></span>
-   <span data-ttu-id="9674f-109">La directory dei dati contiene quattro programmi: DUNION illustra le unioni discriminate (non incapsulate); Inout illustra [ \[ in \] ](../midl/in.md), parametri [ \[ out \] ](../midl/out-idl.md) ; REPAS dimostra [che rappresenta \_ come](/windows/desktop/Midl/represent-as) attributo. XMIT illustra l'attributo [trasmissione \_ As](/windows/desktop/Midl/transmit-as) .</span><span class="sxs-lookup"><span data-stu-id="9674f-109">DATA directory contains four programs: DUNION illustrates discriminated (nonencapsulated) unions; INOUT demonstrates [\[in\]](../midl/in.md), [\[out\]](../midl/out-idl.md) parameters; REPAS demonstrates the [represent\_as](/windows/desktop/Midl/represent-as) attribute; XMIT demonstrates the [transmit\_as](/windows/desktop/Midl/transmit-as) attribute.</span></span>
-   <span data-ttu-id="9674f-110">DYNEPT illustra un'applicazione client che gestisce la connessione al server tramite endpoint dinamici.</span><span class="sxs-lookup"><span data-stu-id="9674f-110">DYNEPT demonstrates a client application managing its connection to the server through dynamic endpoints.</span></span>
-   <span data-ttu-id="9674f-111">La directory FILEREP contiene quattro esempi che illustrano come gli sviluppatori possono scrivere un semplice servizio Replica file, un servizio Replica file multiutente, un servizio che supporta le funzionalità di sicurezza e un servizio che utilizza pipe asincrone RPC.</span><span class="sxs-lookup"><span data-stu-id="9674f-111">FILEREP directory contains four samples illustrating how developers can write a simple file replication service, a multi-user file replication service, a service supporting security features, and a service using RPC asynchronous pipes.</span></span>
-   <span data-ttu-id="9674f-112">GESTISCE la directory contiene tre programmi, AUTO, CXHNDL, USRDEF, che illustrano rispettivamente handle [automatico \_ ](/windows/desktop/Midl/auto-handle), \[ handle di contesto \_ \] e handle generici (definiti dall'utente).</span><span class="sxs-lookup"><span data-stu-id="9674f-112">HANDLES directory contains three programs, AUTO, CXHNDL, USRDEF, which demonstrate [auto\_handle](/windows/desktop/Midl/auto-handle), \[context\_handle\], and generic (user-defined) handles, respectively.</span></span>
-   <span data-ttu-id="9674f-113">HELLo è un'implementazione client/server di "Hello, World".</span><span class="sxs-lookup"><span data-stu-id="9674f-113">HELLO is a client/server implementation of "Hello, world."</span></span>
-   <span data-ttu-id="9674f-114">La directory Pickle contiene due programmi: PICKLP illustra la serializzazione delle procedure dati; La serializzazione del tipo di dati viene illustrata in pickle entrambi i programmi utilizzano gli attributi [ \[ Encode \] ](../midl/encode.md) e [ \[ Decode \] ](../midl/decode.md) .</span><span class="sxs-lookup"><span data-stu-id="9674f-114">PICKLE directory contains two programs: PICKLP demonstrates data procedure serialization; PICKLT demonstrates data type serialization; both programs use the [\[encode\]](../midl/encode.md) and [\[decode\]](../midl/decode.md) attributes.</span></span>
-   <span data-ttu-id="9674f-115">PIPEs illustra l'uso del costruttore di tipo pipe.</span><span class="sxs-lookup"><span data-stu-id="9674f-115">PIPES demonstrates the use of the pipe-type constructor.</span></span>
-   <span data-ttu-id="9674f-116">RPCSVC illustra l'implementazione di un servizio con RPC.</span><span class="sxs-lookup"><span data-stu-id="9674f-116">RPCSVC demonstrates the implementation of a service with RPC.</span></span>
-   <span data-ttu-id="9674f-117">STROUT illustra come allocare memoria in un server per un oggetto bidimensionale, ovvero una matrice di puntatori, e come passarlo di nuovo al client come \[ \] parametro out-only.</span><span class="sxs-lookup"><span data-stu-id="9674f-117">STROUT demonstrates how to allocate memory at a server for a two-dimensional object (an array of pointers) and pass it back to the client as an \[out\]-only parameter.</span></span> <span data-ttu-id="9674f-118">Il client libera quindi la memoria.</span><span class="sxs-lookup"><span data-stu-id="9674f-118">The client then frees the memory.</span></span> <span data-ttu-id="9674f-119">Questa tecnica consente allo stub di chiamare il server senza conoscere in anticipo la quantità di dati che verranno restituiti.</span><span class="sxs-lookup"><span data-stu-id="9674f-119">This technique allows the stub to call the server without knowing in advance how much data will be returned.</span></span>

    <span data-ttu-id="9674f-120">Questo programma consente inoltre all'utente di compilare per UNICODE o ANSI.</span><span class="sxs-lookup"><span data-stu-id="9674f-120">This program also allows the user to compile either for UNICODE or ANSI.</span></span>

<span data-ttu-id="9674f-121">Tutti i file di origine e i makefile per questi programmi si trovano in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="9674f-121">All of the source files and makefiles for these programs are located in the Platform SDK.</span></span>

<span data-ttu-id="9674f-122">Per lo sviluppo di applicazioni RPC di base e per esempi più semplici, vedere gli argomenti dell' [esercitazione](tutorial.md) .</span><span class="sxs-lookup"><span data-stu-id="9674f-122">For basic RPC application development and simpler examples, please see the [Tutorial](tutorial.md) topics.</span></span>

 

 
