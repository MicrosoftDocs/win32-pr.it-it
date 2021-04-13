---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 17 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo di azione personalizzata 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349001"
---
# <a name="custom-action-type-17"></a><span data-ttu-id="a02db-103">Tipo di azione personalizzata 17</span><span class="sxs-lookup"><span data-stu-id="a02db-103">Custom Action Type 17</span></span>

<span data-ttu-id="a02db-104">Questa azione personalizzata chiama una libreria a collegamento dinamico (DLL) scritta in C o C++.</span><span class="sxs-lookup"><span data-stu-id="a02db-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="a02db-105">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="a02db-105">Source</span></span>

<span data-ttu-id="a02db-106">La DLL viene installata con l'applicazione durante la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="a02db-106">The DLL is installed with the application during the current session.</span></span> <span data-ttu-id="a02db-107">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="a02db-108">Il percorso del codice dell'azione personalizzata è determinato dalla risoluzione del percorso di destinazione per il file. di conseguenza, questa azione personalizzata deve essere chiamata dopo che il file è stato installato e prima che venga rimosso.</span><span class="sxs-lookup"><span data-stu-id="a02db-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after that file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="a02db-109">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="a02db-109">Type Value</span></span>

<span data-ttu-id="a02db-110">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="a02db-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="a02db-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="a02db-111">Constants</span></span>                                                          | <span data-ttu-id="a02db-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="a02db-112">Hexadecimal</span></span> | <span data-ttu-id="a02db-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="a02db-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a02db-114">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="a02db-114">**msidbCustomActionTypeDll** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="a02db-115">0x011</span><span class="sxs-lookup"><span data-stu-id="a02db-115">0x011</span></span>       | <span data-ttu-id="a02db-116">17</span><span class="sxs-lookup"><span data-stu-id="a02db-116">17</span></span>      |



 

## <a name="target"></a><span data-ttu-id="a02db-117">Destinazione</span><span class="sxs-lookup"><span data-stu-id="a02db-117">Target</span></span>

<span data-ttu-id="a02db-118">La DLL viene chiamata tramite il punto di ingresso denominato nel campo di destinazione della [tabella CustomAction](customaction-table.md), passando un solo argomento che rappresenta l'handle della sessione di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="a02db-118">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="a02db-119">Il nome del punto di ingresso specificato nella tabella deve corrispondere a quello esportato dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="a02db-119">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="a02db-120">Si noti che se la funzione entry non è specificata da un oggetto. File DEF o con una specifica/EXPORT: linker, il nome può avere un carattere di sottolineatura e un @4 suffisso "".</span><span class="sxs-lookup"><span data-stu-id="a02db-120">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="a02db-121">La funzione chiamata deve specificare la \_ \_ convenzione di chiamata stdcall.</span><span class="sxs-lookup"><span data-stu-id="a02db-121">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="a02db-122">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="a02db-122">Return Processing Options</span></span>

<span data-ttu-id="a02db-123">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="a02db-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="a02db-124">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="a02db-125">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="a02db-125">Execution Scheduling Options</span></span>

<span data-ttu-id="a02db-126">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a02db-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="a02db-127">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a02db-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="a02db-128">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="a02db-129">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="a02db-129">In-Script Execution Options</span></span>

<span data-ttu-id="a02db-130">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="a02db-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="a02db-131">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="a02db-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="a02db-132">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="a02db-133">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="a02db-133">Return Values</span></span>

<span data-ttu-id="a02db-134">Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-134">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a02db-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="a02db-135">Remarks</span></span>

<span data-ttu-id="a02db-136">Un'azione personalizzata che chiama una libreria a collegamento dinamico (DLL) richiede un handle per la sessione di installazione.</span><span class="sxs-lookup"><span data-stu-id="a02db-136">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="a02db-137">Se si tratta anche di un'azione personalizzata di esecuzione posticipata, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione.</span><span class="sxs-lookup"><span data-stu-id="a02db-137">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="a02db-138">Per informazioni sul modo in cui un'azione personalizzata di questo tipo può ottenere informazioni sul contesto, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-138">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="a02db-139">Le azioni personalizzate vengono eseguite in un thread separato e possono avere accesso limitato al sistema.</span><span class="sxs-lookup"><span data-stu-id="a02db-139">Custom actions execute in a separate thread, and may have limited access to the system.</span></span> <span data-ttu-id="a02db-140">Le azioni personalizzate che vengono eseguite in modo asincrono bloccano il thread principale alla chiusura della sequenza corrente o della sessione di installazione fino a quando non vengono restituite.</span><span class="sxs-lookup"><span data-stu-id="a02db-140">Custom actions that run asynchronously block the main thread at the termination of either the current sequence or the install session until they return.</span></span>

<span data-ttu-id="a02db-141">Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzato 17 (DLL), devono rispettare le restrizioni di sequenziazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="a02db-141">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="a02db-142">L'azione personalizzata deve essere sequenziata dopo l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-142">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="a02db-143">In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare la DLL.</span><span class="sxs-lookup"><span data-stu-id="a02db-143">This is so that the custom action can resolve the path needed to locate the DLL.</span></span>
-   <span data-ttu-id="a02db-144">Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (in-script) di questo tipo devono essere sequenziate dopo l' [azione InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-144">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="a02db-145">Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="a02db-145">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a02db-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a02db-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a02db-147">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="a02db-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="a02db-148">Azioni personalizzate di esecuzione posticipata</span><span class="sxs-lookup"><span data-stu-id="a02db-148">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="a02db-149">Librerie a collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="a02db-149">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> </dl>

 

 



