---
title: Registri-vs_4_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 4 \_ 1.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221615"
---
# <a name="registers---vs_4_1"></a><span data-ttu-id="7f7c0-103">Registri-vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7f7c0-103">Registers - vs\_4\_1</span></span>

<span data-ttu-id="7f7c0-104">Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="7f7c0-105">Registri di input</span><span class="sxs-lookup"><span data-stu-id="7f7c0-105">Input Registers</span></span>



| <span data-ttu-id="7f7c0-106">Registrazione</span><span class="sxs-lookup"><span data-stu-id="7f7c0-106">Register</span></span>      | <span data-ttu-id="7f7c0-107">Nome</span><span class="sxs-lookup"><span data-stu-id="7f7c0-107">Name</span></span> | <span data-ttu-id="7f7c0-108">Conteggio</span><span class="sxs-lookup"><span data-stu-id="7f7c0-108">Count</span></span>              | <span data-ttu-id="7f7c0-109">L/S</span><span class="sxs-lookup"><span data-stu-id="7f7c0-109">R/W</span></span> | <span data-ttu-id="7f7c0-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="7f7c0-110">Dimension</span></span> | <span data-ttu-id="7f7c0-111">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="7f7c0-111">Indexable by r\#</span></span> | <span data-ttu-id="7f7c0-112">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="7f7c0-112">Defaults</span></span> | <span data-ttu-id="7f7c0-113">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="7f7c0-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="7f7c0-114">r\#</span><span class="sxs-lookup"><span data-stu-id="7f7c0-114">r\#</span></span>           |      | <span data-ttu-id="7f7c0-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="7f7c0-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="7f7c0-116">L/S</span><span class="sxs-lookup"><span data-stu-id="7f7c0-116">R/W</span></span> | <span data-ttu-id="7f7c0-117">4</span><span class="sxs-lookup"><span data-stu-id="7f7c0-117">4</span></span>         | <span data-ttu-id="7f7c0-118">No</span><span class="sxs-lookup"><span data-stu-id="7f7c0-118">No</span></span>               | <span data-ttu-id="7f7c0-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-119">None</span></span>     | <span data-ttu-id="7f7c0-120">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-120">Yes</span></span>          |
| <span data-ttu-id="7f7c0-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="7f7c0-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="7f7c0-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="7f7c0-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="7f7c0-123">L/S</span><span class="sxs-lookup"><span data-stu-id="7f7c0-123">R/W</span></span> | <span data-ttu-id="7f7c0-124">4</span><span class="sxs-lookup"><span data-stu-id="7f7c0-124">4</span></span>         | <span data-ttu-id="7f7c0-125">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-125">Yes</span></span>              | <span data-ttu-id="7f7c0-126">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-126">None</span></span>     | <span data-ttu-id="7f7c0-127">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-127">Yes</span></span>          |
| <span data-ttu-id="7f7c0-128">v\#</span><span class="sxs-lookup"><span data-stu-id="7f7c0-128">v\#</span></span>           |      | <span data-ttu-id="7f7c0-129">32</span><span class="sxs-lookup"><span data-stu-id="7f7c0-129">32</span></span>                 | <span data-ttu-id="7f7c0-130">R</span><span class="sxs-lookup"><span data-stu-id="7f7c0-130">R</span></span>   | <span data-ttu-id="7f7c0-131">4</span><span class="sxs-lookup"><span data-stu-id="7f7c0-131">4</span></span>         | <span data-ttu-id="7f7c0-132">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-132">Yes</span></span>              | <span data-ttu-id="7f7c0-133">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-133">None</span></span>     | <span data-ttu-id="7f7c0-134">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-134">Yes</span></span>          |
| <span data-ttu-id="7f7c0-135">t\#</span><span class="sxs-lookup"><span data-stu-id="7f7c0-135">t\#</span></span>           |      | <span data-ttu-id="7f7c0-136">128</span><span class="sxs-lookup"><span data-stu-id="7f7c0-136">128</span></span>                | <span data-ttu-id="7f7c0-137">R</span><span class="sxs-lookup"><span data-stu-id="7f7c0-137">R</span></span>   | <span data-ttu-id="7f7c0-138">1</span><span class="sxs-lookup"><span data-stu-id="7f7c0-138">1</span></span>         | <span data-ttu-id="7f7c0-139">No</span><span class="sxs-lookup"><span data-stu-id="7f7c0-139">No</span></span>               | <span data-ttu-id="7f7c0-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-140">None</span></span>     | <span data-ttu-id="7f7c0-141">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-141">Yes</span></span>          |
| <span data-ttu-id="7f7c0-142">s\#</span><span class="sxs-lookup"><span data-stu-id="7f7c0-142">s\#</span></span>           |      | <span data-ttu-id="7f7c0-143">16</span><span class="sxs-lookup"><span data-stu-id="7f7c0-143">16</span></span>                 | <span data-ttu-id="7f7c0-144">R</span><span class="sxs-lookup"><span data-stu-id="7f7c0-144">R</span></span>   | <span data-ttu-id="7f7c0-145">1</span><span class="sxs-lookup"><span data-stu-id="7f7c0-145">1</span></span>         | <span data-ttu-id="7f7c0-146">No</span><span class="sxs-lookup"><span data-stu-id="7f7c0-146">No</span></span>               | <span data-ttu-id="7f7c0-147">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-147">None</span></span>     | <span data-ttu-id="7f7c0-148">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-148">Yes</span></span>          |
| <span data-ttu-id="7f7c0-149">\# \[ Indice CB\]</span><span class="sxs-lookup"><span data-stu-id="7f7c0-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="7f7c0-150">15</span><span class="sxs-lookup"><span data-stu-id="7f7c0-150">15</span></span>                 | <span data-ttu-id="7f7c0-151">R</span><span class="sxs-lookup"><span data-stu-id="7f7c0-151">R</span></span>   | <span data-ttu-id="7f7c0-152">4</span><span class="sxs-lookup"><span data-stu-id="7f7c0-152">4</span></span>         | <span data-ttu-id="7f7c0-153">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="7f7c0-153">Yes(Contents)</span></span>    | <span data-ttu-id="7f7c0-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-154">None</span></span>     | <span data-ttu-id="7f7c0-155">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-155">Yes</span></span>          |
| <span data-ttu-id="7f7c0-156">\[Indice ICB\]</span><span class="sxs-lookup"><span data-stu-id="7f7c0-156">icb\[index\]</span></span>  |      | <span data-ttu-id="7f7c0-157">1</span><span class="sxs-lookup"><span data-stu-id="7f7c0-157">1</span></span>                  | <span data-ttu-id="7f7c0-158">R</span><span class="sxs-lookup"><span data-stu-id="7f7c0-158">R</span></span>   | <span data-ttu-id="7f7c0-159">4</span><span class="sxs-lookup"><span data-stu-id="7f7c0-159">4</span></span>         | <span data-ttu-id="7f7c0-160">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="7f7c0-160">Yes(Contents)</span></span>    | <span data-ttu-id="7f7c0-161">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-161">None</span></span>     | <span data-ttu-id="7f7c0-162">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="7f7c0-163">Registri di output</span><span class="sxs-lookup"><span data-stu-id="7f7c0-163">Output Registers</span></span>



| <span data-ttu-id="7f7c0-164">Registrazione</span><span class="sxs-lookup"><span data-stu-id="7f7c0-164">Register</span></span> | <span data-ttu-id="7f7c0-165">Nome</span><span class="sxs-lookup"><span data-stu-id="7f7c0-165">Name</span></span>            | <span data-ttu-id="7f7c0-166">Conteggio</span><span class="sxs-lookup"><span data-stu-id="7f7c0-166">Count</span></span> | <span data-ttu-id="7f7c0-167">L/S</span><span class="sxs-lookup"><span data-stu-id="7f7c0-167">R/W</span></span> | <span data-ttu-id="7f7c0-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="7f7c0-168">Dimension</span></span> | <span data-ttu-id="7f7c0-169">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="7f7c0-169">Indexable by r\#</span></span> | <span data-ttu-id="7f7c0-170">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="7f7c0-170">Defaults</span></span> | <span data-ttu-id="7f7c0-171">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="7f7c0-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="7f7c0-172">NULL</span><span class="sxs-lookup"><span data-stu-id="7f7c0-172">NULL</span></span>     | <span data-ttu-id="7f7c0-173">Elimina risultato</span><span class="sxs-lookup"><span data-stu-id="7f7c0-173">Discard Result</span></span>  | <span data-ttu-id="7f7c0-174">N/D</span><span class="sxs-lookup"><span data-stu-id="7f7c0-174">N/A</span></span>   | <span data-ttu-id="7f7c0-175">W</span><span class="sxs-lookup"><span data-stu-id="7f7c0-175">W</span></span>   | <span data-ttu-id="7f7c0-176">N/D</span><span class="sxs-lookup"><span data-stu-id="7f7c0-176">N/A</span></span>       | <span data-ttu-id="7f7c0-177">N/D</span><span class="sxs-lookup"><span data-stu-id="7f7c0-177">N/A</span></span>              | <span data-ttu-id="7f7c0-178">N/D</span><span class="sxs-lookup"><span data-stu-id="7f7c0-178">N/A</span></span>      | <span data-ttu-id="7f7c0-179">No</span><span class="sxs-lookup"><span data-stu-id="7f7c0-179">No</span></span>           |
| <span data-ttu-id="7f7c0-180">o\#</span><span class="sxs-lookup"><span data-stu-id="7f7c0-180">o\#</span></span>      | <span data-ttu-id="7f7c0-181">Registro di output</span><span class="sxs-lookup"><span data-stu-id="7f7c0-181">Output Register</span></span> | <span data-ttu-id="7f7c0-182">32</span><span class="sxs-lookup"><span data-stu-id="7f7c0-182">32</span></span>    | <span data-ttu-id="7f7c0-183">W</span><span class="sxs-lookup"><span data-stu-id="7f7c0-183">W</span></span>   | <span data-ttu-id="7f7c0-184">N/D</span><span class="sxs-lookup"><span data-stu-id="7f7c0-184">N/A</span></span>       | <span data-ttu-id="7f7c0-185">N/D</span><span class="sxs-lookup"><span data-stu-id="7f7c0-185">N/A</span></span>              | <span data-ttu-id="7f7c0-186">4</span><span class="sxs-lookup"><span data-stu-id="7f7c0-186">4</span></span>        | <span data-ttu-id="7f7c0-187">Sì</span><span class="sxs-lookup"><span data-stu-id="7f7c0-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="7f7c0-188">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f7c0-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f7c0-189">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7f7c0-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




