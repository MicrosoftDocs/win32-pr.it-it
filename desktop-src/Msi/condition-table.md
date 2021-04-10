---
description: La tabella Condition può essere utilizzata per modificare lo stato di selezione di qualsiasi voce nella tabella feature basata su un'espressione condizionale.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabella Condition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966491"
---
# <a name="condition-table"></a><span data-ttu-id="b7661-103">Tabella Condition</span><span class="sxs-lookup"><span data-stu-id="b7661-103">Condition Table</span></span>

<span data-ttu-id="b7661-104">La tabella Condition può essere utilizzata per modificare lo stato di selezione di qualsiasi voce nella [tabella Feature](feature-table.md) basata su un'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="b7661-104">The Condition table can be used to modify the selection state of any entry in the [Feature table](feature-table.md) based on a conditional expression.</span></span>

<span data-ttu-id="b7661-105">La tabella Condition contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7661-105">The Condition table has the following columns.</span></span>



| <span data-ttu-id="b7661-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="b7661-106">Column</span></span>    | <span data-ttu-id="b7661-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7661-107">Type</span></span>                         | <span data-ttu-id="b7661-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="b7661-108">Key</span></span> | <span data-ttu-id="b7661-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b7661-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="b7661-110">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="b7661-110">Feature\_</span></span> | [<span data-ttu-id="b7661-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="b7661-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b7661-112">S</span><span class="sxs-lookup"><span data-stu-id="b7661-112">Y</span></span>   | <span data-ttu-id="b7661-113">N</span><span class="sxs-lookup"><span data-stu-id="b7661-113">N</span></span>        |
| <span data-ttu-id="b7661-114">Level</span><span class="sxs-lookup"><span data-stu-id="b7661-114">Level</span></span>     | [<span data-ttu-id="b7661-115">Integer</span><span class="sxs-lookup"><span data-stu-id="b7661-115">Integer</span></span>](integer.md)       | <span data-ttu-id="b7661-116">S</span><span class="sxs-lookup"><span data-stu-id="b7661-116">Y</span></span>   | <span data-ttu-id="b7661-117">N</span><span class="sxs-lookup"><span data-stu-id="b7661-117">N</span></span>        |
| <span data-ttu-id="b7661-118">Condizione</span><span class="sxs-lookup"><span data-stu-id="b7661-118">Condition</span></span> | [<span data-ttu-id="b7661-119">Condition</span><span class="sxs-lookup"><span data-stu-id="b7661-119">Condition</span></span>](condition.md)   | <span data-ttu-id="b7661-120">N</span><span class="sxs-lookup"><span data-stu-id="b7661-120">N</span></span>   | <span data-ttu-id="b7661-121">S</span><span class="sxs-lookup"><span data-stu-id="b7661-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b7661-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="b7661-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b7661-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="b7661-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="b7661-124">Chiave esterna nella colonna uno della tabella delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b7661-124">External key into column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="b7661-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Livello</span><span class="sxs-lookup"><span data-stu-id="b7661-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Level</span></span>
</dt> <dd>

<span data-ttu-id="b7661-126">Livello di installazione condizionale per la funzionalità nella \_ colonna feature della tabella.</span><span class="sxs-lookup"><span data-stu-id="b7661-126">A conditional install level for the feature in the Feature\_ column of this table.</span></span> <span data-ttu-id="b7661-127">Il programma di installazione imposta il livello di installazione della funzionalità sul livello specificato in questa colonna se l'espressione nella colonna condizione restituisce TRUE.</span><span class="sxs-lookup"><span data-stu-id="b7661-127">The installer sets the install level of this feature to the level specified in this column if the expression in the Condition column evaluates to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="b7661-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="b7661-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="b7661-129">Se questa espressione condizionale restituisce TRUE, la colonna Level della tabella Feature viene impostata sul livello di installazione condizionale.</span><span class="sxs-lookup"><span data-stu-id="b7661-129">If this conditional expression evaluates to TRUE, then the Level column in the Feature table is set to the conditional install level.</span></span>

<span data-ttu-id="b7661-130">L'espressione nella colonna condizione non deve contenere riferimenti allo stato di installazione di una funzionalità o di un componente.</span><span class="sxs-lookup"><span data-stu-id="b7661-130">The expression in the Condition column should not contain reference to the installed state of any feature or component.</span></span> <span data-ttu-id="b7661-131">Ciò è dovuto al fatto che le espressioni nella colonna condition vengono valutate prima che il programma di installazione valuti gli stati installati delle funzionalità e dei componenti.</span><span class="sxs-lookup"><span data-stu-id="b7661-131">This is because the expressions in the Condition column are evaluated before the installer evaluates the installed states of features and components.</span></span> <span data-ttu-id="b7661-132">Qualsiasi espressione nella tabella della condizione che tenta di verificare lo stato installato di una funzionalità o di un componente restituisce sempre false.</span><span class="sxs-lookup"><span data-stu-id="b7661-132">Any expression in the Condition table that attempts to check the installed state of a feature or component always evaluates to false.</span></span>

<span data-ttu-id="b7661-133">Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b7661-133">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7661-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7661-134">Remarks</span></span>

<span data-ttu-id="b7661-135">Una funzionalità può essere disabilitata in modo permanente impostando la colonna livello su 0.</span><span class="sxs-lookup"><span data-stu-id="b7661-135">A feature can be permanently disabled by setting the Level column to 0.</span></span>

<span data-ttu-id="b7661-136">Il livello può essere impostato in base a qualsiasi istruzione condizionale, ad esempio un test per la piattaforma, il sistema operativo o una particolare impostazione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b7661-136">The Level may be set based on any conditional statement, such as a test for platform, operating system, or a particular property setting.</span></span>

<span data-ttu-id="b7661-137">È necessario scegliere attentamente le condizioni in modo che una funzionalità non sia abilitata durante l'installazione e quindi disabilitata durante la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="b7661-137">Conditions should be carefully chosen so that a feature is not enabled on install and then disabled on uninstall.</span></span> <span data-ttu-id="b7661-138">La funzionalità verrà orfana e il prodotto non potrà essere disinstallato.</span><span class="sxs-lookup"><span data-stu-id="b7661-138">This will orphan the feature and the product will not be able to be uninstalled.</span></span>

<span data-ttu-id="b7661-139">Questa tabella viene definita quando viene eseguita l' [azione CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b7661-139">This table is referred to when the [CostFinalize action](costfinalize-action.md) is executed.</span></span>

<span data-ttu-id="b7661-140">Se la proprietà [**preselezionata**](preselected.md) è stata impostata su 1, il programma di installazione non valuta la tabella della condizione.</span><span class="sxs-lookup"><span data-stu-id="b7661-140">If the [**Preselected**](preselected.md) property has been set to 1, the installer does not evaluate the Condition table.</span></span> <span data-ttu-id="b7661-141">La tabella della condizione influiscono solo sull'installazione delle funzionalità quando non è stata impostata nessuna delle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7661-141">The Condition table affects only the installation of features when none of the following properties have been set:</span></span>

<dl>

[<span data-ttu-id="b7661-142">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b7661-142">**ADDLOCAL**</span></span>](addlocal.md)  
[<span data-ttu-id="b7661-143">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="b7661-143">**REMOVE**</span></span>](remove.md)  
[<span data-ttu-id="b7661-144">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b7661-144">**ADDSOURCE**</span></span>](addsource.md)  
[<span data-ttu-id="b7661-145">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b7661-145">**ADDDEFAULT**</span></span>](adddefault.md)  
[<span data-ttu-id="b7661-146">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="b7661-146">**REINSTALL**</span></span>](reinstall.md)  
[<span data-ttu-id="b7661-147">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="b7661-147">**ADVERTISE**</span></span>](advertise.md)  
[<span data-ttu-id="b7661-148">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b7661-148">**COMPADDLOCAL**</span></span>](compaddlocal.md)  
[<span data-ttu-id="b7661-149">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b7661-149">**COMPADDSOURCE**</span></span>](compaddsource.md)  
[<span data-ttu-id="b7661-150">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b7661-150">**COMPADDDEFAULT**</span></span>](compadddefault.md)  
[<span data-ttu-id="b7661-151">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b7661-151">**FILEADDLOCAL**</span></span>](fileaddlocal.md)  
[<span data-ttu-id="b7661-152">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b7661-152">**FILEADDSOURCE**</span></span>](fileaddsource.md)  
[<span data-ttu-id="b7661-153">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b7661-153">**FILEADDDEFAULT**</span></span>](fileadddefault.md)  
</dl>

## <a name="validation"></a><span data-ttu-id="b7661-154">Convalida</span><span class="sxs-lookup"><span data-stu-id="b7661-154">Validation</span></span>

<dl>

[<span data-ttu-id="b7661-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="b7661-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b7661-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="b7661-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b7661-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="b7661-157">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b7661-158">ICE46</span><span class="sxs-lookup"><span data-stu-id="b7661-158">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b7661-159">ICE79</span><span class="sxs-lookup"><span data-stu-id="b7661-159">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="b7661-160">ICE86</span><span class="sxs-lookup"><span data-stu-id="b7661-160">ICE86</span></span>](ice86.md)  
</dl>

 

 



