---
title: Heap descrittore
description: Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104655"
---
# <a name="descriptor-heaps"></a><span data-ttu-id="3d470-103">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="3d470-103">Descriptor Heaps</span></span>

<span data-ttu-id="3d470-104">Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore.</span><span class="sxs-lookup"><span data-stu-id="3d470-104">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3d470-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3d470-105">In this section</span></span>



| <span data-ttu-id="3d470-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="3d470-106">Topic</span></span>                                                                                             | <span data-ttu-id="3d470-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d470-107">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d470-108">Cenni preliminari sugli heap di descrittori</span><span class="sxs-lookup"><span data-stu-id="3d470-108">Descriptor Heaps Overview</span></span>](descriptor-heaps-overview.md)<br/>                             | <span data-ttu-id="3d470-109">Gli heap del descrittore contengono molti tipi di oggetto che non fanno parte di un oggetto di stato della pipeline (PSO), ad esempio viste di risorse shader (SRVs), viste di accesso non ordinate (UAV), viste del buffer costante (CBVs) e Samplers.</span><span class="sxs-lookup"><span data-stu-id="3d470-109">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span> <br/>                |
| [<span data-ttu-id="3d470-110">Livelli hardware</span><span class="sxs-lookup"><span data-stu-id="3d470-110">Hardware Tiers</span></span>](hardware-support.md)<br/>                                                 | <span data-ttu-id="3d470-111">I livelli di hardware dal livello 1 al livello 3 hanno risorse crescenti disponibili per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d470-111">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="3d470-112">Heap del descrittore visibile dello shader</span><span class="sxs-lookup"><span data-stu-id="3d470-112">Shader Visible Descriptor Heaps</span></span>](shader-visible-descriptor-heaps.md)<br/>                 | <span data-ttu-id="3d470-113">Gli heap del descrittore visibile dello shader sono heap di descrittori a cui possono fare riferimento gli shader tramite le tabelle dei descrittori.</span><span class="sxs-lookup"><span data-stu-id="3d470-113">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="3d470-114">Heap descrittori non shader visibili</span><span class="sxs-lookup"><span data-stu-id="3d470-114">Non Shader Visible Descriptor Heaps</span></span>](non-shader-visible-descriptor-heaps.md)<br/>         | <span data-ttu-id="3d470-115">Per gli shader non è possibile fare riferimento ad alcuni heap del descrittore tramite le tabelle dei descrittori, ma esistono per supportare l'app nella gestione temporanea dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile dello shader.</span><span class="sxs-lookup"><span data-stu-id="3d470-115">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span><br/> |
| [<span data-ttu-id="3d470-116">Creazione di heap descrittore</span><span class="sxs-lookup"><span data-stu-id="3d470-116">Creating Descriptor Heaps</span></span>](creating-descriptor-heaps.md)<br/>                             | <span data-ttu-id="3d470-117">Per creare e configurare un heap del descrittore, è necessario selezionare un tipo di heap del descrittore, determinare il numero di descrittori in esso contenuti e impostare i flag che indicano se si tratta di una CPU visibile e/o uno shader visibile.</span><span class="sxs-lookup"><span data-stu-id="3d470-117">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span> <br/>                    |
| [<span data-ttu-id="3d470-118">Impostazione e popolamento degli heap descrittore</span><span class="sxs-lookup"><span data-stu-id="3d470-118">Setting and Populating Descriptor Heaps</span></span>](setting-descriptor-heaps.md)<br/>                | <span data-ttu-id="3d470-119">I tipi di heap del descrittore che è possibile impostare in un elenco di comandi sono quelli che contengono descrittori per cui è possibile usare le tabelle dei descrittori (al massimo uno per volta).</span><span class="sxs-lookup"><span data-stu-id="3d470-119">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span> <br/>                                                        |
| [<span data-ttu-id="3d470-120">Riepilogo di configurabilità heap descrittore</span><span class="sxs-lookup"><span data-stu-id="3d470-120">Descriptor Heap Configurability Summary</span></span>](descriptor-heap-configurability-summary.md)<br/> | <span data-ttu-id="3d470-121">Nella tabella seguente sono riepilogate le informazioni sullo shader e sul supporto dell'heap visibile non shader.</span><span class="sxs-lookup"><span data-stu-id="3d470-121">The following table summarizes information about Shader and non-Shader visible heap support.</span></span><br/>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3d470-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d470-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d470-123">Descrittori</span><span class="sxs-lookup"><span data-stu-id="3d470-123">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="3d470-124">Tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="3d470-124">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="3d470-125">**ID3D12DescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="3d470-125">**ID3D12DescriptorHeap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[<span data-ttu-id="3d470-126">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="3d470-126">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="3d470-127">Firme radice</span><span class="sxs-lookup"><span data-stu-id="3d470-127">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





