---
description: La tabella AdminExecuteSequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l'azione di amministrazione di primo livello.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Tabella AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311071"
---
# <a name="adminexecutesequence-table"></a><span data-ttu-id="194db-103">Tabella AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="194db-103">AdminExecuteSequence Table</span></span>

<span data-ttu-id="194db-104">La tabella AdminExecuteSequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l' [azione di amministrazione](admin-action.md) di primo livello.</span><span class="sxs-lookup"><span data-stu-id="194db-104">The AdminExecuteSequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed.</span></span>

<span data-ttu-id="194db-105">Le azioni amministrative nella sequenza di installazione, fino all' [azione InstallValidate](installvalidate-action.md) e alle finestre di dialogo di uscita, si trovano nella [tabella AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="194db-105">ADMIN actions in the install sequence, up to the [InstallValidate action](installvalidate-action.md) and any exit dialog boxes, are located in the [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="194db-106">Le azioni amministrative dall'azione InstallValidate fino alla fine della sequenza di installazione si trovano nella tabella AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="194db-106">ADMIN actions from the InstallValidate action through the end of the install sequence are in the AdminExecuteSequence table.</span></span> <span data-ttu-id="194db-107">Poiché la tabella AdminExecuteSequence deve essere autonoma, contiene anche tutte le azioni di inizializzazione necessarie, ad esempio [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="194db-107">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span>

<span data-ttu-id="194db-108">Le [azioni personalizzate](custom-actions.md) che richiedono un'interfaccia utente devono usare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anziché le finestre di dialogo Create con la [tabella della finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="194db-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="194db-109">Le colonne sono identiche a quelle della [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="194db-109">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="194db-110">La tabella AdminExecuteSequence include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="194db-110">The AdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="194db-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="194db-111">Column</span></span>    | <span data-ttu-id="194db-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="194db-112">Type</span></span>                         | <span data-ttu-id="194db-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="194db-113">Key</span></span> | <span data-ttu-id="194db-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="194db-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="194db-115">Azione</span><span class="sxs-lookup"><span data-stu-id="194db-115">Action</span></span>    | [<span data-ttu-id="194db-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="194db-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="194db-117">S</span><span class="sxs-lookup"><span data-stu-id="194db-117">Y</span></span>   | <span data-ttu-id="194db-118">N</span><span class="sxs-lookup"><span data-stu-id="194db-118">N</span></span>        |
| <span data-ttu-id="194db-119">Condizione</span><span class="sxs-lookup"><span data-stu-id="194db-119">Condition</span></span> | [<span data-ttu-id="194db-120">Condition</span><span class="sxs-lookup"><span data-stu-id="194db-120">Condition</span></span>](condition.md)   | <span data-ttu-id="194db-121">N</span><span class="sxs-lookup"><span data-stu-id="194db-121">N</span></span>   | <span data-ttu-id="194db-122">S</span><span class="sxs-lookup"><span data-stu-id="194db-122">Y</span></span>        |
| <span data-ttu-id="194db-123">Sequenza</span><span class="sxs-lookup"><span data-stu-id="194db-123">Sequence</span></span>  | [<span data-ttu-id="194db-124">Integer</span><span class="sxs-lookup"><span data-stu-id="194db-124">Integer</span></span>](integer.md)       | <span data-ttu-id="194db-125">N</span><span class="sxs-lookup"><span data-stu-id="194db-125">N</span></span>   | <span data-ttu-id="194db-126">S</span><span class="sxs-lookup"><span data-stu-id="194db-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="194db-127">Colonne</span><span class="sxs-lookup"><span data-stu-id="194db-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="194db-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="194db-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="194db-129">Nome dell'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="194db-129">Name of the action to execute.</span></span> <span data-ttu-id="194db-130">Si tratta di un'azione standard o di un'azione personalizzata elencata nella [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="194db-130">This is either a standard action or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="194db-131">Chiave della tabella primaria.</span><span class="sxs-lookup"><span data-stu-id="194db-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="194db-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="194db-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="194db-133">Espressione logica.</span><span class="sxs-lookup"><span data-stu-id="194db-133">Logical expression.</span></span> <span data-ttu-id="194db-134">Se l'espressione restituisce false, l'azione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="194db-134">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="194db-135">Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="194db-135">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="194db-136">Per informazioni sulla sintassi delle istruzioni condizionali, vedere Sintassi delle istruzioni [condizionali](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="194db-136">For information on the syntax of conditional statements see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="194db-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="194db-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="194db-138">Un valore positivo indica la posizione della sequenza dell'azione.</span><span class="sxs-lookup"><span data-stu-id="194db-138">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="194db-139">I valori negativi seguenti indicano che l'azione viene chiamata se il programma di installazione restituisce il flag di terminazione.</span><span class="sxs-lookup"><span data-stu-id="194db-139">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="194db-140">Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione.</span><span class="sxs-lookup"><span data-stu-id="194db-140">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="194db-141">Più azioni possono avere flag di terminazione, ma devono essere flag diversi.</span><span class="sxs-lookup"><span data-stu-id="194db-141">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="194db-142">I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="194db-142">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="194db-143">Flag di terminazione</span><span class="sxs-lookup"><span data-stu-id="194db-143">Termination flag</span></span>          | <span data-ttu-id="194db-144">Valore</span><span class="sxs-lookup"><span data-stu-id="194db-144">Value</span></span> | <span data-ttu-id="194db-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="194db-145">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="194db-146">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="194db-146">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="194db-147">-1</span><span class="sxs-lookup"><span data-stu-id="194db-147">-1</span></span>    | <span data-ttu-id="194db-148">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="194db-148">Successful completion.</span></span> <span data-ttu-id="194db-149">Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="194db-149">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="194db-150">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="194db-150">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="194db-151">-2</span><span class="sxs-lookup"><span data-stu-id="194db-151">-2</span></span>    | <span data-ttu-id="194db-152">L'utente termina l'installazione.</span><span class="sxs-lookup"><span data-stu-id="194db-152">User terminates install.</span></span> <span data-ttu-id="194db-153">Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="194db-153">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="194db-154">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="194db-154">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="194db-155">-3</span><span class="sxs-lookup"><span data-stu-id="194db-155">-3</span></span>    | <span data-ttu-id="194db-156">Terminazione irreversibile.</span><span class="sxs-lookup"><span data-stu-id="194db-156">Fatal exit terminates.</span></span> <span data-ttu-id="194db-157">Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="194db-157">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="194db-158">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="194db-158">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="194db-159">-4</span><span class="sxs-lookup"><span data-stu-id="194db-159">-4</span></span>    | <span data-ttu-id="194db-160">L'installazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="194db-160">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="194db-161">Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai chiamata.</span><span class="sxs-lookup"><span data-stu-id="194db-161">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="194db-162">Convalida</span><span class="sxs-lookup"><span data-stu-id="194db-162">Validation</span></span>

<dl>

[<span data-ttu-id="194db-163">ICE03</span><span class="sxs-lookup"><span data-stu-id="194db-163">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="194db-164">ICE06</span><span class="sxs-lookup"><span data-stu-id="194db-164">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="194db-165">ICE12</span><span class="sxs-lookup"><span data-stu-id="194db-165">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="194db-166">ICE13</span><span class="sxs-lookup"><span data-stu-id="194db-166">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="194db-167">ICE26</span><span class="sxs-lookup"><span data-stu-id="194db-167">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="194db-168">ICE27</span><span class="sxs-lookup"><span data-stu-id="194db-168">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="194db-169">ICE28</span><span class="sxs-lookup"><span data-stu-id="194db-169">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="194db-170">ICE75</span><span class="sxs-lookup"><span data-stu-id="194db-170">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="194db-171">ICE77</span><span class="sxs-lookup"><span data-stu-id="194db-171">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="194db-172">ICE79</span><span class="sxs-lookup"><span data-stu-id="194db-172">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="194db-173">ICE82</span><span class="sxs-lookup"><span data-stu-id="194db-173">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="194db-174">ICE84</span><span class="sxs-lookup"><span data-stu-id="194db-174">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="194db-175">ICE86</span><span class="sxs-lookup"><span data-stu-id="194db-175">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="194db-176">ICEM04</span><span class="sxs-lookup"><span data-stu-id="194db-176">ICEM04</span></span>](icem04.md)  
</dl>

 

 



