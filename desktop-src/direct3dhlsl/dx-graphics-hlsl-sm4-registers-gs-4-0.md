---
title: Registri-gs_4_0
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da Geometry shader versione 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515811"
---
# <a name="registers---gs_4_0"></a><span data-ttu-id="251ea-103">Registri-GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="251ea-103">Registers - gs\_4\_0</span></span>

<span data-ttu-id="251ea-104">Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da Geometry shader versione 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="251ea-104">This section contains reference information for the input and output registers implemented by geometry shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="251ea-105">Registri di input</span><span class="sxs-lookup"><span data-stu-id="251ea-105">Input Registers</span></span>



| <span data-ttu-id="251ea-106">Registrazione</span><span class="sxs-lookup"><span data-stu-id="251ea-106">Register</span></span>                 | <span data-ttu-id="251ea-107">Nome</span><span class="sxs-lookup"><span data-stu-id="251ea-107">Name</span></span> | <span data-ttu-id="251ea-108">Conteggio</span><span class="sxs-lookup"><span data-stu-id="251ea-108">Count</span></span>              | <span data-ttu-id="251ea-109">L/S</span><span class="sxs-lookup"><span data-stu-id="251ea-109">R/W</span></span> | <span data-ttu-id="251ea-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="251ea-110">Dimension</span></span>        | <span data-ttu-id="251ea-111">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="251ea-111">Indexable by r\#</span></span> | <span data-ttu-id="251ea-112">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="251ea-112">Defaults</span></span> | <span data-ttu-id="251ea-113">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="251ea-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="251ea-114">r\#</span><span class="sxs-lookup"><span data-stu-id="251ea-114">r\#</span></span>                      |      | <span data-ttu-id="251ea-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="251ea-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="251ea-116">L/S</span><span class="sxs-lookup"><span data-stu-id="251ea-116">R/W</span></span> | <span data-ttu-id="251ea-117">4</span><span class="sxs-lookup"><span data-stu-id="251ea-117">4</span></span>                | <span data-ttu-id="251ea-118">No</span><span class="sxs-lookup"><span data-stu-id="251ea-118">No</span></span>               | <span data-ttu-id="251ea-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-119">None</span></span>     | <span data-ttu-id="251ea-120">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-120">Yes</span></span>          |
| <span data-ttu-id="251ea-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="251ea-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="251ea-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="251ea-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="251ea-123">L/S</span><span class="sxs-lookup"><span data-stu-id="251ea-123">R/W</span></span> | <span data-ttu-id="251ea-124">4</span><span class="sxs-lookup"><span data-stu-id="251ea-124">4</span></span>                | <span data-ttu-id="251ea-125">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-125">Yes</span></span>              | <span data-ttu-id="251ea-126">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-126">None</span></span>     | <span data-ttu-id="251ea-127">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-127">Yes</span></span>          |
| <span data-ttu-id="251ea-128">v ( \# \[ \] \[ elemento Vertex)\]</span><span class="sxs-lookup"><span data-stu-id="251ea-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="251ea-129">32</span><span class="sxs-lookup"><span data-stu-id="251ea-129">32</span></span>                 | <span data-ttu-id="251ea-130">R</span><span class="sxs-lookup"><span data-stu-id="251ea-130">R</span></span>   | <span data-ttu-id="251ea-131">4 (comp) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="251ea-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="251ea-132">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-132">Yes</span></span>              | <span data-ttu-id="251ea-133">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-133">None</span></span>     | <span data-ttu-id="251ea-134">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-134">Yes</span></span>          |
| <span data-ttu-id="251ea-135">vprim</span><span class="sxs-lookup"><span data-stu-id="251ea-135">vprim</span></span>                    |      | <span data-ttu-id="251ea-136">1</span><span class="sxs-lookup"><span data-stu-id="251ea-136">1</span></span>                  | <span data-ttu-id="251ea-137">R</span><span class="sxs-lookup"><span data-stu-id="251ea-137">R</span></span>   | <span data-ttu-id="251ea-138">1</span><span class="sxs-lookup"><span data-stu-id="251ea-138">1</span></span>                | <span data-ttu-id="251ea-139">No</span><span class="sxs-lookup"><span data-stu-id="251ea-139">No</span></span>               | <span data-ttu-id="251ea-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-140">None</span></span>     | <span data-ttu-id="251ea-141">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-141">Yes</span></span>          |
| <span data-ttu-id="251ea-142">t\#</span><span class="sxs-lookup"><span data-stu-id="251ea-142">t\#</span></span>                      |      | <span data-ttu-id="251ea-143">128</span><span class="sxs-lookup"><span data-stu-id="251ea-143">128</span></span>                | <span data-ttu-id="251ea-144">R</span><span class="sxs-lookup"><span data-stu-id="251ea-144">R</span></span>   | <span data-ttu-id="251ea-145">1</span><span class="sxs-lookup"><span data-stu-id="251ea-145">1</span></span>                | <span data-ttu-id="251ea-146">No</span><span class="sxs-lookup"><span data-stu-id="251ea-146">No</span></span>               | <span data-ttu-id="251ea-147">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-147">None</span></span>     | <span data-ttu-id="251ea-148">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-148">Yes</span></span>          |
| <span data-ttu-id="251ea-149">s\#</span><span class="sxs-lookup"><span data-stu-id="251ea-149">s\#</span></span>                      |      | <span data-ttu-id="251ea-150">16</span><span class="sxs-lookup"><span data-stu-id="251ea-150">16</span></span>                 | <span data-ttu-id="251ea-151">R</span><span class="sxs-lookup"><span data-stu-id="251ea-151">R</span></span>   | <span data-ttu-id="251ea-152">1</span><span class="sxs-lookup"><span data-stu-id="251ea-152">1</span></span>                | <span data-ttu-id="251ea-153">No</span><span class="sxs-lookup"><span data-stu-id="251ea-153">No</span></span>               | <span data-ttu-id="251ea-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-154">None</span></span>     | <span data-ttu-id="251ea-155">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-155">Yes</span></span>          |
| <span data-ttu-id="251ea-156">\# \[ Indice CB\]</span><span class="sxs-lookup"><span data-stu-id="251ea-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="251ea-157">15</span><span class="sxs-lookup"><span data-stu-id="251ea-157">15</span></span>                 | <span data-ttu-id="251ea-158">R</span><span class="sxs-lookup"><span data-stu-id="251ea-158">R</span></span>   | <span data-ttu-id="251ea-159">4</span><span class="sxs-lookup"><span data-stu-id="251ea-159">4</span></span>                | <span data-ttu-id="251ea-160">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="251ea-160">Yes(Contents)</span></span>    | <span data-ttu-id="251ea-161">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-161">None</span></span>     | <span data-ttu-id="251ea-162">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-162">Yes</span></span>          |
| <span data-ttu-id="251ea-163">\[Indice ICB\]</span><span class="sxs-lookup"><span data-stu-id="251ea-163">icb\[index\]</span></span>             |      | <span data-ttu-id="251ea-164">1</span><span class="sxs-lookup"><span data-stu-id="251ea-164">1</span></span>                  | <span data-ttu-id="251ea-165">R</span><span class="sxs-lookup"><span data-stu-id="251ea-165">R</span></span>   | <span data-ttu-id="251ea-166">4</span><span class="sxs-lookup"><span data-stu-id="251ea-166">4</span></span>                | <span data-ttu-id="251ea-167">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="251ea-167">Yes(Contents)</span></span>    | <span data-ttu-id="251ea-168">nessuno</span><span class="sxs-lookup"><span data-stu-id="251ea-168">None</span></span>     | <span data-ttu-id="251ea-169">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="251ea-170">Registri di output</span><span class="sxs-lookup"><span data-stu-id="251ea-170">Output Registers</span></span>



| <span data-ttu-id="251ea-171">Registrazione</span><span class="sxs-lookup"><span data-stu-id="251ea-171">Register</span></span> | <span data-ttu-id="251ea-172">Nome</span><span class="sxs-lookup"><span data-stu-id="251ea-172">Name</span></span>            | <span data-ttu-id="251ea-173">Conteggio</span><span class="sxs-lookup"><span data-stu-id="251ea-173">Count</span></span> | <span data-ttu-id="251ea-174">L/S</span><span class="sxs-lookup"><span data-stu-id="251ea-174">R/W</span></span> | <span data-ttu-id="251ea-175">Dimension</span><span class="sxs-lookup"><span data-stu-id="251ea-175">Dimension</span></span> | <span data-ttu-id="251ea-176">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="251ea-176">Indexable by r\#</span></span> | <span data-ttu-id="251ea-177">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="251ea-177">Defaults</span></span> | <span data-ttu-id="251ea-178">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="251ea-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="251ea-179">NULL</span><span class="sxs-lookup"><span data-stu-id="251ea-179">NULL</span></span>     | <span data-ttu-id="251ea-180">Elimina risultato</span><span class="sxs-lookup"><span data-stu-id="251ea-180">Discard Result</span></span>  | <span data-ttu-id="251ea-181">N/D</span><span class="sxs-lookup"><span data-stu-id="251ea-181">N/A</span></span>   | <span data-ttu-id="251ea-182">W</span><span class="sxs-lookup"><span data-stu-id="251ea-182">W</span></span>   | <span data-ttu-id="251ea-183">N/D</span><span class="sxs-lookup"><span data-stu-id="251ea-183">N/A</span></span>       | <span data-ttu-id="251ea-184">N/D</span><span class="sxs-lookup"><span data-stu-id="251ea-184">N/A</span></span>              | <span data-ttu-id="251ea-185">N/D</span><span class="sxs-lookup"><span data-stu-id="251ea-185">N/A</span></span>      | <span data-ttu-id="251ea-186">No</span><span class="sxs-lookup"><span data-stu-id="251ea-186">No</span></span>           |
| <span data-ttu-id="251ea-187">o\#</span><span class="sxs-lookup"><span data-stu-id="251ea-187">o\#</span></span>      | <span data-ttu-id="251ea-188">Registro di output</span><span class="sxs-lookup"><span data-stu-id="251ea-188">Output Register</span></span> | <span data-ttu-id="251ea-189">32</span><span class="sxs-lookup"><span data-stu-id="251ea-189">32</span></span>    | <span data-ttu-id="251ea-190">W</span><span class="sxs-lookup"><span data-stu-id="251ea-190">W</span></span>   | <span data-ttu-id="251ea-191">N/D</span><span class="sxs-lookup"><span data-stu-id="251ea-191">N/A</span></span>       | <span data-ttu-id="251ea-192">N/D</span><span class="sxs-lookup"><span data-stu-id="251ea-192">N/A</span></span>              | <span data-ttu-id="251ea-193">4</span><span class="sxs-lookup"><span data-stu-id="251ea-193">4</span></span>        | <span data-ttu-id="251ea-194">Sì</span><span class="sxs-lookup"><span data-stu-id="251ea-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="251ea-195">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="251ea-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="251ea-196">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="251ea-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




