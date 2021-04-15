---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 54 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Tipo di azione personalizzata 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485492"
---
# <a name="custom-action-type-54"></a><span data-ttu-id="6267d-103">Tipo di azione personalizzata 54</span><span class="sxs-lookup"><span data-stu-id="6267d-103">Custom Action Type 54</span></span>

<span data-ttu-id="6267d-104">Questa azione personalizzata è scritta in VBScript.</span><span class="sxs-lookup"><span data-stu-id="6267d-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="6267d-105">Vedere anche [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="6267d-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="6267d-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="6267d-106">Source</span></span>

<span data-ttu-id="6267d-107">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene un nome di proprietà o una chiave per la [tabella](property-table.md) delle proprietà per una proprietà contenente il testo dello script.</span><span class="sxs-lookup"><span data-stu-id="6267d-107">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="6267d-108">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="6267d-108">Type Value</span></span>

<span data-ttu-id="6267d-109">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6267d-109">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="6267d-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="6267d-110">Constants</span></span>                                                             | <span data-ttu-id="6267d-111">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="6267d-111">Hexadecimal</span></span> | <span data-ttu-id="6267d-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="6267d-112">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="6267d-113">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="6267d-113">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="6267d-114">0x036</span><span class="sxs-lookup"><span data-stu-id="6267d-114">0x036</span></span>       | <span data-ttu-id="6267d-115">54</span><span class="sxs-lookup"><span data-stu-id="6267d-115">54</span></span>      |



 

<span data-ttu-id="6267d-116">Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6267d-116">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="6267d-117">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="6267d-117">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="6267d-118">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6267d-118">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="6267d-119">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6267d-119">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="6267d-120">Costanti</span><span class="sxs-lookup"><span data-stu-id="6267d-120">Constants</span></span>                                                                                                    | <span data-ttu-id="6267d-121">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="6267d-121">Hexadecimal</span></span> | <span data-ttu-id="6267d-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="6267d-122">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="6267d-123">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="6267d-123">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="6267d-124">0x0001036</span><span class="sxs-lookup"><span data-stu-id="6267d-124">0x0001036</span></span>   | <span data-ttu-id="6267d-125">4150</span><span class="sxs-lookup"><span data-stu-id="6267d-125">4150</span></span>    |



 

## <a name="target"></a><span data-ttu-id="6267d-126">Destinazione</span><span class="sxs-lookup"><span data-stu-id="6267d-126">Target</span></span>

<span data-ttu-id="6267d-127">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="6267d-127">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="6267d-128">L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="6267d-128">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="6267d-129">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="6267d-129">Return Processing Options</span></span>

<span data-ttu-id="6267d-130">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="6267d-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="6267d-131">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="6267d-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="6267d-132">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="6267d-132">Execution Scheduling Options</span></span>

<span data-ttu-id="6267d-133">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6267d-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="6267d-134">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="6267d-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="6267d-135">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="6267d-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="6267d-136">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="6267d-136">In-Script Execution Options</span></span>

<span data-ttu-id="6267d-137">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="6267d-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="6267d-138">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="6267d-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="6267d-139">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="6267d-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="6267d-140">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="6267d-140">Return Values</span></span>

<span data-ttu-id="6267d-141">Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6267d-141">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6267d-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="6267d-142">Remarks</span></span>

<span data-ttu-id="6267d-143">Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**sessione**](session-object.md) di installazione.</span><span class="sxs-lookup"><span data-stu-id="6267d-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="6267d-144">Il programma di installazione associa l' **oggetto sessione** allo script con la *sessione* del nome.</span><span class="sxs-lookup"><span data-stu-id="6267d-144">The installer attaches the **Session Object** to the script with the name *Session*.</span></span> <span data-ttu-id="6267d-145">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.</span><span class="sxs-lookup"><span data-stu-id="6267d-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6267d-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6267d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6267d-147">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="6267d-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



