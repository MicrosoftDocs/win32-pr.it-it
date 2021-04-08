---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 18 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Tipo di azione personalizzata 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968464"
---
# <a name="custom-action-type-18"></a><span data-ttu-id="350ce-103">Tipo di azione personalizzata 18</span><span class="sxs-lookup"><span data-stu-id="350ce-103">Custom Action Type 18</span></span>

<span data-ttu-id="350ce-104">Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="350ce-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="350ce-105">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="350ce-105">Source</span></span>

<span data-ttu-id="350ce-106">Il file eseguibile viene generato da un file installato con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350ce-106">The executable is generated from a file installed with the application.</span></span> <span data-ttu-id="350ce-107">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="350ce-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="350ce-108">Il percorso del codice dell'azione personalizzata è determinato dalla risoluzione del percorso di destinazione per il file. Pertanto, questa azione personalizzata deve essere chiamata dopo l'installazione del file e prima della rimozione.</span><span class="sxs-lookup"><span data-stu-id="350ce-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="350ce-109">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="350ce-109">Type Value</span></span>

<span data-ttu-id="350ce-110">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="350ce-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="350ce-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="350ce-111">Constants</span></span>                                                          | <span data-ttu-id="350ce-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="350ce-112">Hexadecimal</span></span> | <span data-ttu-id="350ce-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="350ce-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="350ce-114">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="350ce-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="350ce-115">0x012</span><span class="sxs-lookup"><span data-stu-id="350ce-115">0x012</span></span>       | <span data-ttu-id="350ce-116">18</span><span class="sxs-lookup"><span data-stu-id="350ce-116">18</span></span>      |



 

## <a name="target"></a><span data-ttu-id="350ce-117">Destinazione</span><span class="sxs-lookup"><span data-stu-id="350ce-117">Target</span></span>

<span data-ttu-id="350ce-118">La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene la stringa della riga di comando per il file eseguibile identificato nella colonna di origine.</span><span class="sxs-lookup"><span data-stu-id="350ce-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="350ce-119">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="350ce-119">Return Processing Options</span></span>

<span data-ttu-id="350ce-120">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="350ce-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="350ce-121">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="350ce-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="350ce-122">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="350ce-122">Execution Scheduling Options</span></span>

<span data-ttu-id="350ce-123">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="350ce-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="350ce-124">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="350ce-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="350ce-125">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="350ce-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="350ce-126">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="350ce-126">In-Script Execution Options</span></span>

<span data-ttu-id="350ce-127">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="350ce-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="350ce-128">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="350ce-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="350ce-129">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="350ce-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="350ce-130">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="350ce-130">Return Values</span></span>

<span data-ttu-id="350ce-131">Per l'esito positivo, le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="350ce-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="350ce-132">Il programma di installazione interpreta qualsiasi altro valore restituito come errore.</span><span class="sxs-lookup"><span data-stu-id="350ce-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="350ce-133">Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="350ce-133">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="350ce-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="350ce-134">Remarks</span></span>

<span data-ttu-id="350ce-135">Un'azione personalizzata che avvia un file eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="350ce-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="350ce-136">Se si tratta anche di un' [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md), il programma di installazione utilizza [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando viene richiamata l'azione personalizzata dallo script di installazione.</span><span class="sxs-lookup"><span data-stu-id="350ce-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="350ce-137">Le azioni personalizzate che fanno riferimento a un file installato come origine, ad esempio il tipo di azione personalizzata 18 (EXE), devono rispettare le restrizioni di sequenziazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="350ce-137">Custom actions that reference an installed file as their source, such as Custom Action Type 18 (EXE), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="350ce-138">L'azione personalizzata deve essere sequenziata dopo l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="350ce-138">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="350ce-139">In questo modo l'azione personalizzata può risolvere il percorso necessario per individuare il file EXE.</span><span class="sxs-lookup"><span data-stu-id="350ce-139">This is so that the custom action can resolve the path needed to locate the EXE.</span></span>
-   <span data-ttu-id="350ce-140">Se il file di origine non è già installato nel computer, le azioni personalizzate posticipate (in-script) di questo tipo devono essere sequenziate dopo l' [azione InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="350ce-140">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="350ce-141">Se il file di origine non è già installato nel computer, le azioni personalizzate non posticipate di questo tipo devono essere sequenziate dopo l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="350ce-141">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="350ce-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="350ce-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350ce-143">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="350ce-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="350ce-144">File eseguibili</span><span class="sxs-lookup"><span data-stu-id="350ce-144">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
