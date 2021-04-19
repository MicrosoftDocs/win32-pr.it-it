---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 19 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo di azione personalizzata 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319973"
---
# <a name="custom-action-type-19"></a><span data-ttu-id="bedda-103">Tipo di azione personalizzata 19</span><span class="sxs-lookup"><span data-stu-id="bedda-103">Custom Action Type 19</span></span>

<span data-ttu-id="bedda-104">Questa azione personalizzata Visualizza un messaggio di errore specificato, restituisce un errore e quindi termina l'installazione.</span><span class="sxs-lookup"><span data-stu-id="bedda-104">This custom action displays a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="bedda-105">Il messaggio di errore visualizzato può essere fornito come stringa o come indice nella tabella degli [errori](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="bedda-105">The error message displayed can be supplied as a string or as an index into the [Error table](error-table.md).</span></span>

## <a name="source"></a><span data-ttu-id="bedda-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="bedda-106">Source</span></span>

<span data-ttu-id="bedda-107">Lasciare vuota la colonna di origine della [tabella CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bedda-107">Leave the Source column of the [CustomAction table](customaction-table.md) blank.</span></span>

## <a name="type-value"></a><span data-ttu-id="bedda-108">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="bedda-108">Type Value</span></span>

<span data-ttu-id="bedda-109">Includere il valore seguente nella colonna Type della tabella CustomAction per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="bedda-109">Include the following value in the Type column of the CustomAction table to specify the basic numeric type.</span></span>



| <span data-ttu-id="bedda-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="bedda-110">Constants</span></span>                                                               | <span data-ttu-id="bedda-111">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="bedda-111">Hexadecimal</span></span> | <span data-ttu-id="bedda-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="bedda-112">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="bedda-113">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="bedda-113">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="bedda-114">0x013</span><span class="sxs-lookup"><span data-stu-id="bedda-114">0x013</span></span>       | <span data-ttu-id="bedda-115">19</span><span class="sxs-lookup"><span data-stu-id="bedda-115">19</span></span>      |



 

## <a name="target"></a><span data-ttu-id="bedda-116">Destinazione</span><span class="sxs-lookup"><span data-stu-id="bedda-116">Target</span></span>

<span data-ttu-id="bedda-117">La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata utilizzando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori dei campi numerici).</span><span class="sxs-lookup"><span data-stu-id="bedda-117">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="bedda-118">I parametri da sostituire sono racchiusi tra parentesi quadre, \[ ... \] e possono essere proprietà, variabili di ambiente (% prefix), percorsi di file ( \# prefisso) o percorsi di directory dei componenti ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="bedda-118">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="bedda-119">Se dopo la formattazione la stringa restituisce un valore integer, tale integer viene utilizzato come indice nella tabella degli [errori](error-table.md) per recuperare il messaggio da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="bedda-119">If after formatting the string evaluates to an integer, that integer is used as an index into the [Error table](error-table.md) to retrieve the message to display.</span></span> <span data-ttu-id="bedda-120">Se dopo la formattazione la stringa contiene caratteri non numerici, la stringa stessa viene visualizzata come messaggio.</span><span class="sxs-lookup"><span data-stu-id="bedda-120">If after formatting the string contains non-numeric characters, the string itself is displayed as the message.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="bedda-121">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="bedda-121">Return Processing Options</span></span>

<span data-ttu-id="bedda-122">L'azione personalizzata non usa alcuna opzione.</span><span class="sxs-lookup"><span data-stu-id="bedda-122">The custom action does not use any options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="bedda-123">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="bedda-123">Execution Scheduling Options</span></span>

<span data-ttu-id="bedda-124">L'azione personalizzata non usa alcuna opzione.</span><span class="sxs-lookup"><span data-stu-id="bedda-124">The custom action does not use any options.</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="bedda-125">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="bedda-125">In-Script Execution Options</span></span>

<span data-ttu-id="bedda-126">L'azione personalizzata non usa alcuna opzione.</span><span class="sxs-lookup"><span data-stu-id="bedda-126">The custom action does not use any options.</span></span>

## <a name="return-values"></a><span data-ttu-id="bedda-127">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="bedda-127">Return Values</span></span>

<span data-ttu-id="bedda-128">Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bedda-128">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bedda-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="bedda-129">Remarks</span></span>

<span data-ttu-id="bedda-130">Ad esempio, le azioni personalizzate CAError1, CAError2, CAError3 e CAError4 restituiscono questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="bedda-130">For example, the custom actions CAError1, CAError2, CAError3, and CAError4 return these messages.</span></span>

[<span data-ttu-id="bedda-131">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="bedda-131">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="bedda-132">Azione</span><span class="sxs-lookup"><span data-stu-id="bedda-132">Action</span></span>   | <span data-ttu-id="bedda-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="bedda-133">Type</span></span> | <span data-ttu-id="bedda-134">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="bedda-134">Source</span></span> | <span data-ttu-id="bedda-135">Destinazione</span><span class="sxs-lookup"><span data-stu-id="bedda-135">Target</span></span>                              |
|----------|------|--------|-------------------------------------|
| <span data-ttu-id="bedda-136">CAError1</span><span class="sxs-lookup"><span data-stu-id="bedda-136">CAError1</span></span> | <span data-ttu-id="bedda-137">19</span><span class="sxs-lookup"><span data-stu-id="bedda-137">19</span></span>   |        | <span data-ttu-id="bedda-138">\[Prop1\]</span><span class="sxs-lookup"><span data-stu-id="bedda-138">\[Prop1\]</span></span>                           |
| <span data-ttu-id="bedda-139">CAError2</span><span class="sxs-lookup"><span data-stu-id="bedda-139">CAError2</span></span> | <span data-ttu-id="bedda-140">19</span><span class="sxs-lookup"><span data-stu-id="bedda-140">19</span></span>   |        | <span data-ttu-id="bedda-141">Errore di installazione dovuto a Error2.</span><span class="sxs-lookup"><span data-stu-id="bedda-141">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="bedda-142">CAError3</span><span class="sxs-lookup"><span data-stu-id="bedda-142">CAError3</span></span> | <span data-ttu-id="bedda-143">19</span><span class="sxs-lookup"><span data-stu-id="bedda-143">19</span></span>   |        | <span data-ttu-id="bedda-144">25000</span><span class="sxs-lookup"><span data-stu-id="bedda-144">25000</span></span>                               |
| <span data-ttu-id="bedda-145">CAError4</span><span class="sxs-lookup"><span data-stu-id="bedda-145">CAError4</span></span> | <span data-ttu-id="bedda-146">19</span><span class="sxs-lookup"><span data-stu-id="bedda-146">19</span></span>   |        | <span data-ttu-id="bedda-147">\[Prop2\]</span><span class="sxs-lookup"><span data-stu-id="bedda-147">\[Prop2\]</span></span>                           |



 

[<span data-ttu-id="bedda-148">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="bedda-148">Property Table</span></span>](property-table.md)



| <span data-ttu-id="bedda-149">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bedda-149">Property</span></span> | <span data-ttu-id="bedda-150">Valore</span><span class="sxs-lookup"><span data-stu-id="bedda-150">Value</span></span>                                 |
|----------|---------------------------------------|
| <span data-ttu-id="bedda-151">Prop1</span><span class="sxs-lookup"><span data-stu-id="bedda-151">Prop1</span></span>    | <span data-ttu-id="bedda-152">"Errore di installazione dovuto a Error1".</span><span class="sxs-lookup"><span data-stu-id="bedda-152">"Installation failure due to Error1."</span></span> |
| <span data-ttu-id="bedda-153">Prop2</span><span class="sxs-lookup"><span data-stu-id="bedda-153">Prop2</span></span>    | <span data-ttu-id="bedda-154">"25100"</span><span class="sxs-lookup"><span data-stu-id="bedda-154">"25100"</span></span>                               |



 

[<span data-ttu-id="bedda-155">Tabella degli errori</span><span class="sxs-lookup"><span data-stu-id="bedda-155">Error Table</span></span>](error-table.md)



| <span data-ttu-id="bedda-156">Codice</span><span class="sxs-lookup"><span data-stu-id="bedda-156">Code</span></span>  | <span data-ttu-id="bedda-157">Message</span><span class="sxs-lookup"><span data-stu-id="bedda-157">Message</span></span>                             |
|-------|-------------------------------------|
| <span data-ttu-id="bedda-158">25000</span><span class="sxs-lookup"><span data-stu-id="bedda-158">25000</span></span> | <span data-ttu-id="bedda-159">Errore di installazione dovuto a Error3.</span><span class="sxs-lookup"><span data-stu-id="bedda-159">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="bedda-160">25100</span><span class="sxs-lookup"><span data-stu-id="bedda-160">25100</span></span> | <span data-ttu-id="bedda-161">Errore di installazione dovuto a Error4.</span><span class="sxs-lookup"><span data-stu-id="bedda-161">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="bedda-162">Queste azioni personalizzate restituiscono i messaggi di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="bedda-162">These custom actions return the following error messages:</span></span>



| <span data-ttu-id="bedda-163">Azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="bedda-163">Custom action</span></span> | <span data-ttu-id="bedda-164">Stringa di messaggio restituita</span><span class="sxs-lookup"><span data-stu-id="bedda-164">Returned message string</span></span>             |
|---------------|-------------------------------------|
| <span data-ttu-id="bedda-165">CAError1</span><span class="sxs-lookup"><span data-stu-id="bedda-165">CAError1</span></span>      | <span data-ttu-id="bedda-166">Errore di installazione dovuto a Error1.</span><span class="sxs-lookup"><span data-stu-id="bedda-166">Installation failure due to Error1.</span></span> |
| <span data-ttu-id="bedda-167">CAError2</span><span class="sxs-lookup"><span data-stu-id="bedda-167">CAError2</span></span>      | <span data-ttu-id="bedda-168">Errore di installazione dovuto a Error2.</span><span class="sxs-lookup"><span data-stu-id="bedda-168">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="bedda-169">CAError3</span><span class="sxs-lookup"><span data-stu-id="bedda-169">CAError3</span></span>      | <span data-ttu-id="bedda-170">Errore di installazione dovuto a Error3.</span><span class="sxs-lookup"><span data-stu-id="bedda-170">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="bedda-171">CAError4</span><span class="sxs-lookup"><span data-stu-id="bedda-171">CAError4</span></span>      | <span data-ttu-id="bedda-172">Errore di installazione dovuto a Error4.</span><span class="sxs-lookup"><span data-stu-id="bedda-172">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="bedda-173">Si noti che poiché non è possibile garantire l'ordine di valutazione delle condizioni di avvio mediante la creazione della [tabella LaunchCondition](launchcondition-table.md), è consigliabile utilizzare il tipo di azione personalizzata 19 azioni personalizzate nell'installazione per valutare le condizioni in un ordine specifico.</span><span class="sxs-lookup"><span data-stu-id="bedda-173">Note that because the order of evaluation of launch conditions cannot be guaranteed by authoring the [LaunchCondition table](launchcondition-table.md), you should use Custom Action Type 19 custom actions in your installation to evaluate conditions in a specific order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bedda-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bedda-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bedda-175">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="bedda-175">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



