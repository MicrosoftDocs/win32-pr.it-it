---
title: Limiti della firma radice
description: La firma radice è una proprietà di primo livello e sono previsti limiti e costi severi da considerare.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103579"
---
# <a name="root-signature-limits"></a><span data-ttu-id="4ca38-103">Limiti della firma radice</span><span class="sxs-lookup"><span data-stu-id="4ca38-103">Root Signature Limits</span></span>

<span data-ttu-id="4ca38-104">La firma radice è una proprietà di primo livello e sono previsti limiti e costi severi da considerare.</span><span class="sxs-lookup"><span data-stu-id="4ca38-104">The root signature is prime real estate, and there are strict limits and costs to consider.</span></span>

-   [<span data-ttu-id="4ca38-105">Limiti di memoria e costi</span><span class="sxs-lookup"><span data-stu-id="4ca38-105">Memory limits and costs</span></span>](#memory-limits-and-costs)
-   [<span data-ttu-id="4ca38-106">Costi per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="4ca38-106">Performance costs</span></span>](#performance-costs)
-   [<span data-ttu-id="4ca38-107">Campionatori statici</span><span class="sxs-lookup"><span data-stu-id="4ca38-107">Static samplers</span></span>](#static-samplers)
-   [<span data-ttu-id="4ca38-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ca38-108">Related topics</span></span>](#related-topics)

## <a name="memory-limits-and-costs"></a><span data-ttu-id="4ca38-109">Limiti di memoria e costi</span><span class="sxs-lookup"><span data-stu-id="4ca38-109">Memory limits and costs</span></span>

<span data-ttu-id="4ca38-110">La dimensione massima di una firma radice è 64 DWORD.</span><span class="sxs-lookup"><span data-stu-id="4ca38-110">The maximum size of a root signature is 64 DWORDs.</span></span>

<span data-ttu-id="4ca38-111">Questa dimensione massima viene scelta per evitare abusi della firma radice come modalità di archiviazione dei dati in blocco.</span><span class="sxs-lookup"><span data-stu-id="4ca38-111">This maximum size is chosen to prevent abuse of the root signature as a way of storing bulk data.</span></span> <span data-ttu-id="4ca38-112">Ogni voce nella firma radice ha un costo rispetto a questo limite di 64 DWORD:</span><span class="sxs-lookup"><span data-stu-id="4ca38-112">Each entry in the root signature has a cost towards this 64 DWORD limit:</span></span>

-   <span data-ttu-id="4ca38-113">Le tabelle dei descrittori costano 1 DWORD.</span><span class="sxs-lookup"><span data-stu-id="4ca38-113">Descriptor tables cost 1 DWORD each.</span></span>
-   <span data-ttu-id="4ca38-114">Le costanti radice costano 1 DWORD, perché sono valori a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4ca38-114">Root constants cost 1 DWORD each, since they are 32-bit values.</span></span>
-   <span data-ttu-id="4ca38-115">I descrittori radice (indirizzi virtuali GPU a 64 bit) costano 2 DWORD ciascuno.</span><span class="sxs-lookup"><span data-stu-id="4ca38-115">Root descriptors (64-bit GPU virtual addresses) cost 2 DWORDs each.</span></span>

<span data-ttu-id="4ca38-116">I sampler statici non hanno alcun costo nelle dimensioni della firma radice.</span><span class="sxs-lookup"><span data-stu-id="4ca38-116">Static samplers do not have any cost in the size of the root signature.</span></span>

## <a name="performance-costs"></a><span data-ttu-id="4ca38-117">Costi per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="4ca38-117">Performance costs</span></span>

<span data-ttu-id="4ca38-118">Il costo delle prestazioni (in termini di livelli di riferimento indiretto) è zero per una costante radice, 1 per un descrittore radice e 2 per una tabella descrittore.</span><span class="sxs-lookup"><span data-stu-id="4ca38-118">The performance cost (in terms of levels of indirection) are zero for a root constant, 1 for a root descriptor, and 2 for a descriptor table.</span></span> <span data-ttu-id="4ca38-119">Se una firma radice è di grandi dimensioni e si verifica un overflow della memoria più veloce in una memoria leggermente più lenta (che può verificarsi in alcuni componenti hardware), aggiungere 1 al costo in termini di prestazioni per gli elementi di overflow alla fine della firma radice.</span><span class="sxs-lookup"><span data-stu-id="4ca38-119">If a root signature is large and overflows out of the fastest memory into slightly slower memory (which can happen on some hardware), then add 1 to the performance cost for the overflowing items at the end of the root signature.</span></span>

<span data-ttu-id="4ca38-120">È possibile che si verifichi un overflow nell'hardware che potrebbe avere, ad esempio, una dimensione fissa di 16 DWORD per lo spazio degli argomenti radice.</span><span class="sxs-lookup"><span data-stu-id="4ca38-120">An overflow can occur on hardware that might have, for example, a fixed size of 16 DWORDs for root argument space.</span></span> <span data-ttu-id="4ca38-121">Questo limite può essere ulteriormente ridotto di uno se viene usato l'assembler di input.</span><span class="sxs-lookup"><span data-stu-id="4ca38-121">This limit might be further reduced by one if the Input Assembler is used.</span></span> <span data-ttu-id="4ca38-122">In questo caso, se la firma radice è troppo grande per la memoria nativa DWORD 15 o 16, si verifica un overflow in memoria leggermente più lenta.</span><span class="sxs-lookup"><span data-stu-id="4ca38-122">In this case there is overflow into slightly slower memory if the root signature is too large for the 15 or 16 DWORD native memory.</span></span> <span data-ttu-id="4ca38-123">In altri componenti hardware non esiste una memoria di argomenti radice nativa fissa, quindi la situazione di overflow non si verifica mai.</span><span class="sxs-lookup"><span data-stu-id="4ca38-123">In other hardware there is no fixed native root argument memory (so the overflow situation never occurs).</span></span>

<span data-ttu-id="4ca38-124">Per tutti i componenti hardware, se viene modificato un argomento radice, il driver deve mantenere una versione di tutti gli argomenti radice (a differenza di altre risorse di archiviazione quali gli heap dei descrittori e le risorse del buffer, che non vengono sottoporre a controllo delle versioni dal driver).</span><span class="sxs-lookup"><span data-stu-id="4ca38-124">For all hardware, if any root argument changes, the driver must maintain a version of all the root arguments (unlike other storage such as descriptor heaps and buffer resources, which are not versioned by the driver).</span></span> <span data-ttu-id="4ca38-125">Nell'hardware in cui si verifica una situazione di overflow, è necessario eseguire il controllo delle versioni solo dell'area nativa o di overflow, a seconda della posizione in cui si è verificata la modifica.</span><span class="sxs-lookup"><span data-stu-id="4ca38-125">In hardware that an overflow situation occurs, only the native or overflow area needs to be versioned, depending on where the change occurred.</span></span> <span data-ttu-id="4ca38-126">La quantità di controllo delle versioni deve essere ovviamente mantenuta al minimo necessario.</span><span class="sxs-lookup"><span data-stu-id="4ca38-126">The amount of versioning should obviously be kept to the necessary minimum.</span></span>

<span data-ttu-id="4ca38-127">In genere, tenere presenti le linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ca38-127">Generally, consider the following guidelines:</span></span>

-   <span data-ttu-id="4ca38-128">Usare una firma radice di dimensioni ridotte in base alle esigenze, anche se bilanciarla con la flessibilità di una firma radice più grande.</span><span class="sxs-lookup"><span data-stu-id="4ca38-128">Use a small a root signature as necessary, though balance this with the flexibility of a larger root signature.</span></span>
-   <span data-ttu-id="4ca38-129">Disporre i parametri in una firma radice di grandi dimensioni in modo che i parametri con maggiore probabilità vengano modificati spesso o se la latenza di accesso bassa per un determinato parametro è importante, prima di tutto.</span><span class="sxs-lookup"><span data-stu-id="4ca38-129">Arrange parameters in a large root signature so that the parameters most likely to change often, or if low access latency for a given parameter is important, occur first.</span></span>
-   <span data-ttu-id="4ca38-130">Se è opportuno, usare le costanti radice o le visualizzazioni di buffer costanti radice per inserire viste del buffer costanti in un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="4ca38-130">If convenient, use root constants or root constant buffer views over putting constant buffer views in a descriptor heap.</span></span>

## <a name="static-samplers"></a><span data-ttu-id="4ca38-131">Campionatori statici</span><span class="sxs-lookup"><span data-stu-id="4ca38-131">Static samplers</span></span>

<span data-ttu-id="4ca38-132">I sampler statici, ovvero i Sampler in cui lo stato è completamente definito e non modificabile, fanno parte delle firme radice, ma non vengono conteggiati per il limite DWORD 64.</span><span class="sxs-lookup"><span data-stu-id="4ca38-132">Static samplers (samplers where the state is fully defined and immutable) are part of root signatures, but do not count towards the 64 DWORD limit.</span></span> <span data-ttu-id="4ca38-133">Se un campionatore può essere definito come statico, non è necessario che il campionatore faccia parte di un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="4ca38-133">If a sampler can be defined as static, there is no need for the sampler to be part of a descriptor heap.</span></span>

<span data-ttu-id="4ca38-134">Non vi sono costi in termini di prestazioni per l'uso di Sampler statici e una firma radice può contenere una combinazione di Samplers statici (archiviati nella firma radice o nello spazio riservato su alcuni hardware) e i sampler dinamici (archiviati in un heap del descrittore del campionatore).</span><span class="sxs-lookup"><span data-stu-id="4ca38-134">There is no performance cost to using static samplers, and a root signature can contain a mix of static samplers (stored in the root signature, or in reserved space on some hardware) and dynamic samplers (stored in a sampler descriptor heap).</span></span> <span data-ttu-id="4ca38-135">I Sampler in un heap dei descrittori possono essere assegnati dinamicamente e indicizzati, i sampler statici non possono.</span><span class="sxs-lookup"><span data-stu-id="4ca38-135">Samplers in a descriptor heap can be dynamically assigned and indexed, which static samplers cannot.</span></span>

<span data-ttu-id="4ca38-136">I sampler statici possono essere scritti come parte della firma radice in HLSL shader (vedere specificare le [firme radice in HLSL](specifying-root-signatures-in-hlsl.md)).</span><span class="sxs-lookup"><span data-stu-id="4ca38-136">Static samplers can be written as part of the root signature in HLSL shaders (refer to [Specifying Root Signatures in HLSL](specifying-root-signatures-in-hlsl.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ca38-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ca38-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ca38-138">Firme radice</span><span class="sxs-lookup"><span data-stu-id="4ca38-138">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




