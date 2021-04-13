---
description: L'attivazione JIT COM+ causa essenzialmente una compromissione tra i client greedy e i server greedy per ottenere prestazioni ottimali. I client ottengono i riferimenti agli oggetti, mentre i server possono gestire in modo più accurato l'utilizzo della memoria.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Pool di oggetti e attivazione JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401510"
---
# <a name="object-pooling-and-com-jit-activation"></a><span data-ttu-id="bee90-104">Pool di oggetti e attivazione JIT COM+</span><span class="sxs-lookup"><span data-stu-id="bee90-104">Object Pooling and COM+ JIT Activation</span></span>

<span data-ttu-id="bee90-105">L'attivazione JIT COM+ causa essenzialmente una compromissione tra i client greedy e i server greedy per ottenere prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="bee90-105">COM+ JIT activation essentially strikes a compromise between greedy clients and greedy servers for the sake of getting optimal performance.</span></span> <span data-ttu-id="bee90-106">I client ottengono i riferimenti agli oggetti, mentre i server possono gestire in modo più accurato l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="bee90-106">Clients get to keep object references, while servers can more closely manage memory utilization.</span></span>

<span data-ttu-id="bee90-107">È possibile perfezionarlo ulteriormente utilizzando il [pool di oggetti com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="bee90-107">You can refine this further by using [COM+ Object Pooling](com--object-pooling.md).</span></span> <span data-ttu-id="bee90-108">Raggruppando gli oggetti abilitati per JIT, è possibile dedicare una certa quantità di memoria per conservare un certo numero di oggetti attivi in memoria, pronti per il riutilizzo immediato.</span><span class="sxs-lookup"><span data-stu-id="bee90-108">By pooling objects that are JIT activated, you can dedicate a certain amount of memory to hold a certain number of objects active in memory, ready for immediate reuse.</span></span> <span data-ttu-id="bee90-109">Questa operazione è più sensata quando gli oggetti sono costosi da creare, come nel caso in cui contengono più risorse.</span><span class="sxs-lookup"><span data-stu-id="bee90-109">This makes the most sense when objects are expensive to create, as in the case where they hold multiple resources.</span></span>

<span data-ttu-id="bee90-110">In questo modo, è possibile creare un pool di oggetti attivati tramite JIT, in modo da ottenere i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bee90-110">Pooling JIT-activated objects in this manner, you can achieve the following benefits:</span></span>

-   <span data-ttu-id="bee90-111">Tempi di riattivazione degli oggetti molto accelerati.</span><span class="sxs-lookup"><span data-stu-id="bee90-111">Greatly accelerated object reactivation times.</span></span>
-   <span data-ttu-id="bee90-112">Riutilizzo delle risorse costose degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="bee90-112">Reuse of any expensive resources the objects are holding.</span></span>
-   <span data-ttu-id="bee90-113">Gestione più precisa dell'utilizzo di memoria e risorse per gli oggetti in pool.</span><span class="sxs-lookup"><span data-stu-id="bee90-113">More precise governing of memory and resource use for the pooled objects.</span></span>
-   <span data-ttu-id="bee90-114">Conservazione della flessibilità amministrativa in modo che l'applicazione possa essere ridimensionata in modo da usare le risorse disponibili e adattarsi ai requisiti di prestazioni mutevoli.</span><span class="sxs-lookup"><span data-stu-id="bee90-114">Retention of administrative flexibility so that your application can scale to use available resources and adapt to changing performance requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bee90-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bee90-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee90-116">Concetti relativi all'attivazione JIT di COM+</span><span class="sxs-lookup"><span data-stu-id="bee90-116">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="bee90-117">Pool di oggetti COM+</span><span class="sxs-lookup"><span data-stu-id="bee90-117">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="bee90-118">Abilitazione dell'attivazione JIT per un componente</span><span class="sxs-lookup"><span data-stu-id="bee90-118">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="bee90-119">Transazioni e attivazione JIT COM+</span><span class="sxs-lookup"><span data-stu-id="bee90-119">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



