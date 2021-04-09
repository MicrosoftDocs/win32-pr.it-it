---
description: ICEM12 verifica che in una tabella ModuleSequence le azioni standard includano numeri di sequenza e azioni personalizzate hanno BaseAction e After values.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049626"
---
# <a name="icem12"></a><span data-ttu-id="571af-103">ICEM12</span><span class="sxs-lookup"><span data-stu-id="571af-103">ICEM12</span></span>

<span data-ttu-id="571af-104">ICEM12 verifica che in una tabella ModuleSequence le azioni standard includano numeri di sequenza e azioni personalizzate hanno BaseAction e After values.</span><span class="sxs-lookup"><span data-stu-id="571af-104">ICEM12 verifies that in a ModuleSequence table, standard actions have sequence numbers and custom actions have BaseAction and After values.</span></span>

<span data-ttu-id="571af-105">Questo ICEM è disponibile nel file Mergemod. cub fornito in Windows Installer SDK 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="571af-105">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="571af-106">Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="571af-106">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="571af-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="571af-107">Result</span></span>

<span data-ttu-id="571af-108">ICEM12 Invia un errore nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="571af-108">ICEM12 posts an error in the following cases:</span></span>

-   <span data-ttu-id="571af-109">Trova il modulo che contiene un' [azione standard](standard-actions.md) senza un numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="571af-109">It finds the module contains a [standard action](standard-actions.md) without a sequence number.</span></span>
-   <span data-ttu-id="571af-110">Rileva che un'azione standard contiene valori immessi nei campi BaseAction o After della tabella [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence Table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence Table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence Table](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="571af-110">It finds that a standard action has values entered in the BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>
-   <span data-ttu-id="571af-111">Trova il modulo che contiene un' [azione personalizzata](custom-actions.md) senza i valori immessi nei campi Sequence, BaseAction o After della [tabella ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence Table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence Table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence Table](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="571af-111">It finds the module contains a [custom action](custom-actions.md) without any values entered into the Sequence, BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>

<span data-ttu-id="571af-112">ICEM12 Invia un avviso se trova un'azione personalizzata con un numero di sequenza specificato, ma nessun valore nei campi BaseAction o After.</span><span class="sxs-lookup"><span data-stu-id="571af-112">ICEM12 posts a warning if it finds a custom action that has a Sequence number specified, but no value in the BaseAction or After fields.</span></span>

<span data-ttu-id="571af-113">Si noti che tutte le azioni trovate nella [tabella CustomAction](customaction-table.md) sono considerate azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="571af-113">Note that all actions found in the [CustomAction table](customaction-table.md) are considered custom actions.</span></span> <span data-ttu-id="571af-114">Tutte le altre azioni sono considerate azioni standard.</span><span class="sxs-lookup"><span data-stu-id="571af-114">All other action are considered standard actions.</span></span>

## <a name="example"></a><span data-ttu-id="571af-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="571af-115">Example</span></span>

<span data-ttu-id="571af-116">ICEM12 invia i messaggi di avviso e di errore seguenti per un modulo che contiene le voci del database indicate di seguito:</span><span class="sxs-lookup"><span data-stu-id="571af-116">ICEM12 posts the following error and warning messages for a module that contains the database entries shown below:</span></span>

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[<span data-ttu-id="571af-117">CustomAction</span><span class="sxs-lookup"><span data-stu-id="571af-117">CustomAction</span></span>](customaction-table.md)



| <span data-ttu-id="571af-118">Azione</span><span class="sxs-lookup"><span data-stu-id="571af-118">Action</span></span>  | <span data-ttu-id="571af-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="571af-119">Type</span></span> | <span data-ttu-id="571af-120">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="571af-120">Source</span></span>  | <span data-ttu-id="571af-121">Destinazione</span><span class="sxs-lookup"><span data-stu-id="571af-121">Target</span></span>  |
|---------|------|---------|---------|
| <span data-ttu-id="571af-122">Action1</span><span class="sxs-lookup"><span data-stu-id="571af-122">Action1</span></span> | <span data-ttu-id="571af-123">30</span><span class="sxs-lookup"><span data-stu-id="571af-123">30</span></span>   | <span data-ttu-id="571af-124">source1</span><span class="sxs-lookup"><span data-stu-id="571af-124">source1</span></span> | <span data-ttu-id="571af-125">Target1</span><span class="sxs-lookup"><span data-stu-id="571af-125">target1</span></span> |
| <span data-ttu-id="571af-126">Action3</span><span class="sxs-lookup"><span data-stu-id="571af-126">Action3</span></span> | <span data-ttu-id="571af-127">30</span><span class="sxs-lookup"><span data-stu-id="571af-127">30</span></span>   | <span data-ttu-id="571af-128">source3</span><span class="sxs-lookup"><span data-stu-id="571af-128">source3</span></span> | <span data-ttu-id="571af-129">Target3</span><span class="sxs-lookup"><span data-stu-id="571af-129">target3</span></span> |



 

[<span data-ttu-id="571af-130">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="571af-130">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)



| <span data-ttu-id="571af-131">Azione</span><span class="sxs-lookup"><span data-stu-id="571af-131">Action</span></span>  | <span data-ttu-id="571af-132">Sequenza</span><span class="sxs-lookup"><span data-stu-id="571af-132">Sequence</span></span> | <span data-ttu-id="571af-133">BaseAction</span><span class="sxs-lookup"><span data-stu-id="571af-133">BaseAction</span></span> | <span data-ttu-id="571af-134">After</span><span class="sxs-lookup"><span data-stu-id="571af-134">After</span></span> | <span data-ttu-id="571af-135">Condizione</span><span class="sxs-lookup"><span data-stu-id="571af-135">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="571af-136">Action2</span><span class="sxs-lookup"><span data-stu-id="571af-136">Action2</span></span> |          | <span data-ttu-id="571af-137">Action1</span><span class="sxs-lookup"><span data-stu-id="571af-137">Action1</span></span>    | <span data-ttu-id="571af-138">1</span><span class="sxs-lookup"><span data-stu-id="571af-138">1</span></span>     | <span data-ttu-id="571af-139">true</span><span class="sxs-lookup"><span data-stu-id="571af-139">true</span></span>      |
| <span data-ttu-id="571af-140">Action3</span><span class="sxs-lookup"><span data-stu-id="571af-140">Action3</span></span> |          |            |       | <span data-ttu-id="571af-141">true</span><span class="sxs-lookup"><span data-stu-id="571af-141">true</span></span>      |



 

[<span data-ttu-id="571af-142">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="571af-142">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="571af-143">Azione</span><span class="sxs-lookup"><span data-stu-id="571af-143">Action</span></span>  | <span data-ttu-id="571af-144">Sequenza</span><span class="sxs-lookup"><span data-stu-id="571af-144">Sequence</span></span> | <span data-ttu-id="571af-145">BaseAction</span><span class="sxs-lookup"><span data-stu-id="571af-145">BaseAction</span></span> | <span data-ttu-id="571af-146">After</span><span class="sxs-lookup"><span data-stu-id="571af-146">After</span></span> | <span data-ttu-id="571af-147">Condizione</span><span class="sxs-lookup"><span data-stu-id="571af-147">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="571af-148">Action1</span><span class="sxs-lookup"><span data-stu-id="571af-148">Action1</span></span> | <span data-ttu-id="571af-149">1</span><span class="sxs-lookup"><span data-stu-id="571af-149">1</span></span>        |            |       | <span data-ttu-id="571af-150">true</span><span class="sxs-lookup"><span data-stu-id="571af-150">true</span></span>      |



 

<span data-ttu-id="571af-151">Per correggere questi errori, provare a eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="571af-151">To fix these errors try the following:</span></span>

-   <span data-ttu-id="571af-152">Rimuovere il numero di sequenza per l'azione personalizzata action1 e usare invece i campi BaseAction e After.</span><span class="sxs-lookup"><span data-stu-id="571af-152">Remove the sequence number for the custom action Action1 and use the BaseAction and After fields instead.</span></span>
-   <span data-ttu-id="571af-153">Immettere i valori nei campi Sequence, BaseAction o After per l'azione personalizzata Action3.</span><span class="sxs-lookup"><span data-stu-id="571af-153">Enter values into the Sequence, BaseAction, or After fields for the custom action Action3.</span></span> <span data-ttu-id="571af-154">Lasciare vuoti i campi BaseAction e After per l'azione standard Action2.</span><span class="sxs-lookup"><span data-stu-id="571af-154">Leave the BaseAction and After fields empty for standard action Action2.</span></span>
-   <span data-ttu-id="571af-155">Non lasciare vuoto il campo sequenza per l'azione standard Action2.</span><span class="sxs-lookup"><span data-stu-id="571af-155">Do not leave the Sequence field empty for standard action Action2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="571af-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="571af-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="571af-157">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="571af-157">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



