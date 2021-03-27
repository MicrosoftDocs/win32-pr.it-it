---
title: Registri-gs_4_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da Geometry shader versioni 4 \_ 0 e 4 \_ 1.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221616"
---
# <a name="registers---gs_4_1"></a><span data-ttu-id="65a85-103">Registri-GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="65a85-103">Registers - gs\_4\_1</span></span>

<span data-ttu-id="65a85-104">Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da Geometry shader versioni 4 \_ 0 e 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="65a85-104">This section contains reference information for the input and output registers implemented by geometry shader versions 4\_0 and 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="65a85-105">Registri di input</span><span class="sxs-lookup"><span data-stu-id="65a85-105">Input Registers</span></span>



| <span data-ttu-id="65a85-106">Registrazione</span><span class="sxs-lookup"><span data-stu-id="65a85-106">Register</span></span>                 | <span data-ttu-id="65a85-107">Nome</span><span class="sxs-lookup"><span data-stu-id="65a85-107">Name</span></span> | <span data-ttu-id="65a85-108">Conteggio</span><span class="sxs-lookup"><span data-stu-id="65a85-108">Count</span></span>              | <span data-ttu-id="65a85-109">L/S</span><span class="sxs-lookup"><span data-stu-id="65a85-109">R/W</span></span> | <span data-ttu-id="65a85-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="65a85-110">Dimension</span></span>        | <span data-ttu-id="65a85-111">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="65a85-111">Indexable by r\#</span></span> | <span data-ttu-id="65a85-112">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="65a85-112">Defaults</span></span> | <span data-ttu-id="65a85-113">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="65a85-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="65a85-114">r\#</span><span class="sxs-lookup"><span data-stu-id="65a85-114">r\#</span></span>                      |      | <span data-ttu-id="65a85-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="65a85-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="65a85-116">L/S</span><span class="sxs-lookup"><span data-stu-id="65a85-116">R/W</span></span> | <span data-ttu-id="65a85-117">4</span><span class="sxs-lookup"><span data-stu-id="65a85-117">4</span></span>                | <span data-ttu-id="65a85-118">No</span><span class="sxs-lookup"><span data-stu-id="65a85-118">No</span></span>               | <span data-ttu-id="65a85-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-119">None</span></span>     | <span data-ttu-id="65a85-120">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-120">Yes</span></span>          |
| <span data-ttu-id="65a85-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="65a85-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="65a85-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="65a85-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="65a85-123">L/S</span><span class="sxs-lookup"><span data-stu-id="65a85-123">R/W</span></span> | <span data-ttu-id="65a85-124">4</span><span class="sxs-lookup"><span data-stu-id="65a85-124">4</span></span>                | <span data-ttu-id="65a85-125">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-125">Yes</span></span>              | <span data-ttu-id="65a85-126">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-126">None</span></span>     | <span data-ttu-id="65a85-127">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-127">Yes</span></span>          |
| <span data-ttu-id="65a85-128">v ( \# \[ \] \[ elemento Vertex)\]</span><span class="sxs-lookup"><span data-stu-id="65a85-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="65a85-129">32</span><span class="sxs-lookup"><span data-stu-id="65a85-129">32</span></span>                 | <span data-ttu-id="65a85-130">R</span><span class="sxs-lookup"><span data-stu-id="65a85-130">R</span></span>   | <span data-ttu-id="65a85-131">4 (comp) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="65a85-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="65a85-132">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-132">Yes</span></span>              | <span data-ttu-id="65a85-133">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-133">None</span></span>     | <span data-ttu-id="65a85-134">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-134">Yes</span></span>          |
| <span data-ttu-id="65a85-135">vprim</span><span class="sxs-lookup"><span data-stu-id="65a85-135">vprim</span></span>                    |      | <span data-ttu-id="65a85-136">1</span><span class="sxs-lookup"><span data-stu-id="65a85-136">1</span></span>                  | <span data-ttu-id="65a85-137">R</span><span class="sxs-lookup"><span data-stu-id="65a85-137">R</span></span>   | <span data-ttu-id="65a85-138">1</span><span class="sxs-lookup"><span data-stu-id="65a85-138">1</span></span>                | <span data-ttu-id="65a85-139">No</span><span class="sxs-lookup"><span data-stu-id="65a85-139">No</span></span>               | <span data-ttu-id="65a85-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-140">None</span></span>     | <span data-ttu-id="65a85-141">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-141">Yes</span></span>          |
| <span data-ttu-id="65a85-142">t\#</span><span class="sxs-lookup"><span data-stu-id="65a85-142">t\#</span></span>                      |      | <span data-ttu-id="65a85-143">128</span><span class="sxs-lookup"><span data-stu-id="65a85-143">128</span></span>                | <span data-ttu-id="65a85-144">R</span><span class="sxs-lookup"><span data-stu-id="65a85-144">R</span></span>   | <span data-ttu-id="65a85-145">1</span><span class="sxs-lookup"><span data-stu-id="65a85-145">1</span></span>                | <span data-ttu-id="65a85-146">No</span><span class="sxs-lookup"><span data-stu-id="65a85-146">No</span></span>               | <span data-ttu-id="65a85-147">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-147">None</span></span>     | <span data-ttu-id="65a85-148">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-148">Yes</span></span>          |
| <span data-ttu-id="65a85-149">s\#</span><span class="sxs-lookup"><span data-stu-id="65a85-149">s\#</span></span>                      |      | <span data-ttu-id="65a85-150">16</span><span class="sxs-lookup"><span data-stu-id="65a85-150">16</span></span>                 | <span data-ttu-id="65a85-151">R</span><span class="sxs-lookup"><span data-stu-id="65a85-151">R</span></span>   | <span data-ttu-id="65a85-152">1</span><span class="sxs-lookup"><span data-stu-id="65a85-152">1</span></span>                | <span data-ttu-id="65a85-153">No</span><span class="sxs-lookup"><span data-stu-id="65a85-153">No</span></span>               | <span data-ttu-id="65a85-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-154">None</span></span>     | <span data-ttu-id="65a85-155">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-155">Yes</span></span>          |
| <span data-ttu-id="65a85-156">\# \[ Indice CB\]</span><span class="sxs-lookup"><span data-stu-id="65a85-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="65a85-157">15</span><span class="sxs-lookup"><span data-stu-id="65a85-157">15</span></span>                 | <span data-ttu-id="65a85-158">R</span><span class="sxs-lookup"><span data-stu-id="65a85-158">R</span></span>   | <span data-ttu-id="65a85-159">4</span><span class="sxs-lookup"><span data-stu-id="65a85-159">4</span></span>                | <span data-ttu-id="65a85-160">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="65a85-160">Yes(Contents)</span></span>    | <span data-ttu-id="65a85-161">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-161">None</span></span>     | <span data-ttu-id="65a85-162">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-162">Yes</span></span>          |
| <span data-ttu-id="65a85-163">\[Indice ICB\]</span><span class="sxs-lookup"><span data-stu-id="65a85-163">icb\[index\]</span></span>             |      | <span data-ttu-id="65a85-164">1</span><span class="sxs-lookup"><span data-stu-id="65a85-164">1</span></span>                  | <span data-ttu-id="65a85-165">R</span><span class="sxs-lookup"><span data-stu-id="65a85-165">R</span></span>   | <span data-ttu-id="65a85-166">4</span><span class="sxs-lookup"><span data-stu-id="65a85-166">4</span></span>                | <span data-ttu-id="65a85-167">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="65a85-167">Yes(Contents)</span></span>    | <span data-ttu-id="65a85-168">nessuno</span><span class="sxs-lookup"><span data-stu-id="65a85-168">None</span></span>     | <span data-ttu-id="65a85-169">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="65a85-170">Registri di output</span><span class="sxs-lookup"><span data-stu-id="65a85-170">Output Registers</span></span>



| <span data-ttu-id="65a85-171">Registrazione</span><span class="sxs-lookup"><span data-stu-id="65a85-171">Register</span></span> | <span data-ttu-id="65a85-172">Nome</span><span class="sxs-lookup"><span data-stu-id="65a85-172">Name</span></span>            | <span data-ttu-id="65a85-173">Conteggio</span><span class="sxs-lookup"><span data-stu-id="65a85-173">Count</span></span> | <span data-ttu-id="65a85-174">L/S</span><span class="sxs-lookup"><span data-stu-id="65a85-174">R/W</span></span> | <span data-ttu-id="65a85-175">Dimension</span><span class="sxs-lookup"><span data-stu-id="65a85-175">Dimension</span></span> | <span data-ttu-id="65a85-176">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="65a85-176">Indexable by r\#</span></span> | <span data-ttu-id="65a85-177">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="65a85-177">Defaults</span></span> | <span data-ttu-id="65a85-178">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="65a85-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="65a85-179">NULL</span><span class="sxs-lookup"><span data-stu-id="65a85-179">NULL</span></span>     | <span data-ttu-id="65a85-180">Elimina risultato</span><span class="sxs-lookup"><span data-stu-id="65a85-180">Discard Result</span></span>  | <span data-ttu-id="65a85-181">N/D</span><span class="sxs-lookup"><span data-stu-id="65a85-181">N/A</span></span>   | <span data-ttu-id="65a85-182">W</span><span class="sxs-lookup"><span data-stu-id="65a85-182">W</span></span>   | <span data-ttu-id="65a85-183">N/D</span><span class="sxs-lookup"><span data-stu-id="65a85-183">N/A</span></span>       | <span data-ttu-id="65a85-184">N/D</span><span class="sxs-lookup"><span data-stu-id="65a85-184">N/A</span></span>              | <span data-ttu-id="65a85-185">N/D</span><span class="sxs-lookup"><span data-stu-id="65a85-185">N/A</span></span>      | <span data-ttu-id="65a85-186">No</span><span class="sxs-lookup"><span data-stu-id="65a85-186">No</span></span>           |
| <span data-ttu-id="65a85-187">o\#</span><span class="sxs-lookup"><span data-stu-id="65a85-187">o\#</span></span>      | <span data-ttu-id="65a85-188">Registro di output</span><span class="sxs-lookup"><span data-stu-id="65a85-188">Output Register</span></span> | <span data-ttu-id="65a85-189">32</span><span class="sxs-lookup"><span data-stu-id="65a85-189">32</span></span>    | <span data-ttu-id="65a85-190">W</span><span class="sxs-lookup"><span data-stu-id="65a85-190">W</span></span>   | <span data-ttu-id="65a85-191">N/D</span><span class="sxs-lookup"><span data-stu-id="65a85-191">N/A</span></span>       | <span data-ttu-id="65a85-192">N/D</span><span class="sxs-lookup"><span data-stu-id="65a85-192">N/A</span></span>              | <span data-ttu-id="65a85-193">4</span><span class="sxs-lookup"><span data-stu-id="65a85-193">4</span></span>        | <span data-ttu-id="65a85-194">Sì</span><span class="sxs-lookup"><span data-stu-id="65a85-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="65a85-195">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65a85-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65a85-196">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="65a85-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




