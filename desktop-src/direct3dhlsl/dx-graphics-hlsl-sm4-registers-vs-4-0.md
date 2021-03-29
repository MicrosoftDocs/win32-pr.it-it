---
title: Registri-vs_4_0
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 4 \_ 0.
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992784"
---
# <a name="registers---vs_4_0"></a><span data-ttu-id="7ceb7-103">Registri-vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ceb7-103">Registers - vs\_4\_0</span></span>

<span data-ttu-id="7ceb7-104">Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="7ceb7-105">Registri di input</span><span class="sxs-lookup"><span data-stu-id="7ceb7-105">Input Registers</span></span>



| <span data-ttu-id="7ceb7-106">Registrazione</span><span class="sxs-lookup"><span data-stu-id="7ceb7-106">Register</span></span>      | <span data-ttu-id="7ceb7-107">Nome</span><span class="sxs-lookup"><span data-stu-id="7ceb7-107">Name</span></span> | <span data-ttu-id="7ceb7-108">Conteggio</span><span class="sxs-lookup"><span data-stu-id="7ceb7-108">Count</span></span>              | <span data-ttu-id="7ceb7-109">L/S</span><span class="sxs-lookup"><span data-stu-id="7ceb7-109">R/W</span></span> | <span data-ttu-id="7ceb7-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="7ceb7-110">Dimension</span></span> | <span data-ttu-id="7ceb7-111">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="7ceb7-111">Indexable by r\#</span></span> | <span data-ttu-id="7ceb7-112">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="7ceb7-112">Defaults</span></span> | <span data-ttu-id="7ceb7-113">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="7ceb7-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="7ceb7-114">r\#</span><span class="sxs-lookup"><span data-stu-id="7ceb7-114">r\#</span></span>           |      | <span data-ttu-id="7ceb7-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="7ceb7-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="7ceb7-116">L/S</span><span class="sxs-lookup"><span data-stu-id="7ceb7-116">R/W</span></span> | <span data-ttu-id="7ceb7-117">4</span><span class="sxs-lookup"><span data-stu-id="7ceb7-117">4</span></span>         | <span data-ttu-id="7ceb7-118">No</span><span class="sxs-lookup"><span data-stu-id="7ceb7-118">No</span></span>               | <span data-ttu-id="7ceb7-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="7ceb7-119">None</span></span>     | <span data-ttu-id="7ceb7-120">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-120">Yes</span></span>          |
| <span data-ttu-id="7ceb7-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="7ceb7-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="7ceb7-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="7ceb7-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="7ceb7-123">L/S</span><span class="sxs-lookup"><span data-stu-id="7ceb7-123">R/W</span></span> | <span data-ttu-id="7ceb7-124">4</span><span class="sxs-lookup"><span data-stu-id="7ceb7-124">4</span></span>         | <span data-ttu-id="7ceb7-125">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-125">Yes</span></span>              | <span data-ttu-id="7ceb7-126">nessuno</span><span class="sxs-lookup"><span data-stu-id="7ceb7-126">None</span></span>     | <span data-ttu-id="7ceb7-127">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-127">Yes</span></span>          |
| <span data-ttu-id="7ceb7-128">v\#</span><span class="sxs-lookup"><span data-stu-id="7ceb7-128">v\#</span></span>           |      | <span data-ttu-id="7ceb7-129">16</span><span class="sxs-lookup"><span data-stu-id="7ceb7-129">16</span></span>                 | <span data-ttu-id="7ceb7-130">R</span><span class="sxs-lookup"><span data-stu-id="7ceb7-130">R</span></span>   | <span data-ttu-id="7ceb7-131">4</span><span class="sxs-lookup"><span data-stu-id="7ceb7-131">4</span></span>         | <span data-ttu-id="7ceb7-132">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-132">Yes</span></span>              | <span data-ttu-id="7ceb7-133">nessuno</span><span class="sxs-lookup"><span data-stu-id="7ceb7-133">None</span></span>     | <span data-ttu-id="7ceb7-134">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-134">Yes</span></span>          |
| <span data-ttu-id="7ceb7-135">t\#</span><span class="sxs-lookup"><span data-stu-id="7ceb7-135">t\#</span></span>           |      | <span data-ttu-id="7ceb7-136">128</span><span class="sxs-lookup"><span data-stu-id="7ceb7-136">128</span></span>                | <span data-ttu-id="7ceb7-137">R</span><span class="sxs-lookup"><span data-stu-id="7ceb7-137">R</span></span>   | <span data-ttu-id="7ceb7-138">1</span><span class="sxs-lookup"><span data-stu-id="7ceb7-138">1</span></span>         | <span data-ttu-id="7ceb7-139">No</span><span class="sxs-lookup"><span data-stu-id="7ceb7-139">No</span></span>               | <span data-ttu-id="7ceb7-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="7ceb7-140">None</span></span>     | <span data-ttu-id="7ceb7-141">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-141">Yes</span></span>          |
| <span data-ttu-id="7ceb7-142">s\#</span><span class="sxs-lookup"><span data-stu-id="7ceb7-142">s\#</span></span>           |      | <span data-ttu-id="7ceb7-143">16</span><span class="sxs-lookup"><span data-stu-id="7ceb7-143">16</span></span>                 | <span data-ttu-id="7ceb7-144">R</span><span class="sxs-lookup"><span data-stu-id="7ceb7-144">R</span></span>   | <span data-ttu-id="7ceb7-145">1</span><span class="sxs-lookup"><span data-stu-id="7ceb7-145">1</span></span>         | <span data-ttu-id="7ceb7-146">No</span><span class="sxs-lookup"><span data-stu-id="7ceb7-146">No</span></span>               | <span data-ttu-id="7ceb7-147">nessuno</span><span class="sxs-lookup"><span data-stu-id="7ceb7-147">None</span></span>     | <span data-ttu-id="7ceb7-148">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-148">Yes</span></span>          |
| <span data-ttu-id="7ceb7-149">\# \[ Indice CB\]</span><span class="sxs-lookup"><span data-stu-id="7ceb7-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="7ceb7-150">15</span><span class="sxs-lookup"><span data-stu-id="7ceb7-150">15</span></span>                 | <span data-ttu-id="7ceb7-151">R</span><span class="sxs-lookup"><span data-stu-id="7ceb7-151">R</span></span>   | <span data-ttu-id="7ceb7-152">4</span><span class="sxs-lookup"><span data-stu-id="7ceb7-152">4</span></span>         | <span data-ttu-id="7ceb7-153">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="7ceb7-153">Yes(Contents)</span></span>    | <span data-ttu-id="7ceb7-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="7ceb7-154">None</span></span>     | <span data-ttu-id="7ceb7-155">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-155">Yes</span></span>          |
| <span data-ttu-id="7ceb7-156">\[Indice ICB\]</span><span class="sxs-lookup"><span data-stu-id="7ceb7-156">icb\[index\]</span></span>  |      | <span data-ttu-id="7ceb7-157">1</span><span class="sxs-lookup"><span data-stu-id="7ceb7-157">1</span></span>                  | <span data-ttu-id="7ceb7-158">R</span><span class="sxs-lookup"><span data-stu-id="7ceb7-158">R</span></span>   | <span data-ttu-id="7ceb7-159">4</span><span class="sxs-lookup"><span data-stu-id="7ceb7-159">4</span></span>         | <span data-ttu-id="7ceb7-160">Sì (contenuto)</span><span class="sxs-lookup"><span data-stu-id="7ceb7-160">Yes(Contents)</span></span>    | <span data-ttu-id="7ceb7-161">nessuno</span><span class="sxs-lookup"><span data-stu-id="7ceb7-161">None</span></span>     | <span data-ttu-id="7ceb7-162">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="7ceb7-163">Registri di output</span><span class="sxs-lookup"><span data-stu-id="7ceb7-163">Output Registers</span></span>



| <span data-ttu-id="7ceb7-164">Registrazione</span><span class="sxs-lookup"><span data-stu-id="7ceb7-164">Register</span></span> | <span data-ttu-id="7ceb7-165">Nome</span><span class="sxs-lookup"><span data-stu-id="7ceb7-165">Name</span></span>            | <span data-ttu-id="7ceb7-166">Conteggio</span><span class="sxs-lookup"><span data-stu-id="7ceb7-166">Count</span></span> | <span data-ttu-id="7ceb7-167">L/S</span><span class="sxs-lookup"><span data-stu-id="7ceb7-167">R/W</span></span> | <span data-ttu-id="7ceb7-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="7ceb7-168">Dimension</span></span> | <span data-ttu-id="7ceb7-169">Indicizzabile da r\#</span><span class="sxs-lookup"><span data-stu-id="7ceb7-169">Indexable by r\#</span></span> | <span data-ttu-id="7ceb7-170">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="7ceb7-170">Defaults</span></span> | <span data-ttu-id="7ceb7-171">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="7ceb7-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="7ceb7-172">NULL</span><span class="sxs-lookup"><span data-stu-id="7ceb7-172">NULL</span></span>     | <span data-ttu-id="7ceb7-173">Elimina risultato</span><span class="sxs-lookup"><span data-stu-id="7ceb7-173">Discard Result</span></span>  | <span data-ttu-id="7ceb7-174">N/D</span><span class="sxs-lookup"><span data-stu-id="7ceb7-174">N/A</span></span>   | <span data-ttu-id="7ceb7-175">W</span><span class="sxs-lookup"><span data-stu-id="7ceb7-175">W</span></span>   | <span data-ttu-id="7ceb7-176">N/D</span><span class="sxs-lookup"><span data-stu-id="7ceb7-176">N/A</span></span>       | <span data-ttu-id="7ceb7-177">N/D</span><span class="sxs-lookup"><span data-stu-id="7ceb7-177">N/A</span></span>              | <span data-ttu-id="7ceb7-178">N/D</span><span class="sxs-lookup"><span data-stu-id="7ceb7-178">N/A</span></span>      | <span data-ttu-id="7ceb7-179">No</span><span class="sxs-lookup"><span data-stu-id="7ceb7-179">No</span></span>           |
| <span data-ttu-id="7ceb7-180">o\#</span><span class="sxs-lookup"><span data-stu-id="7ceb7-180">o\#</span></span>      | <span data-ttu-id="7ceb7-181">Registro di output</span><span class="sxs-lookup"><span data-stu-id="7ceb7-181">Output Register</span></span> | <span data-ttu-id="7ceb7-182">16</span><span class="sxs-lookup"><span data-stu-id="7ceb7-182">16</span></span>    | <span data-ttu-id="7ceb7-183">W</span><span class="sxs-lookup"><span data-stu-id="7ceb7-183">W</span></span>   | <span data-ttu-id="7ceb7-184">N/D</span><span class="sxs-lookup"><span data-stu-id="7ceb7-184">N/A</span></span>       | <span data-ttu-id="7ceb7-185">N/D</span><span class="sxs-lookup"><span data-stu-id="7ceb7-185">N/A</span></span>              | <span data-ttu-id="7ceb7-186">4</span><span class="sxs-lookup"><span data-stu-id="7ceb7-186">4</span></span>        | <span data-ttu-id="7ceb7-187">Sì</span><span class="sxs-lookup"><span data-stu-id="7ceb7-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="7ceb7-188">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ceb7-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ceb7-189">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7ceb7-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




