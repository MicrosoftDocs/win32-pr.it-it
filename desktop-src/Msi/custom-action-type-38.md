---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 38 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Tipo di azione personalizzata 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968018"
---
# <a name="custom-action-type-38"></a><span data-ttu-id="06459-103">Tipo di azione personalizzata 38</span><span class="sxs-lookup"><span data-stu-id="06459-103">Custom Action Type 38</span></span>

<span data-ttu-id="06459-104">Questa azione personalizzata è scritta in VBScript.</span><span class="sxs-lookup"><span data-stu-id="06459-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="06459-105">Vedere anche [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="06459-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="06459-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="06459-106">Source</span></span>

<span data-ttu-id="06459-107">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene il valore null.</span><span class="sxs-lookup"><span data-stu-id="06459-107">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="06459-108">Il codice di script per l'azione personalizzata viene archiviato come una stringa di testo letterale di script nel campo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="06459-108">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="06459-109">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="06459-109">Type Value</span></span>

<span data-ttu-id="06459-110">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="06459-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="06459-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="06459-111">Constants</span></span>                                                              | <span data-ttu-id="06459-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="06459-112">Hexadecimal</span></span> | <span data-ttu-id="06459-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="06459-113">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="06459-114">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="06459-114">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="06459-115">0x026</span><span class="sxs-lookup"><span data-stu-id="06459-115">0x026</span></span>       | <span data-ttu-id="06459-116">38</span><span class="sxs-lookup"><span data-stu-id="06459-116">38</span></span>      |



 

<span data-ttu-id="06459-117">Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="06459-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="06459-118">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="06459-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="06459-119">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="06459-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="06459-120">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="06459-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="06459-121">Costanti</span><span class="sxs-lookup"><span data-stu-id="06459-121">Constants</span></span>                                                                                                     | <span data-ttu-id="06459-122">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="06459-122">Hexadecimal</span></span> | <span data-ttu-id="06459-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="06459-123">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="06459-124">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="06459-124">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="06459-125">0x0001026</span><span class="sxs-lookup"><span data-stu-id="06459-125">0x0001026</span></span>   | <span data-ttu-id="06459-126">4134</span><span class="sxs-lookup"><span data-stu-id="06459-126">4134</span></span>    |



 

## <a name="target"></a><span data-ttu-id="06459-127">Destinazione</span><span class="sxs-lookup"><span data-stu-id="06459-127">Target</span></span>

<span data-ttu-id="06459-128">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene il codice di script per l'azione personalizzata come una stringa di testo di script letterali.</span><span class="sxs-lookup"><span data-stu-id="06459-128">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="06459-129">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="06459-129">Return Processing Options</span></span>

<span data-ttu-id="06459-130">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="06459-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="06459-131">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="06459-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="06459-132">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="06459-132">Execution Scheduling Options</span></span>

<span data-ttu-id="06459-133">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="06459-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="06459-134">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="06459-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="06459-135">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="06459-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="06459-136">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="06459-136">In-Script Execution Options</span></span>

<span data-ttu-id="06459-137">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="06459-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="06459-138">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="06459-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="06459-139">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="06459-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="06459-140">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="06459-140">Return Values</span></span>

<span data-ttu-id="06459-141">Questo tipo di azione personalizzata restituisce sempre success.</span><span class="sxs-lookup"><span data-stu-id="06459-141">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="06459-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="06459-142">Remarks</span></span>

<span data-ttu-id="06459-143">Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**sessione**](session-object.md) di installazione.</span><span class="sxs-lookup"><span data-stu-id="06459-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="06459-144">Il programma di installazione associa l' **oggetto sessione** allo script con il nome "Session".</span><span class="sxs-lookup"><span data-stu-id="06459-144">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="06459-145">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.</span><span class="sxs-lookup"><span data-stu-id="06459-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06459-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06459-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06459-147">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="06459-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



