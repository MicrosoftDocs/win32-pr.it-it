---
title: Livelli hardware
description: I livelli di hardware dal livello 1 al livello 3 hanno risorse crescenti disponibili per la pipeline.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548782"
---
# <a name="hardware-tiers"></a><span data-ttu-id="a0452-103">Livelli hardware</span><span class="sxs-lookup"><span data-stu-id="a0452-103">Hardware Tiers</span></span>

<span data-ttu-id="a0452-104">I livelli di hardware dal livello 1 al livello 3 hanno risorse crescenti disponibili per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0452-104">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span>

-   [<span data-ttu-id="a0452-105">Limiti dipendenti dall'hardware</span><span class="sxs-lookup"><span data-stu-id="a0452-105">Limits dependant on hardware</span></span>](#limits-dependant-on-hardware)
-   [<span data-ttu-id="a0452-106">Limiti invariabili</span><span class="sxs-lookup"><span data-stu-id="a0452-106">Invariable limits</span></span>](#invariable-limits)
-   [<span data-ttu-id="a0452-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0452-107">Related topics</span></span>](#related-topics)

## <a name="limits-dependant-on-hardware"></a><span data-ttu-id="a0452-108">Limiti dipendenti dall'hardware</span><span class="sxs-lookup"><span data-stu-id="a0452-108">Limits dependant on hardware</span></span>



| <span data-ttu-id="a0452-109">Risorse disponibili per la pipeline</span><span class="sxs-lookup"><span data-stu-id="a0452-109">Resources Available to the Pipeline</span></span>                                                                                                              | <span data-ttu-id="a0452-110">Livello 1</span><span class="sxs-lookup"><span data-stu-id="a0452-110">Tier 1</span></span>                                                                   | <span data-ttu-id="a0452-111">Livello 2</span><span class="sxs-lookup"><span data-stu-id="a0452-111">Tier 2</span></span>        | <span data-ttu-id="a0452-112">Livello 3</span><span class="sxs-lookup"><span data-stu-id="a0452-112">Tier 3</span></span>        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| <span data-ttu-id="a0452-113">Livelli di funzionalità</span><span class="sxs-lookup"><span data-stu-id="a0452-113">Feature levels</span></span>                                                                                                                                   | <span data-ttu-id="a0452-114">11.0 +</span><span class="sxs-lookup"><span data-stu-id="a0452-114">11.0+</span></span>                                                                    | <span data-ttu-id="a0452-115">11.0 +</span><span class="sxs-lookup"><span data-stu-id="a0452-115">11.0+</span></span>         | <span data-ttu-id="a0452-116">11.1 +</span><span class="sxs-lookup"><span data-stu-id="a0452-116">11.1+</span></span>         |
| <span data-ttu-id="a0452-117">Numero massimo di descrittori in un heap Constant Buffer View (CBV), Shader Resource View (SRV) o Unordered Access View (UAV) usato per il rendering</span><span class="sxs-lookup"><span data-stu-id="a0452-117">Maximum number of descriptors in a Constant Buffer View (CBV), Shader Resource View (SRV), or Unordered Access View(UAV) heap used for rendering</span></span> | <span data-ttu-id="a0452-118">1\.000.000</span><span class="sxs-lookup"><span data-stu-id="a0452-118">1,000,000</span></span>                                                                | <span data-ttu-id="a0452-119">1\.000.000</span><span class="sxs-lookup"><span data-stu-id="a0452-119">1,000,000</span></span>     | <span data-ttu-id="a0452-120">1.000.000 +</span><span class="sxs-lookup"><span data-stu-id="a0452-120">1,000,000+</span></span>    |
| <span data-ttu-id="a0452-121">Numero massimo di visualizzazioni del buffer costante in tutte le tabelle dei descrittori per fase shader</span><span class="sxs-lookup"><span data-stu-id="a0452-121">Maximum number of Constant Buffer Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="a0452-122">14</span><span class="sxs-lookup"><span data-stu-id="a0452-122">14</span></span>                                                                       | <span data-ttu-id="a0452-123">14</span><span class="sxs-lookup"><span data-stu-id="a0452-123">14</span></span>            | <span data-ttu-id="a0452-124">**heap completo**</span><span class="sxs-lookup"><span data-stu-id="a0452-124">**full heap**</span></span> |
| <span data-ttu-id="a0452-125">Numero massimo di visualizzazioni delle risorse dello shader in tutte le tabelle dei descrittori per fase shader</span><span class="sxs-lookup"><span data-stu-id="a0452-125">Maximum number of Shader Resource Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="a0452-126">128</span><span class="sxs-lookup"><span data-stu-id="a0452-126">128</span></span>                                                                      | <span data-ttu-id="a0452-127">**heap completo**</span><span class="sxs-lookup"><span data-stu-id="a0452-127">**full heap**</span></span> | <span data-ttu-id="a0452-128">heap completo</span><span class="sxs-lookup"><span data-stu-id="a0452-128">full heap</span></span>     |
| <span data-ttu-id="a0452-129">Numero massimo di viste di accesso non ordinate in tutte le tabelle dei descrittori in tutte le fasi</span><span class="sxs-lookup"><span data-stu-id="a0452-129">Maximum number of Unordered Access Views in all descriptor tables across all stages</span></span>                                                              | <span data-ttu-id="a0452-130">64 per i livelli di funzionalità 11.1 +</span><span class="sxs-lookup"><span data-stu-id="a0452-130">64 for feature levels 11.1+</span></span><br/> <span data-ttu-id="a0452-131">8 per il livello di funzionalità 11</span><span class="sxs-lookup"><span data-stu-id="a0452-131">8 for feature level 11</span></span><br/> | <span data-ttu-id="a0452-132">64</span><span class="sxs-lookup"><span data-stu-id="a0452-132">64</span></span>            | <span data-ttu-id="a0452-133">**heap completo**</span><span class="sxs-lookup"><span data-stu-id="a0452-133">**full heap**</span></span> |
| <span data-ttu-id="a0452-134">Numero massimo di campioni in tutte le tabelle dei descrittori per fase shader</span><span class="sxs-lookup"><span data-stu-id="a0452-134">Maximum number of Samplers in all descriptor tables per shader stage</span></span>                                                                             | <span data-ttu-id="a0452-135">16</span><span class="sxs-lookup"><span data-stu-id="a0452-135">16</span></span>                                                                       | <span data-ttu-id="a0452-136">**2048**</span><span class="sxs-lookup"><span data-stu-id="a0452-136">**2048**</span></span> | <span data-ttu-id="a0452-137">2048</span><span class="sxs-lookup"><span data-stu-id="a0452-137">2048</span></span>     |



 

<span data-ttu-id="a0452-138">Le voci in **grassetto** evidenziano miglioramenti significativi rispetto al livello precedente.</span><span class="sxs-lookup"><span data-stu-id="a0452-138">**Bold** entries highlight significant improvements over the previous tier.</span></span>

<span data-ttu-id="a0452-139">Esiste una restrizione aggiuntiva per l'hardware di livello 1 che si applica a tutti gli heap e all'hardware di livello 2 che si applica agli heap CBV e UAV, che tutte le voci dell'heap dei descrittori incluse nelle tabelle dei descrittori nella firma radice *devono* essere popolate con i descrittori durante l'esecuzione dello shader, anche se lo shader (probabilmente a causa della dirama</span><span class="sxs-lookup"><span data-stu-id="a0452-139">There is an additional restriction for Tier 1 hardware that applies to all heaps, and to Tier 2 hardware that applies to CBV and UAV heaps, that all descriptor heap entries covered by descriptor tables in the root signature *must* be populated with descriptors by the time the shader executes, even if the shader (perhaps due to branching) does not need the descriptor.</span></span> <span data-ttu-id="a0452-140">Non esiste alcuna restrizione per l'hardware di livello 3.</span><span class="sxs-lookup"><span data-stu-id="a0452-140">There is no such restriction for Tier 3 hardware.</span></span> <span data-ttu-id="a0452-141">Una mitigazione per questa restrizione è l'uso diligente dei [descrittori null](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="a0452-141">One mitigation for this restriction is the diligent use of [Null descriptors](descriptors.md).</span></span>

## <a name="invariable-limits"></a><span data-ttu-id="a0452-142">Limiti invariabili</span><span class="sxs-lookup"><span data-stu-id="a0452-142">Invariable limits</span></span>

<span data-ttu-id="a0452-143">Il numero massimo di campioni in un heap del descrittore visibile dello shader è 2048.</span><span class="sxs-lookup"><span data-stu-id="a0452-143">The maximum number of samplers in a shader visible descriptor heap is 2048.</span></span>

<span data-ttu-id="a0452-144">Il numero massimo di campioni statici univoci tra le firme radice attive è 2032, che lascia 16 per i driver che necessitano dei propri Sampler.</span><span class="sxs-lookup"><span data-stu-id="a0452-144">The maximum number of unique static samplers across live root signatures is 2032 (which leaves 16 for drivers that need their own samplers).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0452-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0452-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0452-146">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="a0452-146">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="a0452-147">Livelli di funzionalità hardware</span><span class="sxs-lookup"><span data-stu-id="a0452-147">Hardware Feature Levels</span></span>](hardware-feature-levels.md)
</dt> </dl>

 

 





