---
title: Accesso alle interfacce tra gli Apartment
description: Accesso alle interfacce tra gli Apartment
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709259"
---
# <a name="accessing-interfaces-across-apartments"></a><span data-ttu-id="d5838-103">Accesso alle interfacce tra gli Apartment</span><span class="sxs-lookup"><span data-stu-id="d5838-103">Accessing Interfaces Across Apartments</span></span>

<span data-ttu-id="d5838-104">COM consente a qualsiasi Apartment di un processo di ottenere l'accesso a un'interfaccia implementata in un oggetto in qualsiasi altro Apartment nel processo.</span><span class="sxs-lookup"><span data-stu-id="d5838-104">COM provides a way for any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.</span></span> <span data-ttu-id="d5838-105">Questa operazione viene eseguita tramite l'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="d5838-105">This is done through the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="d5838-106">Questa interfaccia dispone di tre metodi, che consentono di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5838-106">This interface has three methods, which allow you to do the following:</span></span>

-   <span data-ttu-id="d5838-107">Registrare un'interfaccia come interfaccia *globale* (processwide).</span><span class="sxs-lookup"><span data-stu-id="d5838-107">Register an interface as a *global* (processwide) interface.</span></span>
-   <span data-ttu-id="d5838-108">Ottiene un puntatore a tale interfaccia da qualsiasi altro Apartment tramite un cookie.</span><span class="sxs-lookup"><span data-stu-id="d5838-108">Get a pointer to that interface from any other apartment through a cookie.</span></span>
-   <span data-ttu-id="d5838-109">Revocare la registrazione globale di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d5838-109">Revoke the global registration of an interface.</span></span>

<span data-ttu-id="d5838-110">L'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) rappresenta un modo efficiente per un processo di archiviazione di un puntatore a interfaccia in una posizione di memoria a cui è possibile accedere da più Apartment all'interno del processo, ad esempio variabili a livello di processo e oggetti *agile* (oggetti a thread libero, con marshalling) che contengono puntatori di interfaccia ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="d5838-110">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as process-wide variables and *agile* objects (free-threaded, marshaled objects) containing interface pointers to other objects.</span></span>

<span data-ttu-id="d5838-111">Un oggetto agile non è a conoscenza dell'infrastruttura COM sottostante in cui viene eseguito. in altre parole, l'Apartment, il contesto e il thread in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d5838-111">An agile object is unaware of the underlying COM infrastructure in which it runs; in other words, what apartment, context, and thread it is executing on.</span></span> <span data-ttu-id="d5838-112">È possibile che l'oggetto sia in attesa di interfacce specifiche per un apartment o un contesto.</span><span class="sxs-lookup"><span data-stu-id="d5838-112">The object may be holding on to interfaces that are specific to an apartment or context.</span></span> <span data-ttu-id="d5838-113">Per questo motivo, la chiamata di queste interfacce da qualsiasi posizione in cui è in esecuzione il componente agile potrebbe non funzionare sempre correttamente.</span><span class="sxs-lookup"><span data-stu-id="d5838-113">For this reason, calling these interfaces from wherever the agile component is executing might not always work properly.</span></span> <span data-ttu-id="d5838-114">La tabella dell'interfaccia globale evita questo problema garantendo che venga usato un proxy valido (o un puntatore diretto) all'oggetto, in base alla posizione in cui è in esecuzione l'oggetto agile.</span><span class="sxs-lookup"><span data-stu-id="d5838-114">The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.</span></span>

> [!Note]  
> <span data-ttu-id="d5838-115">La tabella dell'interfaccia globale non è portabile tra i limiti del processo o del computer, quindi non può essere usata al posto del normale meccanismo di passaggio dei parametri.</span><span class="sxs-lookup"><span data-stu-id="d5838-115">The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.</span></span>

 

<span data-ttu-id="d5838-116">Per informazioni sulla creazione e sull'utilizzo di una tabella di interfaccia globale, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5838-116">For information about creating and using a global interface table, see the following topics:</span></span>

-   [<span data-ttu-id="d5838-117">Creazione della tabella dell'interfaccia globale</span><span class="sxs-lookup"><span data-stu-id="d5838-117">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
-   [<span data-ttu-id="d5838-118">Quando usare la tabella dell'interfaccia globale</span><span class="sxs-lookup"><span data-stu-id="d5838-118">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a><span data-ttu-id="d5838-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5838-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5838-120">Scelta del modello di threading</span><span class="sxs-lookup"><span data-stu-id="d5838-120">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="d5838-121">Apartment con multithreading</span><span class="sxs-lookup"><span data-stu-id="d5838-121">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="d5838-122">Problemi di threading del server in-process</span><span class="sxs-lookup"><span data-stu-id="d5838-122">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="d5838-123">Processi, thread e Apartment</span><span class="sxs-lookup"><span data-stu-id="d5838-123">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="d5838-124">Comunicazione a thread singolo e multithreading</span><span class="sxs-lookup"><span data-stu-id="d5838-124">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="d5838-125">Apartment a thread singolo</span><span class="sxs-lookup"><span data-stu-id="d5838-125">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




