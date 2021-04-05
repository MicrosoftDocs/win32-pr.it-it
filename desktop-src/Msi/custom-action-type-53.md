---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 53 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Tipo di azione personalizzata 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a016d3b3f5a282567b909215d6ab7b32759417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967818"
---
# <a name="custom-action-type-53"></a><span data-ttu-id="61292-103">Tipo di azione personalizzata 53</span><span class="sxs-lookup"><span data-stu-id="61292-103">Custom Action Type 53</span></span>

<span data-ttu-id="61292-104">Questa azione personalizzata è scritta in JScript, ad esempio ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="61292-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="61292-105">Windows Installer non supporta JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="61292-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="61292-106">Per ulteriori informazioni, vedere [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="61292-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="61292-107">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="61292-107">Source</span></span>

<span data-ttu-id="61292-108">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene un nome di proprietà o una chiave per la [tabella](property-table.md) delle proprietà per una proprietà contenente il testo dello script.</span><span class="sxs-lookup"><span data-stu-id="61292-108">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="61292-109">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="61292-109">Type Value</span></span>

<span data-ttu-id="61292-110">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="61292-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="61292-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="61292-111">Constants</span></span>                                                            | <span data-ttu-id="61292-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="61292-112">Hexadecimal</span></span> | <span data-ttu-id="61292-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="61292-113">Decimal</span></span> |
|----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="61292-114">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="61292-114">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="61292-115">0x035</span><span class="sxs-lookup"><span data-stu-id="61292-115">0x035</span></span>       | <span data-ttu-id="61292-116">53</span><span class="sxs-lookup"><span data-stu-id="61292-116">53</span></span>      |



 

<span data-ttu-id="61292-117">Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="61292-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="61292-118">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="61292-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="61292-119">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="61292-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="61292-120">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="61292-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="61292-121">Costanti</span><span class="sxs-lookup"><span data-stu-id="61292-121">Constants</span></span>                                                                                                   | <span data-ttu-id="61292-122">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="61292-122">Hexadecimal</span></span> | <span data-ttu-id="61292-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="61292-123">Decimal</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="61292-124">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="61292-124">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="61292-125">0x0001035</span><span class="sxs-lookup"><span data-stu-id="61292-125">0x0001035</span></span>   | <span data-ttu-id="61292-126">4149</span><span class="sxs-lookup"><span data-stu-id="61292-126">4149</span></span>    |



 

## <a name="target"></a><span data-ttu-id="61292-127">Destinazione</span><span class="sxs-lookup"><span data-stu-id="61292-127">Target</span></span>

<span data-ttu-id="61292-128">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="61292-128">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="61292-129">L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="61292-129">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="61292-130">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="61292-130">Return Processing Options</span></span>

<span data-ttu-id="61292-131">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="61292-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="61292-132">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="61292-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="61292-133">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="61292-133">Execution Scheduling Options</span></span>

<span data-ttu-id="61292-134">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="61292-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="61292-135">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="61292-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="61292-136">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="61292-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="61292-137">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="61292-137">In-Script Execution Options</span></span>

<span data-ttu-id="61292-138">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="61292-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="61292-139">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="61292-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="61292-140">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="61292-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="61292-141">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="61292-141">Return Values</span></span>

<span data-ttu-id="61292-142">Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="61292-142">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61292-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="61292-143">Remarks</span></span>

<span data-ttu-id="61292-144">Un'azione personalizzata scritta in JScript richiede l'oggetto [**sessione**](session-object.md) di installazione.</span><span class="sxs-lookup"><span data-stu-id="61292-144">A custom action that is written in JScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="61292-145">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script usa uno dei metodi descritti in [ottenere informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="61292-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script uses one of the methods described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61292-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61292-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61292-147">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="61292-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



