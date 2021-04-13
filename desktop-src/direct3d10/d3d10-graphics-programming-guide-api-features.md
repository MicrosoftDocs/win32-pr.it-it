---
description: La pipeline grafica Direct3D 10 rappresenta una modifica dell'architettura fondamentale, ricompilata in base all'hardware e al software per potenziare la prossima generazione di giochi e applicazioni multimediali 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Funzionalità API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225580"
---
# <a name="api-features-direct3d-10"></a><span data-ttu-id="d6d52-103">Funzionalità API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d6d52-103">API Features (Direct3D 10)</span></span>

<span data-ttu-id="d6d52-104">La pipeline grafica Direct3D 10 rappresenta una modifica dell'architettura fondamentale, ricompilata in base all'hardware e al software per potenziare la prossima generazione di giochi e applicazioni multimediali 3D.</span><span class="sxs-lookup"><span data-stu-id="d6d52-104">The Direct3D 10 graphics pipeline represents a fundamental architecture change, rebuilt from the ground-up in hardware and software to power the next-generation of games and 3D multimedia applications.</span></span> <span data-ttu-id="d6d52-105">Usa Windows Display Driver Model (WDDM), che consente di migliorare le prestazioni e il comportamento, ad esempio la memoria GPU virtuale.</span><span class="sxs-lookup"><span data-stu-id="d6d52-105">It uses the Windows Display Driver Model (WDDM), which enables performance and behavioral enhancements such as virtual GPU memory.</span></span>

<span data-ttu-id="d6d52-106">Gli sviluppatori che hanno familiarità con Direct3D 9 scopriranno una serie di miglioramenti funzionali e miglioramenti delle prestazioni in Direct3D 10, tra cui:</span><span class="sxs-lookup"><span data-stu-id="d6d52-106">Developers familiar with Direct3D 9 will discover a series of functional enhancements and performance improvements in Direct3D 10, including:</span></span>

-   <span data-ttu-id="d6d52-107">Possibilità di elaborare intere primitive nella nuova [fase geometry-shader](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d6d52-107">The ability to process entire primitives in the new [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>
-   <span data-ttu-id="d6d52-108">Possibilità di restituire i dati dei vertici generati dalla pipeline alla memoria usando la [fase di output del flusso](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span><span class="sxs-lookup"><span data-stu-id="d6d52-108">The ability to output pipeline-generated vertex data to memory using the [stream-output stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span></span>
-   <span data-ttu-id="d6d52-109">Organizzazione dello stato della pipeline in 5 [oggetti di stato](d3d10-graphics-programming-guide-api-features-state-objects.md)non modificabili, consentendo una configurazione rapida della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6d52-109">Organization of pipeline state into 5 immutable [state objects](d3d10-graphics-programming-guide-api-features-state-objects.md), enabling fast configuration of the pipeline.</span></span>
-   <span data-ttu-id="d6d52-110">Organizzazione di costanti shader in [buffer costanti](d3d10-graphics-programming-guide-resources-types.md), riducendo al minimo l'overhead della larghezza di banda per la fornitura di dati della costante shader.</span><span class="sxs-lookup"><span data-stu-id="d6d52-110">Organization of shader constants into [constant buffers](d3d10-graphics-programming-guide-resources-types.md), minimizing bandwidth overhead for supplying shader-constant data.</span></span>
-   <span data-ttu-id="d6d52-111">Possibilità di eseguire lo swapping e la configurazione di materiali per primitive usando un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="d6d52-111">The ability to perform per-primitive material swapping and setup using a geometry shader.</span></span>
-   <span data-ttu-id="d6d52-112">Nuovi [tipi di risorse](d3d10-graphics-programming-guide-resources-types.md) , incluse le matrici di trama che possono essere indicizzate da shader, e formati di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6d52-112">New [resource types](d3d10-graphics-programming-guide-resources-types.md) (including texture arrays that can be indexed from shaders) and resource formats.</span></span>
-   <span data-ttu-id="d6d52-113">Aumento della generalizzazione dell'accesso alle risorse tramite una [vista](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="d6d52-113">Increased generalization of resource access using a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>
-   <span data-ttu-id="d6d52-114">I bit di funzionalità hardware legacy sono stati rimossi a favore di un set completo di funzionalità garantite, che sono destinate all'hardware di classe Direct3D 10 (minima).</span><span class="sxs-lookup"><span data-stu-id="d6d52-114">Legacy hardware capability bits (caps) have been removed in favor of a rich set of guaranteed functionality, which targets Direct3D 10-class hardware (minimum).</span></span>
-   <span data-ttu-id="d6d52-115">[Runtime sovrapposto](d3d10-graphics-programming-guide-api-features-layers.md) : l'API Direct3D 10 è costruita con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori (debug e così via) nei livelli esterni.</span><span class="sxs-lookup"><span data-stu-id="d6d52-115">[Layered Runtime](d3d10-graphics-programming-guide-api-features-layers.md) - The Direct3D 10 API is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality (debug, etc.) in outer layers.</span></span>
-   <span data-ttu-id="d6d52-116">Integrazione completa di HLSL: tutti gli shader Direct3D 10 sono scritti in HLSL e implementati con il [nucleo di shader comune](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span><span class="sxs-lookup"><span data-stu-id="d6d52-116">Full HLSL integration - All Direct3D 10 shaders are written in HLSL and implemented with the [common-shader core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span></span>
-   <span data-ttu-id="d6d52-117">Aumento del numero di destinazioni di rendering, trame e Sampler.</span><span class="sxs-lookup"><span data-stu-id="d6d52-117">An increase in the number of render targets, textures, and samplers.</span></span> <span data-ttu-id="d6d52-118">Non esiste neanche un limite di lunghezza dello shader.</span><span class="sxs-lookup"><span data-stu-id="d6d52-118">There is also no shader length limit.</span></span>
-   <span data-ttu-id="d6d52-119">Operazioni shader Integer e bit per bit.</span><span class="sxs-lookup"><span data-stu-id="d6d52-119">Integer and bitwise shader operations.</span></span>
-   <span data-ttu-id="d6d52-120">Readback di una superficie di profondità/stencil o una risorsa multicampionata, quando non è più associata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d6d52-120">Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.</span></span>
-   <span data-ttu-id="d6d52-121">Supporto multicampionato da Alpha a code coverage.</span><span class="sxs-lookup"><span data-stu-id="d6d52-121">Multisampled alpha-to-coverage support.</span></span>

<span data-ttu-id="d6d52-122">Ci sono altre differenze di comportamento che gli sviluppatori di Direct3D 9 devono conoscere (vedere le [considerazioni su Direct3D 9 in Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span><span class="sxs-lookup"><span data-stu-id="d6d52-122">There are additional behavioral differences that Direct3D 9 developers should also be aware of (see [Direct3D 9 to Direct3D 10 Considerations](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span></span>

<span data-ttu-id="d6d52-123">Di seguito è riportato un elenco di funzionalità di Direct3D 9 che non sono più supportate o sono state rivedute in Direct3D 10 (vedere [funzionalità deprecate](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span><span class="sxs-lookup"><span data-stu-id="d6d52-123">Here is a list of Direct3D 9 features that either are no longer supported, or have been revised in Direct3D 10 (see [Deprecated Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6d52-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6d52-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6d52-125">Guida di programmazione per Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="d6d52-125">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
