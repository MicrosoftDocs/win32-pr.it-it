---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 22 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Tipo di azione personalizzata 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00b4772b1d2532c0291223cc5c4b6a63ead9324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350631"
---
# <a name="custom-action-type-22"></a><span data-ttu-id="9bed0-103">Tipo di azione personalizzata 22</span><span class="sxs-lookup"><span data-stu-id="9bed0-103">Custom Action Type 22</span></span>

<span data-ttu-id="9bed0-104">Questa azione personalizzata è scritta in VBScript.</span><span class="sxs-lookup"><span data-stu-id="9bed0-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="9bed0-105">Vedere anche [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="9bed0-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="9bed0-106">Source</span></span>

<span data-ttu-id="9bed0-107">Lo script viene installato con l'applicazione durante la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="9bed0-107">The script is installed with the application during the current session.</span></span> <span data-ttu-id="9bed0-108">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="9bed0-109">Il percorso del codice dell'azione personalizzata è determinato dalla risoluzione del percorso di destinazione per il file. Pertanto, questa azione personalizzata deve essere chiamata dopo l'installazione del file e prima della rimozione.</span><span class="sxs-lookup"><span data-stu-id="9bed0-109">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="9bed0-110">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="9bed0-110">Type Value</span></span>

<span data-ttu-id="9bed0-111">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9bed0-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="9bed0-112">Costanti</span><span class="sxs-lookup"><span data-stu-id="9bed0-112">Constants</span></span>                                                               | <span data-ttu-id="9bed0-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="9bed0-113">Hexadecimal</span></span> | <span data-ttu-id="9bed0-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="9bed0-114">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9bed0-115">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="9bed0-115">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="9bed0-116">0x016</span><span class="sxs-lookup"><span data-stu-id="9bed0-116">0x016</span></span>       | <span data-ttu-id="9bed0-117">22</span><span class="sxs-lookup"><span data-stu-id="9bed0-117">22</span></span>      |



 

<span data-ttu-id="9bed0-118">Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9bed0-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="9bed0-119">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="9bed0-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="9bed0-120">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="9bed0-121">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9bed0-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="9bed0-122">Costanti</span><span class="sxs-lookup"><span data-stu-id="9bed0-122">Constants</span></span>                                                                                                      | <span data-ttu-id="9bed0-123">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="9bed0-123">Hexadecimal</span></span> | <span data-ttu-id="9bed0-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="9bed0-124">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9bed0-125">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="9bed0-125">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="9bed0-126">0x0001016</span><span class="sxs-lookup"><span data-stu-id="9bed0-126">0x0001016</span></span>   | <span data-ttu-id="9bed0-127">4118</span><span class="sxs-lookup"><span data-stu-id="9bed0-127">4118</span></span>    |



 

## <a name="target"></a><span data-ttu-id="9bed0-128">Destinazione</span><span class="sxs-lookup"><span data-stu-id="9bed0-128">Target</span></span>

<span data-ttu-id="9bed0-129">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="9bed0-129">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="9bed0-130">L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="9bed0-130">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9bed0-131">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="9bed0-131">Return Processing Options</span></span>

<span data-ttu-id="9bed0-132">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="9bed0-132">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9bed0-133">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-133">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9bed0-134">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="9bed0-134">Execution Scheduling Options</span></span>

<span data-ttu-id="9bed0-135">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9bed0-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9bed0-136">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="9bed0-136">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9bed0-137">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-137">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9bed0-138">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="9bed0-138">In-Script Execution Options</span></span>

<span data-ttu-id="9bed0-139">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="9bed0-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9bed0-140">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="9bed0-140">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9bed0-141">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-141">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9bed0-142">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="9bed0-142">Return Values</span></span>

<span data-ttu-id="9bed0-143">Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-143">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9bed0-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bed0-144">Remarks</span></span>

<span data-ttu-id="9bed0-145">Un'azione personalizzata scritta in JScript o VBScript richiede l' [**oggetto sessione**](session-object.md)di installazione.</span><span class="sxs-lookup"><span data-stu-id="9bed0-145">A custom action that is written in JScript or VBScript requires the install [**Session Object**](session-object.md).</span></span> <span data-ttu-id="9bed0-146">Si tratta dell' **oggetto Session** del tipo e il programma di installazione lo connette allo script con il nome "Session".</span><span class="sxs-lookup"><span data-stu-id="9bed0-146">This is of the type **Session Object** and the installer attaches it to the script with the name "Session".</span></span> <span data-ttu-id="9bed0-147">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.</span><span class="sxs-lookup"><span data-stu-id="9bed0-147">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="9bed0-148">Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzata 22 (VBcript), devono rispettare le restrizioni di sequenziazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="9bed0-148">Custom actions that reference an installed file as their source, such as Custom Action Type 22 (VBcript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="9bed0-149">L'azione personalizzata deve essere sequenziata dopo l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-149">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="9bed0-150">In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare il file di origine contenente VBScript.</span><span class="sxs-lookup"><span data-stu-id="9bed0-150">This is so that the custom action can resolve the path needed to locate the source file containing the VBScript.</span></span>
-   <span data-ttu-id="9bed0-151">Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (in-script) di questo tipo devono essere sequenziate dopo l' [azione InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-151">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="9bed0-152">Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9bed0-152">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bed0-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bed0-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bed0-154">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="9bed0-154">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



