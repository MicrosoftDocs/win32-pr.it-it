---
description: 'Questo esempio illustra il layout di un file con estensione cub contenente due CIEM. Il programma di installazione esegue le azioni personalizzate nella sequenza: ICE01 e ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: File Sample. cub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966637"
---
# <a name="sample-cub-file"></a><span data-ttu-id="5055e-104">File Sample. cub</span><span class="sxs-lookup"><span data-stu-id="5055e-104">Sample .cub File</span></span>

<span data-ttu-id="5055e-105">Questo esempio illustra il layout di un file con estensione cub contenente due [CIEM](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="5055e-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="5055e-106">Il programma di installazione esegue le azioni personalizzate nella sequenza: ICE01 e ICE08.</span><span class="sxs-lookup"><span data-stu-id="5055e-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="5055e-107">L'azione personalizzata ICE01 è un' [azione personalizzata di tipo 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="5055e-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="5055e-108">Si tratta di un punto di ingresso per una DLL archiviata come flusso nel file con estensione cub.</span><span class="sxs-lookup"><span data-stu-id="5055e-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="5055e-109">Questo flusso è elencato nella tabella binaria ice.dll.</span><span class="sxs-lookup"><span data-stu-id="5055e-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="5055e-110">L'azione personalizzata ICE08 è un [tipo di azione personalizzata 6](custom-action-type-6.md).</span><span class="sxs-lookup"><span data-stu-id="5055e-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="5055e-111">Si tratta di un punto di ingresso di una funzione in VBScript archiviato come flusso nel file con estensione cub.</span><span class="sxs-lookup"><span data-stu-id="5055e-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="5055e-112">Questo flusso è elencato nella tabella binaria come ice.vbs.</span><span class="sxs-lookup"><span data-stu-id="5055e-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="5055e-113">Tabella binaria</span><span class="sxs-lookup"><span data-stu-id="5055e-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="5055e-114">Nome</span><span class="sxs-lookup"><span data-stu-id="5055e-114">Name</span></span>    | <span data-ttu-id="5055e-115">Data</span><span class="sxs-lookup"><span data-stu-id="5055e-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="5055e-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="5055e-116">ice.vbs</span></span> | <span data-ttu-id="5055e-117">Dati binari non formattati di ice.vbs</span><span class="sxs-lookup"><span data-stu-id="5055e-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="5055e-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="5055e-118">ice.dll</span></span> | <span data-ttu-id="5055e-119">Dati binari non formattati di ice.dll</span><span class="sxs-lookup"><span data-stu-id="5055e-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="5055e-120">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="5055e-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="5055e-121">Azione</span><span class="sxs-lookup"><span data-stu-id="5055e-121">Action</span></span> | <span data-ttu-id="5055e-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="5055e-122">Type</span></span> | <span data-ttu-id="5055e-123">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="5055e-123">Source</span></span>  | <span data-ttu-id="5055e-124">Destinazione</span><span class="sxs-lookup"><span data-stu-id="5055e-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="5055e-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="5055e-125">ICE01</span></span>  | <span data-ttu-id="5055e-126">1</span><span class="sxs-lookup"><span data-stu-id="5055e-126">1</span></span>    | <span data-ttu-id="5055e-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="5055e-127">ice.dll</span></span> | <span data-ttu-id="5055e-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="5055e-128">ICE01</span></span>  |
| <span data-ttu-id="5055e-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="5055e-129">ICE08</span></span>  | <span data-ttu-id="5055e-130">6</span><span class="sxs-lookup"><span data-stu-id="5055e-130">6</span></span>    | <span data-ttu-id="5055e-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="5055e-131">ice.vbs</span></span> | <span data-ttu-id="5055e-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="5055e-132">ICE02</span></span>  |



 

<span data-ttu-id="5055e-133">\_Tabella ICESequence</span><span class="sxs-lookup"><span data-stu-id="5055e-133">\_ICESequence Table</span></span>



| <span data-ttu-id="5055e-134">Azione</span><span class="sxs-lookup"><span data-stu-id="5055e-134">Action</span></span> | <span data-ttu-id="5055e-135">Condizione</span><span class="sxs-lookup"><span data-stu-id="5055e-135">Condition</span></span> | <span data-ttu-id="5055e-136">Sequenza</span><span class="sxs-lookup"><span data-stu-id="5055e-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="5055e-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="5055e-137">ICE01</span></span>  |           | <span data-ttu-id="5055e-138">10</span><span class="sxs-lookup"><span data-stu-id="5055e-138">10</span></span>       |
| <span data-ttu-id="5055e-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="5055e-139">ICE08</span></span>  |           | <span data-ttu-id="5055e-140">20</span><span class="sxs-lookup"><span data-stu-id="5055e-140">20</span></span>       |



 

<span data-ttu-id="5055e-141">\_Tabella speciale</span><span class="sxs-lookup"><span data-stu-id="5055e-141">\_Special Table</span></span>

<span data-ttu-id="5055e-142">ICE01 e ICE08 non richiedono l'inclusione di tabelle di elaborazione speciali.</span><span class="sxs-lookup"><span data-stu-id="5055e-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="5055e-143">Quando il file con estensione cub contiene tabelle speciali, è necessario includerle anche nella \_ tabella di convalida.</span><span class="sxs-lookup"><span data-stu-id="5055e-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="5055e-144">\_Tabella di convalida</span><span class="sxs-lookup"><span data-stu-id="5055e-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="5055e-145">Tabella</span><span class="sxs-lookup"><span data-stu-id="5055e-145">Table</span></span>         | <span data-ttu-id="5055e-146">Colonna</span><span class="sxs-lookup"><span data-stu-id="5055e-146">Column</span></span>    | <span data-ttu-id="5055e-147">Nullable</span><span class="sxs-lookup"><span data-stu-id="5055e-147">Nullable</span></span> | <span data-ttu-id="5055e-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="5055e-148">MinValue</span></span> | <span data-ttu-id="5055e-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5055e-149">MaxValue</span></span> | <span data-ttu-id="5055e-150">KeyTable</span><span class="sxs-lookup"><span data-stu-id="5055e-150">KeyTable</span></span> | <span data-ttu-id="5055e-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="5055e-151">KeyColumn</span></span> | <span data-ttu-id="5055e-152">Category</span><span class="sxs-lookup"><span data-stu-id="5055e-152">Category</span></span>                         | <span data-ttu-id="5055e-153">Set</span><span class="sxs-lookup"><span data-stu-id="5055e-153">Set</span></span> | <span data-ttu-id="5055e-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5055e-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="5055e-155">Binary</span><span class="sxs-lookup"><span data-stu-id="5055e-155">Binary</span></span>        | <span data-ttu-id="5055e-156">Nome</span><span class="sxs-lookup"><span data-stu-id="5055e-156">Name</span></span>      | <span data-ttu-id="5055e-157">N</span><span class="sxs-lookup"><span data-stu-id="5055e-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-158">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5055e-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="5055e-159">Binary</span><span class="sxs-lookup"><span data-stu-id="5055e-159">Binary</span></span>        | <span data-ttu-id="5055e-160">Data</span><span class="sxs-lookup"><span data-stu-id="5055e-160">Data</span></span>      | <span data-ttu-id="5055e-161">N</span><span class="sxs-lookup"><span data-stu-id="5055e-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-162">Binario</span><span class="sxs-lookup"><span data-stu-id="5055e-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="5055e-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="5055e-163">CustomAction</span></span>  | <span data-ttu-id="5055e-164">Azione</span><span class="sxs-lookup"><span data-stu-id="5055e-164">Action</span></span>    | <span data-ttu-id="5055e-165">N</span><span class="sxs-lookup"><span data-stu-id="5055e-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-166">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5055e-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="5055e-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="5055e-167">CustomAction</span></span>  | <span data-ttu-id="5055e-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="5055e-168">Type</span></span>      | <span data-ttu-id="5055e-169">N</span><span class="sxs-lookup"><span data-stu-id="5055e-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-170">Integer</span><span class="sxs-lookup"><span data-stu-id="5055e-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="5055e-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="5055e-171">CustomAction</span></span>  | <span data-ttu-id="5055e-172">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="5055e-172">Source</span></span>    | <span data-ttu-id="5055e-173">S</span><span class="sxs-lookup"><span data-stu-id="5055e-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-174">CustomSource</span><span class="sxs-lookup"><span data-stu-id="5055e-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="5055e-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="5055e-175">CustomAction</span></span>  | <span data-ttu-id="5055e-176">Destinazione</span><span class="sxs-lookup"><span data-stu-id="5055e-176">Target</span></span>    | <span data-ttu-id="5055e-177">S</span><span class="sxs-lookup"><span data-stu-id="5055e-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-178">Formattato</span><span class="sxs-lookup"><span data-stu-id="5055e-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="5055e-179">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="5055e-179">\_ICESequence</span></span> | <span data-ttu-id="5055e-180">Azione</span><span class="sxs-lookup"><span data-stu-id="5055e-180">Action</span></span>    | <span data-ttu-id="5055e-181">N</span><span class="sxs-lookup"><span data-stu-id="5055e-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-182">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5055e-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="5055e-183">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="5055e-183">\_ICESequence</span></span> | <span data-ttu-id="5055e-184">Condizione</span><span class="sxs-lookup"><span data-stu-id="5055e-184">Condition</span></span> | <span data-ttu-id="5055e-185">S</span><span class="sxs-lookup"><span data-stu-id="5055e-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-186">Condition</span><span class="sxs-lookup"><span data-stu-id="5055e-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="5055e-187">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="5055e-187">\_ICESequence</span></span> | <span data-ttu-id="5055e-188">Sequenza</span><span class="sxs-lookup"><span data-stu-id="5055e-188">Sequence</span></span>  | <span data-ttu-id="5055e-189">S</span><span class="sxs-lookup"><span data-stu-id="5055e-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="5055e-190">Integer</span><span class="sxs-lookup"><span data-stu-id="5055e-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



