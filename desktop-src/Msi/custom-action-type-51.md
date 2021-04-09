---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 51 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Tipo di azione personalizzata 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968103"
---
# <a name="custom-action-type-51"></a><span data-ttu-id="99dc3-103">Tipo di azione personalizzata 51</span><span class="sxs-lookup"><span data-stu-id="99dc3-103">Custom Action Type 51</span></span>

<span data-ttu-id="99dc3-104">Questa azione personalizzata imposta una proprietà da una stringa di testo formattata.</span><span class="sxs-lookup"><span data-stu-id="99dc3-104">This custom action sets a property from a formatted text string.</span></span>

<span data-ttu-id="99dc3-105">Per influenzare una proprietà utilizzata in una condizione su un componente o una funzionalità, l'azione personalizzata deve precedere l' [azione CostFinalize secondo](costfinalize-action.md) nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="99dc3-105">To affect a property used in a condition on a component or feature, the custom action must come before the [CostFinalize action](costfinalize-action.md) in the action sequence.</span></span>

## <a name="source"></a><span data-ttu-id="99dc3-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="99dc3-106">Source</span></span>

<span data-ttu-id="99dc3-107">Il campo di origine della [tabella CustomAction](customaction-table.md) può contenere il nome di una proprietà o una chiave per la [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="99dc3-107">The Source field of the [CustomAction table](customaction-table.md) can contain either the name of a property or a key to the [Property table](property-table.md).</span></span> <span data-ttu-id="99dc3-108">Questa proprietà viene impostata dalla stringa formattata nel campo di destinazione usando [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span><span class="sxs-lookup"><span data-stu-id="99dc3-108">This property is set by the formatted string in the Target field using [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span></span>

## <a name="type-value"></a><span data-ttu-id="99dc3-109">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="99dc3-109">Type Value</span></span>

<span data-ttu-id="99dc3-110">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="99dc3-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="99dc3-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="99dc3-111">Constants</span></span>                                                             | <span data-ttu-id="99dc3-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="99dc3-112">Hexadecimal</span></span> | <span data-ttu-id="99dc3-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="99dc3-113">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="99dc3-114">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="99dc3-114">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="99dc3-115">0x033</span><span class="sxs-lookup"><span data-stu-id="99dc3-115">0x033</span></span>       | <span data-ttu-id="99dc3-116">51</span><span class="sxs-lookup"><span data-stu-id="99dc3-116">51</span></span>      |



 

## <a name="target"></a><span data-ttu-id="99dc3-117">Destinazione</span><span class="sxs-lookup"><span data-stu-id="99dc3-117">Target</span></span>

<span data-ttu-id="99dc3-118">La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata utilizzando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori dei campi numerici).</span><span class="sxs-lookup"><span data-stu-id="99dc3-118">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="99dc3-119">I parametri da sostituire sono racchiusi tra parentesi quadre, \[ ... \] e possono essere proprietà, variabili di ambiente (% prefix), percorsi di file ( \# prefisso) o percorsi di directory dei componenti ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="99dc3-119">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="99dc3-120">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="99dc3-120">Return Processing Options</span></span>

<span data-ttu-id="99dc3-121">L'azione personalizzata non usa queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="99dc3-121">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="99dc3-122">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="99dc3-122">Execution Scheduling Options</span></span>

<span data-ttu-id="99dc3-123">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="99dc3-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="99dc3-124">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="99dc3-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="99dc3-125">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="99dc3-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="99dc3-126">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="99dc3-126">In-Script Execution Options</span></span>

<span data-ttu-id="99dc3-127">L'azione personalizzata non usa queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="99dc3-127">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="99dc3-128">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="99dc3-128">Return Values</span></span>

<span data-ttu-id="99dc3-129">Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="99dc3-129">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99dc3-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="99dc3-130">Remarks</span></span>

<span data-ttu-id="99dc3-131">Se si imposta una [proprietà privata](private-properties.md) nella sequenza dell'interfaccia utente creando un'azione personalizzata in una delle tabelle di sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="99dc3-131">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="99dc3-132">Per impostare la proprietà nella sequenza di esecuzione, è inoltre necessario inserire un'azione personalizzata in una tabella della sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="99dc3-132">To set the property in the execution sequence, you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="99dc3-133">In alternativa, è possibile rendere la proprietà una [proprietà pubblica](public-properties.md) e includerla nella [**proprietà SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="99dc3-133">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99dc3-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99dc3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99dc3-135">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="99dc3-135">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="99dc3-136">Azioni personalizzate del testo formattato</span><span class="sxs-lookup"><span data-stu-id="99dc3-136">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



