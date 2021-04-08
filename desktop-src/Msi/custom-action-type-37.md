---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 37 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Tipo di azione personalizzata 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a42d4837af6fe2878f33624251d9c06550855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057978"
---
# <a name="custom-action-type-37"></a><span data-ttu-id="62148-103">Tipo di azione personalizzata 37</span><span class="sxs-lookup"><span data-stu-id="62148-103">Custom Action Type 37</span></span>

<span data-ttu-id="62148-104">Questa azione personalizzata è scritta in JScript, ad esempio ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="62148-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="62148-105">Windows Installer non supporta JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="62148-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="62148-106">Per ulteriori informazioni, vedere [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="62148-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="62148-107">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="62148-107">Source</span></span>

<span data-ttu-id="62148-108">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene il valore null.</span><span class="sxs-lookup"><span data-stu-id="62148-108">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="62148-109">Il codice di script per l'azione personalizzata viene archiviato come una stringa di testo letterale di script nel campo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62148-109">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="62148-110">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="62148-110">Type Value</span></span>

<span data-ttu-id="62148-111">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="62148-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="62148-112">Costanti</span><span class="sxs-lookup"><span data-stu-id="62148-112">Constants</span></span>                                                             | <span data-ttu-id="62148-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="62148-113">Hexadecimal</span></span> | <span data-ttu-id="62148-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="62148-114">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="62148-115">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="62148-115">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="62148-116">0x025</span><span class="sxs-lookup"><span data-stu-id="62148-116">0x025</span></span>       | <span data-ttu-id="62148-117">37</span><span class="sxs-lookup"><span data-stu-id="62148-117">37</span></span>      |



 

<span data-ttu-id="62148-118">Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="62148-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="62148-119">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="62148-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="62148-120">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="62148-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="62148-121">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="62148-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="62148-122">Costanti</span><span class="sxs-lookup"><span data-stu-id="62148-122">Constants</span></span>                                                                                                    | <span data-ttu-id="62148-123">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="62148-123">Hexadecimal</span></span> | <span data-ttu-id="62148-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="62148-124">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="62148-125">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="62148-125">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="62148-126">0x0001025</span><span class="sxs-lookup"><span data-stu-id="62148-126">0x0001025</span></span>   | <span data-ttu-id="62148-127">4133</span><span class="sxs-lookup"><span data-stu-id="62148-127">4133</span></span>    |



 

## <a name="target"></a><span data-ttu-id="62148-128">Destinazione</span><span class="sxs-lookup"><span data-stu-id="62148-128">Target</span></span>

<span data-ttu-id="62148-129">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene il codice di script per l'azione personalizzata come una stringa di testo di script letterali.</span><span class="sxs-lookup"><span data-stu-id="62148-129">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="62148-130">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="62148-130">Return Processing Options</span></span>

<span data-ttu-id="62148-131">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="62148-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="62148-132">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="62148-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="62148-133">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="62148-133">Execution Scheduling Options</span></span>

<span data-ttu-id="62148-134">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="62148-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="62148-135">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="62148-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="62148-136">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="62148-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="62148-137">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="62148-137">In-Script Execution Options</span></span>

<span data-ttu-id="62148-138">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="62148-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="62148-139">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="62148-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="62148-140">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="62148-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="62148-141">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="62148-141">Return Values</span></span>

<span data-ttu-id="62148-142">Questo tipo di azione personalizzata restituisce sempre success.</span><span class="sxs-lookup"><span data-stu-id="62148-142">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="62148-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="62148-143">Remarks</span></span>

<span data-ttu-id="62148-144">Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**sessione**](session-object.md) di installazione.</span><span class="sxs-lookup"><span data-stu-id="62148-144">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="62148-145">Il programma di installazione associa l' **oggetto sessione** allo script con il nome "Session".</span><span class="sxs-lookup"><span data-stu-id="62148-145">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="62148-146">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.</span><span class="sxs-lookup"><span data-stu-id="62148-146">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62148-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62148-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62148-148">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="62148-148">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



