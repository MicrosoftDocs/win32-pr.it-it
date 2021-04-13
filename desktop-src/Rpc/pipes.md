---
title: Pipe (RPC)
description: Il costruttore del tipo di pipe è un meccanismo estremamente efficiente per il passaggio di grandi quantità di dati o per una quantità di dati che non è disponibile in memoria per volta.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- RPC (Remote Procedure Call), descrizione, pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474873"
---
# <a name="pipes-rpc"></a><span data-ttu-id="1951f-104">Pipe (RPC)</span><span class="sxs-lookup"><span data-stu-id="1951f-104">Pipes (RPC)</span></span>

<span data-ttu-id="1951f-105">Il costruttore del tipo di pipe è un meccanismo estremamente efficiente per il passaggio di grandi quantità di dati o per una quantità di dati che non è disponibile in memoria per volta.</span><span class="sxs-lookup"><span data-stu-id="1951f-105">The pipe type constructor is a highly efficient mechanism for passing large amounts of data, or any quantity of data that is not all available in memory at one time.</span></span> <span data-ttu-id="1951f-106">Utilizzando una pipe, il tempo di esecuzione RPC gestisce il trasferimento effettivo dei dati, eliminando il sovraccarico associato a chiamate di procedure remote ripetute.</span><span class="sxs-lookup"><span data-stu-id="1951f-106">By using a pipe, RPC run time handles the actual data transfer, eliminating the overhead associated with repeated remote procedure calls.</span></span>

<span data-ttu-id="1951f-107">Quando un client richiama una procedura remota che dispone di un parametro pipe, il client e il server immettono cicli per trasferire i dati.</span><span class="sxs-lookup"><span data-stu-id="1951f-107">After a client invokes a remote procedure that has a pipe parameter, the client and server enter loops to transfer data.</span></span> <span data-ttu-id="1951f-108">I dati possono essere prodotti sul client o sul server.</span><span class="sxs-lookup"><span data-stu-id="1951f-108">The data can be produced on the client or the server.</span></span> <span data-ttu-id="1951f-109">In entrambi i casi, non è necessario che la quantità di dati (in byte) sia nota in anticipo.</span><span class="sxs-lookup"><span data-stu-id="1951f-109">Either way, the amount of data (in bytes) does not have to be known in advance.</span></span> <span data-ttu-id="1951f-110">I dati possono essere prodotti o utilizzati in modo incrementale.</span><span class="sxs-lookup"><span data-stu-id="1951f-110">The data can be produced or consumed incrementally.</span></span> <span data-ttu-id="1951f-111">Nel ciclo di trasferimento dei dati, il server chiama routine stub che caricano o scaricano un buffer di dati.</span><span class="sxs-lookup"><span data-stu-id="1951f-111">While in the data-transfer loop, the server calls stub routines that load or unload a buffer of data.</span></span> <span data-ttu-id="1951f-112">Il client chiama le procedure definite dal programmatore per allocare i buffer, caricare i dati in e scaricare i dati dai buffer.</span><span class="sxs-lookup"><span data-stu-id="1951f-112">The client calls programmer-defined procedures to allocate buffers, load data into and unload data from the buffers.</span></span>

<span data-ttu-id="1951f-113">In questa sezione viene fornita una panoramica dell'utilizzo di pipe per le chiamate di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="1951f-113">This section provides an overview of using pipes for remote procedure calls.</span></span> <span data-ttu-id="1951f-114">Viene presentata la panoramica negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="1951f-114">It presents the overview in the following topics:</span></span>

-   [<span data-ttu-id="1951f-115">Terminologia pipe essenziale</span><span class="sxs-lookup"><span data-stu-id="1951f-115">Essential Pipe Terminology</span></span>](essential-pipe-terminology.md)
-   [<span data-ttu-id="1951f-116">Stato della pipe</span><span class="sxs-lookup"><span data-stu-id="1951f-116">The Pipe State</span></span>](the-pipe-state.md)
-   [<span data-ttu-id="1951f-117">Definizione di pipe nei file IDL</span><span class="sxs-lookup"><span data-stu-id="1951f-117">Defining Pipes in IDL Files</span></span>](defining-pipes-in-idl-files.md)
-   [<span data-ttu-id="1951f-118">Implementazione della pipe lato client</span><span class="sxs-lookup"><span data-stu-id="1951f-118">Client-Side Pipe Implementation</span></span>](client-side-pipe-implementation.md)
-   [<span data-ttu-id="1951f-119">Implementazione della pipe lato server</span><span class="sxs-lookup"><span data-stu-id="1951f-119">Server-Side Pipe Implementation</span></span>](server-side-pipe-implementation.md)
-   [<span data-ttu-id="1951f-120">Regole per più pipe</span><span class="sxs-lookup"><span data-stu-id="1951f-120">Rules for Multiple Pipes</span></span>](rules-for-multiple-pipes.md)
-   [<span data-ttu-id="1951f-121">Combinazione di parametri pipe e nonpipe</span><span class="sxs-lookup"><span data-stu-id="1951f-121">Combining Pipe and Nonpipe Parameters</span></span>](combining-pipe-and-nonpipe-parameters.md)

<span data-ttu-id="1951f-122">Per ulteriori informazioni sulla sintassi e sulle restrizioni della pipe, vedere [pipe](/windows/desktop/Midl/pipe) in riferimenti al linguaggio MIDL.</span><span class="sxs-lookup"><span data-stu-id="1951f-122">For more information on pipe syntax and restrictions, see [pipe](/windows/desktop/Midl/pipe) in the MIDL Language Reference.</span></span> <span data-ttu-id="1951f-123">Il programma PIPEs Sample (SDK) di esempio Platform Software Development Kit (SDK) \\ Mostra come usare **\[ in, out \]** Pipes per trasferire i dati tra un client e un server.</span><span class="sxs-lookup"><span data-stu-id="1951f-123">The PIPES sample program in the Platform Software Development Kit (SDK) samples\\rpc directory demonstrates how to use **\[in,out\]** pipes to transfer data between a client and a server.</span></span>

 

 
