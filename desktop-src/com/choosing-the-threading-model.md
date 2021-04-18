---
title: Scelta del modello di threading
description: Scelta del modello di threading
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396782"
---
# <a name="choosing-the-threading-model"></a><span data-ttu-id="405bc-103">Scelta del modello di threading</span><span class="sxs-lookup"><span data-stu-id="405bc-103">Choosing the Threading Model</span></span>

<span data-ttu-id="405bc-104">La scelta del modello di threading per un oggetto dipende dalla funzione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="405bc-104">Choosing the threading model for an object depends on the object's function.</span></span> <span data-ttu-id="405bc-105">Un oggetto che esegue l'I/O esteso può supportare il threading libero per fornire la massima risposta ai client consentendo chiamate di interfaccia durante la latenza di I/O.</span><span class="sxs-lookup"><span data-stu-id="405bc-105">An object that does extensive I/O might support free-threading to provide maximum response to clients by allowing interface calls during I/O latency.</span></span> <span data-ttu-id="405bc-106">D'altra parte, un oggetto che interagisce con l'utente potrebbe supportare il threading di Apartment per sincronizzare le chiamate COM in ingresso con le relative operazioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="405bc-106">On the other hand, an object that interacts with the user might support apartment threading to synchronize incoming COM calls with its window operations.</span></span>

<span data-ttu-id="405bc-107">È più facile supportare il threading di Apartment negli appartamenti a thread singolo poiché COM fornisce la sincronizzazione in base alle singole chiamate.</span><span class="sxs-lookup"><span data-stu-id="405bc-107">It is easier to support apartment threading in single-threaded apartments because COM provides synchronization on a per-call basis.</span></span> <span data-ttu-id="405bc-108">Il supporto del threading libero è più difficile perché l'oggetto deve implementare la sincronizzazione. Tuttavia, la risposta ai client potrebbe essere migliore perché la sincronizzazione può essere implementata per sezioni più piccole di codice.</span><span class="sxs-lookup"><span data-stu-id="405bc-108">Supporting free-threading is more difficult because the object must implement synchronization; however, response to clients may be better because synchronization can be implemented for smaller sections of code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="405bc-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="405bc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="405bc-110">Accesso alle interfacce tra gli Apartment</span><span class="sxs-lookup"><span data-stu-id="405bc-110">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="405bc-111">Apartment con multithreading</span><span class="sxs-lookup"><span data-stu-id="405bc-111">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="405bc-112">Problemi di threading del server in-process</span><span class="sxs-lookup"><span data-stu-id="405bc-112">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="405bc-113">Processi, thread e Apartment</span><span class="sxs-lookup"><span data-stu-id="405bc-113">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="405bc-114">Comunicazione a thread singolo e multithreading</span><span class="sxs-lookup"><span data-stu-id="405bc-114">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="405bc-115">Apartment a thread singolo</span><span class="sxs-lookup"><span data-stu-id="405bc-115">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




