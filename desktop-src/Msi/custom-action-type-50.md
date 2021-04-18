---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 50 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Tipo di azione personalizzata 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315909"
---
# <a name="custom-action-type-50"></a><span data-ttu-id="f78ff-103">Tipo di azione personalizzata 50</span><span class="sxs-lookup"><span data-stu-id="f78ff-103">Custom Action Type 50</span></span>

<span data-ttu-id="f78ff-104">Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f78ff-104">This custom action calls an executable launched with a command line.</span></span>

<span data-ttu-id="f78ff-105">Vedere anche [file eseguibili](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="f78ff-105">See also [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="f78ff-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="f78ff-106">Source</span></span>

<span data-ttu-id="f78ff-107">Il file eseguibile viene generato da un file esistente.</span><span class="sxs-lookup"><span data-stu-id="f78ff-107">The executable is generated from an existing file.</span></span> <span data-ttu-id="f78ff-108">Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella di proprietà](property-table.md) per una proprietà che contiene il percorso completo del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="f78ff-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Property table](property-table.md) for a property that contains the full path to the executable file.</span></span>

## <a name="type-value"></a><span data-ttu-id="f78ff-109">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="f78ff-109">Type Value</span></span>

<span data-ttu-id="f78ff-110">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="f78ff-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="f78ff-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="f78ff-111">Constants</span></span>                                                        | <span data-ttu-id="f78ff-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="f78ff-112">Hexadecimal</span></span> | <span data-ttu-id="f78ff-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="f78ff-113">Decimal</span></span> |
|------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f78ff-114">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="f78ff-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="f78ff-115">0x032</span><span class="sxs-lookup"><span data-stu-id="f78ff-115">0x032</span></span>       | <span data-ttu-id="f78ff-116">50</span><span class="sxs-lookup"><span data-stu-id="f78ff-116">50</span></span>      |



 

## <a name="target"></a><span data-ttu-id="f78ff-117">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f78ff-117">Target</span></span>

<span data-ttu-id="f78ff-118">La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene la stringa della riga di comando per il file eseguibile identificato nella colonna di origine.</span><span class="sxs-lookup"><span data-stu-id="f78ff-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f78ff-119">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="f78ff-119">Return Processing Options</span></span>

<span data-ttu-id="f78ff-120">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="f78ff-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="f78ff-121">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="f78ff-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f78ff-122">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="f78ff-122">Execution Scheduling Options</span></span>

<span data-ttu-id="f78ff-123">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f78ff-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="f78ff-124">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="f78ff-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="f78ff-125">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f78ff-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f78ff-126">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="f78ff-126">In-Script Execution Options</span></span>

<span data-ttu-id="f78ff-127">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="f78ff-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="f78ff-128">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="f78ff-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="f78ff-129">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="f78ff-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="f78ff-130">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="f78ff-130">Return Values</span></span>

<span data-ttu-id="f78ff-131">Per l'esito positivo, le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="f78ff-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="f78ff-132">Il programma di installazione interpreta qualsiasi altro valore restituito come errore.</span><span class="sxs-lookup"><span data-stu-id="f78ff-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="f78ff-133">Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="f78ff-133">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="f78ff-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="f78ff-134">Remarks</span></span>

<span data-ttu-id="f78ff-135">Un'azione personalizzata che avvia un file eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="f78ff-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="f78ff-136">Se si tratta anche di un' [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md), il programma di installazione utilizza CreateProcessAsUser ha o CreateProcess per creare il processo quando viene richiamata l'azione personalizzata dallo script di installazione.</span><span class="sxs-lookup"><span data-stu-id="f78ff-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses CreateProcessAsUser or CreateProcess to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f78ff-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f78ff-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f78ff-138">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="f78ff-138">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



