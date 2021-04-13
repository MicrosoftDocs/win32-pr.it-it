---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 21 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Tipo di azione personalizzata 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348996"
---
# <a name="custom-action-type-21"></a><span data-ttu-id="2a59b-103">Tipo di azione personalizzata 21</span><span class="sxs-lookup"><span data-stu-id="2a59b-103">Custom Action Type 21</span></span>

<span data-ttu-id="2a59b-104">Questa azione personalizzata è scritta in JScript, ad esempio ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="2a59b-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="2a59b-105">Windows Installer non supporta JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="2a59b-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="2a59b-106">Per ulteriori informazioni, vedere [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="2a59b-107">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="2a59b-107">Source</span></span>

<span data-ttu-id="2a59b-108">Lo script viene installato con l'applicazione durante la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="2a59b-108">The script is installed with the application during the current session.</span></span> <span data-ttu-id="2a59b-109">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="2a59b-110">Il percorso del codice dell'azione personalizzata è determinato dalla risoluzione del percorso di destinazione per il file. Pertanto, questa azione personalizzata deve essere chiamata dopo l'installazione del file e prima della rimozione.</span><span class="sxs-lookup"><span data-stu-id="2a59b-110">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="2a59b-111">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="2a59b-111">Type Value</span></span>

<span data-ttu-id="2a59b-112">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2a59b-112">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="2a59b-113">Costanti</span><span class="sxs-lookup"><span data-stu-id="2a59b-113">Constants</span></span>                                                              | <span data-ttu-id="2a59b-114">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="2a59b-114">Hexadecimal</span></span> | <span data-ttu-id="2a59b-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="2a59b-115">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="2a59b-116">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="2a59b-116">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="2a59b-117">0x015</span><span class="sxs-lookup"><span data-stu-id="2a59b-117">0x015</span></span>       | <span data-ttu-id="2a59b-118">21</span><span class="sxs-lookup"><span data-stu-id="2a59b-118">21</span></span>      |



 

<span data-ttu-id="2a59b-119">Windows Installer possibile utilizzare [azioni personalizzate a 64 bit](64-bit-custom-actions.md) sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2a59b-119">Windows Installer may use [64-bit Custom Actions](64-bit-custom-actions.md) on 64-bit operating systems.</span></span> <span data-ttu-id="2a59b-120">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="2a59b-120">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="2a59b-121">Per informazioni, vedere azioni personalizzate a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2a59b-121">For information see 64-bit Custom Actions.</span></span> <span data-ttu-id="2a59b-122">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2a59b-122">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="2a59b-123">Costanti</span><span class="sxs-lookup"><span data-stu-id="2a59b-123">Constants</span></span>                                                                                                     | <span data-ttu-id="2a59b-124">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="2a59b-124">Hexadecimal</span></span> | <span data-ttu-id="2a59b-125">Decimal</span><span class="sxs-lookup"><span data-stu-id="2a59b-125">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="2a59b-126">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="2a59b-126">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="2a59b-127">0x0001015</span><span class="sxs-lookup"><span data-stu-id="2a59b-127">0x0001015</span></span>   | <span data-ttu-id="2a59b-128">4117</span><span class="sxs-lookup"><span data-stu-id="2a59b-128">4117</span></span>    |



 

## <a name="target"></a><span data-ttu-id="2a59b-129">Destinazione</span><span class="sxs-lookup"><span data-stu-id="2a59b-129">Target</span></span>

<span data-ttu-id="2a59b-130">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="2a59b-130">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="2a59b-131">L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="2a59b-131">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="2a59b-132">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="2a59b-132">Return Processing Options</span></span>

<span data-ttu-id="2a59b-133">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="2a59b-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="2a59b-134">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-134">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="2a59b-135">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="2a59b-135">Execution Scheduling Options</span></span>

<span data-ttu-id="2a59b-136">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2a59b-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="2a59b-137">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="2a59b-137">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="2a59b-138">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-138">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="2a59b-139">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="2a59b-139">In-Script Execution Options</span></span>

<span data-ttu-id="2a59b-140">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="2a59b-140">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="2a59b-141">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="2a59b-141">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="2a59b-142">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-142">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="2a59b-143">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="2a59b-143">Return Values</span></span>

<span data-ttu-id="2a59b-144">Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-144">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a59b-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a59b-145">Remarks</span></span>

<span data-ttu-id="2a59b-146">Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**sessione**](session-object.md) di installazione.</span><span class="sxs-lookup"><span data-stu-id="2a59b-146">A custom action that is written in JScript or VBScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="2a59b-147">Il programma di installazione associa l' **oggetto sessione** allo script con il nome "Session".</span><span class="sxs-lookup"><span data-stu-id="2a59b-147">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="2a59b-148">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.</span><span class="sxs-lookup"><span data-stu-id="2a59b-148">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="2a59b-149">Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzata 21 (JScript), devono rispettare le restrizioni di sequenziazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a59b-149">Custom actions that reference an installed file as their source, such as Custom Action Type 21 (JScript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="2a59b-150">L'azione personalizzata deve essere sequenziata dopo l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-150">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="2a59b-151">In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare il file di origine contenente JScript.</span><span class="sxs-lookup"><span data-stu-id="2a59b-151">This is so that the custom action can resolve the path needed to locate the source file containing the JScript.</span></span>
-   <span data-ttu-id="2a59b-152">Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (in-script) di questo tipo devono essere sequenziate dopo l' [azione InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-152">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="2a59b-153">Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="2a59b-153">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a59b-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a59b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a59b-155">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="2a59b-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



