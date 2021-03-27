---
title: Registri-ps_4_0
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da pixel shader versione 4 \_ 0.
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396094"
---
# <a name="registers---ps_4_0"></a><span data-ttu-id="d3164-103">Registri-PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d3164-103">Registers - ps\_4\_0</span></span>

<span data-ttu-id="d3164-104">Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da pixel shader versione 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="d3164-104">This section contains reference information for the input and output registers implemented by pixel shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="d3164-105">Registri di input</span><span class="sxs-lookup"><span data-stu-id="d3164-105">Input Registers</span></span>



| <span data-ttu-id="d3164-106">Registrazione</span><span class="sxs-lookup"><span data-stu-id="d3164-106">Register</span></span>      | <span data-ttu-id="d3164-107">Nome</span><span class="sxs-lookup"><span data-stu-id="d3164-107">Name</span></span> | <span data-ttu-id="d3164-108">Conteggio</span><span class="sxs-lookup"><span data-stu-id="d3164-108">Count</span></span>              | <span data-ttu-id="d3164-109">L/S</span><span class="sxs-lookup"><span data-stu-id="d3164-109">R/W</span></span> | <span data-ttu-id="d3164-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="d3164-110">Dimension</span></span> | <span data-ttu-id="d3164-111">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="d3164-111">Indexable by r\#</span></span> | <span data-ttu-id="d3164-112">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="d3164-112">Defaults</span></span> | <span data-ttu-id="d3164-113">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="d3164-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="d3164-114">r\#</span><span class="sxs-lookup"><span data-stu-id="d3164-114">r\#</span></span>           |      | <span data-ttu-id="d3164-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="d3164-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="d3164-116">L/S</span><span class="sxs-lookup"><span data-stu-id="d3164-116">R/W</span></span> | <span data-ttu-id="d3164-117">4</span><span class="sxs-lookup"><span data-stu-id="d3164-117">4</span></span>         | <span data-ttu-id="d3164-118">No</span><span class="sxs-lookup"><span data-stu-id="d3164-118">No</span></span>               | <span data-ttu-id="d3164-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="d3164-119">None</span></span>     | <span data-ttu-id="d3164-120">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-120">Yes</span></span>          |
| <span data-ttu-id="d3164-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="d3164-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="d3164-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="d3164-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="d3164-123">L/S</span><span class="sxs-lookup"><span data-stu-id="d3164-123">R/W</span></span> | <span data-ttu-id="d3164-124">4</span><span class="sxs-lookup"><span data-stu-id="d3164-124">4</span></span>         | <span data-ttu-id="d3164-125">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-125">Yes</span></span>              | <span data-ttu-id="d3164-126">nessuno</span><span class="sxs-lookup"><span data-stu-id="d3164-126">None</span></span>     | <span data-ttu-id="d3164-127">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-127">Yes</span></span>          |
| <span data-ttu-id="d3164-128">v\#</span><span class="sxs-lookup"><span data-stu-id="d3164-128">v\#</span></span>           |      | <span data-ttu-id="d3164-129">32</span><span class="sxs-lookup"><span data-stu-id="d3164-129">32</span></span>                 | <span data-ttu-id="d3164-130">R</span><span class="sxs-lookup"><span data-stu-id="d3164-130">R</span></span>   | <span data-ttu-id="d3164-131">4</span><span class="sxs-lookup"><span data-stu-id="d3164-131">4</span></span>         | <span data-ttu-id="d3164-132">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-132">Yes</span></span>              | <span data-ttu-id="d3164-133">nessuno</span><span class="sxs-lookup"><span data-stu-id="d3164-133">None</span></span>     | <span data-ttu-id="d3164-134">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-134">Yes</span></span>          |
| <span data-ttu-id="d3164-135">t\#</span><span class="sxs-lookup"><span data-stu-id="d3164-135">t\#</span></span>           |      | <span data-ttu-id="d3164-136">128</span><span class="sxs-lookup"><span data-stu-id="d3164-136">128</span></span>                | <span data-ttu-id="d3164-137">R</span><span class="sxs-lookup"><span data-stu-id="d3164-137">R</span></span>   | <span data-ttu-id="d3164-138">1</span><span class="sxs-lookup"><span data-stu-id="d3164-138">1</span></span>         | <span data-ttu-id="d3164-139">No</span><span class="sxs-lookup"><span data-stu-id="d3164-139">No</span></span>               | <span data-ttu-id="d3164-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="d3164-140">None</span></span>     | <span data-ttu-id="d3164-141">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-141">Yes</span></span>          |
| <span data-ttu-id="d3164-142">s\#</span><span class="sxs-lookup"><span data-stu-id="d3164-142">s\#</span></span>           |      | <span data-ttu-id="d3164-143">16</span><span class="sxs-lookup"><span data-stu-id="d3164-143">16</span></span>                 | <span data-ttu-id="d3164-144">R</span><span class="sxs-lookup"><span data-stu-id="d3164-144">R</span></span>   | <span data-ttu-id="d3164-145">1</span><span class="sxs-lookup"><span data-stu-id="d3164-145">1</span></span>         | <span data-ttu-id="d3164-146">No</span><span class="sxs-lookup"><span data-stu-id="d3164-146">No</span></span>               | <span data-ttu-id="d3164-147">nessuno</span><span class="sxs-lookup"><span data-stu-id="d3164-147">None</span></span>     | <span data-ttu-id="d3164-148">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-148">Yes</span></span>          |
| <span data-ttu-id="d3164-149">\# \[ Indice CB\]</span><span class="sxs-lookup"><span data-stu-id="d3164-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="d3164-150">15</span><span class="sxs-lookup"><span data-stu-id="d3164-150">15</span></span>                 | <span data-ttu-id="d3164-151">R</span><span class="sxs-lookup"><span data-stu-id="d3164-151">R</span></span>   | <span data-ttu-id="d3164-152">4</span><span class="sxs-lookup"><span data-stu-id="d3164-152">4</span></span>         | <span data-ttu-id="d3164-153">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="d3164-153">Yes(Contents)</span></span>    | <span data-ttu-id="d3164-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="d3164-154">None</span></span>     | <span data-ttu-id="d3164-155">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-155">Yes</span></span>          |
| <span data-ttu-id="d3164-156">\[Indice ICB\]</span><span class="sxs-lookup"><span data-stu-id="d3164-156">icb\[index\]</span></span>  |      | <span data-ttu-id="d3164-157">1</span><span class="sxs-lookup"><span data-stu-id="d3164-157">1</span></span>                  | <span data-ttu-id="d3164-158">R</span><span class="sxs-lookup"><span data-stu-id="d3164-158">R</span></span>   | <span data-ttu-id="d3164-159">4</span><span class="sxs-lookup"><span data-stu-id="d3164-159">4</span></span>         | <span data-ttu-id="d3164-160">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="d3164-160">Yes(Contents)</span></span>    | <span data-ttu-id="d3164-161">nessuno</span><span class="sxs-lookup"><span data-stu-id="d3164-161">None</span></span>     | <span data-ttu-id="d3164-162">Sì</span><span class="sxs-lookup"><span data-stu-id="d3164-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="d3164-163">Registri di output</span><span class="sxs-lookup"><span data-stu-id="d3164-163">Output Registers</span></span>



| <span data-ttu-id="d3164-164">Registrazione</span><span class="sxs-lookup"><span data-stu-id="d3164-164">Register</span></span> | <span data-ttu-id="d3164-165">Nome</span><span class="sxs-lookup"><span data-stu-id="d3164-165">Name</span></span>            | <span data-ttu-id="d3164-166">Conteggio</span><span class="sxs-lookup"><span data-stu-id="d3164-166">Count</span></span> | <span data-ttu-id="d3164-167">L/S</span><span class="sxs-lookup"><span data-stu-id="d3164-167">R/W</span></span> | <span data-ttu-id="d3164-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="d3164-168">Dimension</span></span> | <span data-ttu-id="d3164-169">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="d3164-169">Indexable by r\#</span></span> | <span data-ttu-id="d3164-170">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="d3164-170">Defaults</span></span> | <span data-ttu-id="d3164-171">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="d3164-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="d3164-172">NULL</span><span class="sxs-lookup"><span data-stu-id="d3164-172">NULL</span></span>     | <span data-ttu-id="d3164-173">Elimina risultato</span><span class="sxs-lookup"><span data-stu-id="d3164-173">Discard Result</span></span>  | <span data-ttu-id="d3164-174">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-174">N/A</span></span>   | <span data-ttu-id="d3164-175">W</span><span class="sxs-lookup"><span data-stu-id="d3164-175">W</span></span>   | <span data-ttu-id="d3164-176">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-176">N/A</span></span>       | <span data-ttu-id="d3164-177">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-177">N/A</span></span>              | <span data-ttu-id="d3164-178">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-178">N/A</span></span>      | <span data-ttu-id="d3164-179">No</span><span class="sxs-lookup"><span data-stu-id="d3164-179">No</span></span>           |
| <span data-ttu-id="d3164-180">o\#</span><span class="sxs-lookup"><span data-stu-id="d3164-180">o\#</span></span>      | <span data-ttu-id="d3164-181">Registro di output</span><span class="sxs-lookup"><span data-stu-id="d3164-181">Output Register</span></span> | <span data-ttu-id="d3164-182">8</span><span class="sxs-lookup"><span data-stu-id="d3164-182">8</span></span>     | <span data-ttu-id="d3164-183">W</span><span class="sxs-lookup"><span data-stu-id="d3164-183">W</span></span>   | <span data-ttu-id="d3164-184">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-184">N/A</span></span>       | <span data-ttu-id="d3164-185">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-185">N/A</span></span>              | <span data-ttu-id="d3164-186">4</span><span class="sxs-lookup"><span data-stu-id="d3164-186">4</span></span>        | <span data-ttu-id="d3164-187">No</span><span class="sxs-lookup"><span data-stu-id="d3164-187">No</span></span>           |
| <span data-ttu-id="d3164-188">oDepth</span><span class="sxs-lookup"><span data-stu-id="d3164-188">oDepth</span></span>   | <span data-ttu-id="d3164-189">Profondità di output</span><span class="sxs-lookup"><span data-stu-id="d3164-189">Output Depth</span></span>    | <span data-ttu-id="d3164-190">1</span><span class="sxs-lookup"><span data-stu-id="d3164-190">1</span></span>     | <span data-ttu-id="d3164-191">W</span><span class="sxs-lookup"><span data-stu-id="d3164-191">W</span></span>   | <span data-ttu-id="d3164-192">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-192">N/A</span></span>       | <span data-ttu-id="d3164-193">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-193">N/A</span></span>              | <span data-ttu-id="d3164-194">1</span><span class="sxs-lookup"><span data-stu-id="d3164-194">1</span></span>        | <span data-ttu-id="d3164-195">N/D</span><span class="sxs-lookup"><span data-stu-id="d3164-195">N/A</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="d3164-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3164-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3164-197">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="d3164-197">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




