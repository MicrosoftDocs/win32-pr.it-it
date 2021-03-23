---
title: Pipeline e shader con Direct3D 12
description: La pipeline programmabile di Direct3D 12 aumenta significativamente le prestazioni di rendering rispetto alle interfacce di programmazione grafica di generazione precedente.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548815"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a><span data-ttu-id="eedbf-103">Pipeline e shader con Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eedbf-103">Pipelines and Shaders with Direct3D 12</span></span>

<span data-ttu-id="eedbf-104">La pipeline programmabile di Direct3D 12 aumenta significativamente le prestazioni di rendering rispetto alle interfacce di programmazione grafica di generazione precedente.</span><span class="sxs-lookup"><span data-stu-id="eedbf-104">The Direct3D 12 programmable pipeline significantly increases rendering performance compared to previous generation graphics programming interfaces.</span></span>

-   [<span data-ttu-id="eedbf-105">Pipeline grafica Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eedbf-105">Direct3D 12 graphics pipeline</span></span>](#direct3d-12-graphics-pipeline)
-   [<span data-ttu-id="eedbf-106">Oggetti stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="eedbf-106">Pipeline state objects</span></span>](#pipeline-state-objects)
-   [<span data-ttu-id="eedbf-107">Pipeline di calcolo Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eedbf-107">Direct3D 12 compute pipeline</span></span>](#direct3d-12-compute-pipeline)
-   [<span data-ttu-id="eedbf-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eedbf-108">Related topics</span></span>](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a><span data-ttu-id="eedbf-109">Pipeline grafica Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eedbf-109">Direct3D 12 graphics pipeline</span></span>

<span data-ttu-id="eedbf-110">Il diagramma seguente illustra la pipeline grafica e lo stato di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="eedbf-110">The following diagram illustrates the Direct3D 12 graphics pipeline and state.</span></span>

![diagramma che illustra la pipeline e lo stato di Direct3D 12](images/pipeline.png)

<span data-ttu-id="eedbf-112">Una pipeline grafica è il flusso sequenziale di input e output di dati quando la GPU esegue il rendering dei frame.</span><span class="sxs-lookup"><span data-stu-id="eedbf-112">A graphics pipeline is the sequential flow of data inputs and outputs as the GPU renders frames.</span></span> <span data-ttu-id="eedbf-113">Dato lo stato e gli input della pipeline, la GPU esegue una serie di operazioni per creare le immagini risultanti.</span><span class="sxs-lookup"><span data-stu-id="eedbf-113">Given the pipeline state and inputs, the GPU performs a series of operations to create the resulting images.</span></span> <span data-ttu-id="eedbf-114">Una pipeline grafica contiene shader, che eseguono effetti e calcoli di rendering programmabili e operazioni di funzione fisse.</span><span class="sxs-lookup"><span data-stu-id="eedbf-114">A graphics pipeline contains shaders, which perform programmable rendering effects and calculations, and fixed function operations.</span></span>

<span data-ttu-id="eedbf-115">Quando si fa riferimento al diagramma di stato della pipeline, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="eedbf-115">Note the following when referring to the pipeline state diagram:</span></span>

-   <span data-ttu-id="eedbf-116">Le tabelle e gli heap del descrittore possono essere disposti arbitrariamente: è possibile fare riferimento a SRVs, CBVs e UAV e allocarli in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="eedbf-116">The descriptor tables and heaps can be arbitrarily arranged: SRVs, CBVs and UAVs can be referenced and allocated in any order.</span></span>
-   <span data-ttu-id="eedbf-117">Alcune operazioni della pipeline sono configurabili.</span><span class="sxs-lookup"><span data-stu-id="eedbf-117">Some operations of the pipeline are configurable.</span></span> <span data-ttu-id="eedbf-118">La fusione di output, ad esempio, agisce in genere su una base di lettura e modifica con la destinazione di rendering e le visualizzazioni depth stencil.</span><span class="sxs-lookup"><span data-stu-id="eedbf-118">For example, the output merger typically operates on a read-modify-write basis with the render target and depth stencil views.</span></span> <span data-ttu-id="eedbf-119">Tuttavia, la pipeline può essere configurata in modo che una di queste viste sia di sola lettura o di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="eedbf-119">However the pipeline can be configured so that either of these views are read-only or write-only.</span></span>
-   <span data-ttu-id="eedbf-120">I sampler statici non fanno parte degli argomenti radice perché sono statici.</span><span class="sxs-lookup"><span data-stu-id="eedbf-120">Static samplers are not part of the root arguments since they are static.</span></span>

## <a name="pipeline-state-objects"></a><span data-ttu-id="eedbf-121">Oggetti stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="eedbf-121">Pipeline state objects</span></span>

<span data-ttu-id="eedbf-122">Direct3D 12 introduce l'oggetto di stato della pipeline (PSO).</span><span class="sxs-lookup"><span data-stu-id="eedbf-122">Direct3D 12 introduces the pipeline state object (PSO).</span></span> <span data-ttu-id="eedbf-123">Anziché archiviare e rappresentare lo stato della pipeline in un numero elevato di oggetti di alto livello, gli Stati dei componenti della pipeline come Assembler di input, rasterizzatore, pixel shader e Unione di output vengono archiviati in un oggetto PSO.</span><span class="sxs-lookup"><span data-stu-id="eedbf-123">Rather than storing and representing pipeline state across a large number of high-level objects, the states of pipeline components like the input assembler, rasterizer, pixel shader, and output merger are stored in a PSO.</span></span> <span data-ttu-id="eedbf-124">Un oggetto PSO è un oggetto di stato della pipeline unificato che non è modificabile dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="eedbf-124">A PSO is a unified pipeline state object that is immutable after creation.</span></span> <span data-ttu-id="eedbf-125">Il PSO attualmente selezionato può essere modificato in modo rapido e dinamico e l'hardware e i driver possono convertire direttamente un oggetto PSO in istruzioni e stato hardware nativi, preparando la GPU per l'elaborazione grafica.</span><span class="sxs-lookup"><span data-stu-id="eedbf-125">The currently selected PSO can be changed quickly and dynamically, and the hardware and drivers can directly convert a PSO into native hardware instructions and state, readying the GPU for graphics processing.</span></span> <span data-ttu-id="eedbf-126">Per applicare un oggetto PSO, l'hardware copia una quantità minima di stato pre-calcolato direttamente nei registri hardware.</span><span class="sxs-lookup"><span data-stu-id="eedbf-126">To apply a PSO, the hardware copies a minimal amount of pre-computed state directly to the hardware registers.</span></span> <span data-ttu-id="eedbf-127">In questo modo viene rimosso il sovraccarico causato dal driver grafico che esegue continuamente il ricalcolo dello stato dell'hardware in base a tutte le impostazioni di rendering e pipeline attualmente applicabili.</span><span class="sxs-lookup"><span data-stu-id="eedbf-127">This removes the overhead caused by the graphics driver continually recomputing hardware state based on all currently applicable rendering and pipeline settings.</span></span> <span data-ttu-id="eedbf-128">Il risultato è una riduzione significativa del sovraccarico delle chiamate di progetto, delle prestazioni migliorate e di altre chiamate per frame.</span><span class="sxs-lookup"><span data-stu-id="eedbf-128">The result is significantly reduced draw call overhead, increased performance, and more draw calls per frame.</span></span>

<span data-ttu-id="eedbf-129">Il PSO attualmente applicato definisce e connette tutti gli shader usati nella pipeline di rendering.</span><span class="sxs-lookup"><span data-stu-id="eedbf-129">The currently applied PSO defines and connects all of the shaders being used in the rendering pipeline.</span></span> <span data-ttu-id="eedbf-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) è precompilato in oggetti shader, che vengono quindi usati in fase di esecuzione come input per gli oggetti di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="eedbf-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) is pre-compiled into shader objects, which are then used at run time as input for pipeline state objects.</span></span> <span data-ttu-id="eedbf-131">Per ulteriori informazioni sul modo in cui le funzioni PSO all'interno della pipeline grafica, vedere [gestione dello stato della pipeline grafica in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="eedbf-131">For more information about how the PSO functions within the graphics pipeline, see [Managing graphics pipeline state in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="direct3d-12-compute-pipeline"></a><span data-ttu-id="eedbf-132">Pipeline di calcolo Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eedbf-132">Direct3D 12 compute pipeline</span></span>

<span data-ttu-id="eedbf-133">Il diagramma seguente illustra la pipeline di calcolo e lo stato di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="eedbf-133">The following diagram illustrates the Direct3D 12 compute pipeline and state.</span></span>

![Diagramma che mostra la pipeline di calcolo Direct3D 12.](images/compute-pipeline.png)

<span data-ttu-id="eedbf-135">In questa pipeline non sono presenti unità di funzione fisse, tuttavia gli heap del descrittore, gli heap del campionatore e i sampler statici sono ancora disponibili in calcolo.</span><span class="sxs-lookup"><span data-stu-id="eedbf-135">There are no fixed function units in this pipeline, however descriptor heaps, sampler heaps and static samplers are still available in compute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eedbf-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eedbf-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eedbf-137">Invio di lavoro in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eedbf-137">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 