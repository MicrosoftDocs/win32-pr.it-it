---
title: Comunicazione Single-Threaded e multithreading
description: Comunicazione Single-Threaded e multithreading
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329303"
---
# <a name="single-threaded-and-multithreaded-communication"></a><span data-ttu-id="0ed92-103">Comunicazione Single-Threaded e multithreading</span><span class="sxs-lookup"><span data-stu-id="0ed92-103">Single-Threaded and Multithreaded Communication</span></span>

<span data-ttu-id="0ed92-104">Un client o un server che supporta gli Apartment a thread singolo e a thread multipli avrà un apartment multithread, che contiene tutti i thread inizializzati come a thread libero e uno o più Apartment a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="0ed92-104">A client or server that supports both single-threaded and multithreaded apartments will have one multithreaded apartment, containing all threads initialized as free-threaded, and one or more single-threaded apartments.</span></span> <span data-ttu-id="0ed92-105">È necessario effettuare il marshalling di puntatori di interfaccia tra Apartment, ma è possibile usare senza marshalling in un Apartment.</span><span class="sxs-lookup"><span data-stu-id="0ed92-105">Interface pointers must be marshaled between apartments but can be used without marshaling within an apartment.</span></span> <span data-ttu-id="0ed92-106">Le chiamate agli oggetti in un Apartment a thread singolo verranno sincronizzate da COM.</span><span class="sxs-lookup"><span data-stu-id="0ed92-106">Calls to objects in a single-threaded apartment will be synchronized by COM.</span></span> <span data-ttu-id="0ed92-107">Le chiamate a oggetti nell'Apartment con multithreading non verranno sincronizzate da COM.</span><span class="sxs-lookup"><span data-stu-id="0ed92-107">Calls to objects in the multithreaded apartment will not be synchronized by COM.</span></span>

<span data-ttu-id="0ed92-108">Tutte le informazioni sugli Apartment a thread singolo si applicano ai thread contrassegnati come modello di Apartment e tutte le informazioni sugli Apartment con multithreading si applicano a tutti i thread contrassegnati come a thread libero.</span><span class="sxs-lookup"><span data-stu-id="0ed92-108">All of the information on single-threaded apartments applies to the threads marked as apartment model, and all of the information on multithreaded apartments applies to all of the threads marked as free-threaded.</span></span> <span data-ttu-id="0ed92-109">Le regole di threading dell'Apartment si applicano alla comunicazione tra Apartment, che richiede il marshalling dei puntatori di interfaccia tra gli appartamenti con chiamate a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) e [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), come descritto in [Apartment a thread singolo](single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="0ed92-109">Apartment threading rules apply to inter-apartment communication, requiring that interface pointers be marshaled between apartments with calls to [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) and [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), as described in [Single-Threaded Apartments](single-threaded-apartments.md).</span></span>

> [!Note]  
> <span data-ttu-id="0ed92-110">Quando si gestiscono server in-process, è necessario tenere presenti alcune considerazioni speciali.</span><span class="sxs-lookup"><span data-stu-id="0ed92-110">Some special considerations apply when dealing with in-process servers.</span></span> <span data-ttu-id="0ed92-111">Per ulteriori informazioni, vedere [problemi di threading del server in-process](in-process-server-threading-issues.md).</span><span class="sxs-lookup"><span data-stu-id="0ed92-111">For more information, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0ed92-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ed92-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ed92-113">Accesso alle interfacce tra gli Apartment</span><span class="sxs-lookup"><span data-stu-id="0ed92-113">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="0ed92-114">Scelta del modello di threading</span><span class="sxs-lookup"><span data-stu-id="0ed92-114">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="0ed92-115">Apartment con multithreading</span><span class="sxs-lookup"><span data-stu-id="0ed92-115">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="0ed92-116">Problemi di threading del server in-process</span><span class="sxs-lookup"><span data-stu-id="0ed92-116">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="0ed92-117">Processi, thread e Apartment</span><span class="sxs-lookup"><span data-stu-id="0ed92-117">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="0ed92-118">Apartment a thread singolo</span><span class="sxs-lookup"><span data-stu-id="0ed92-118">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




