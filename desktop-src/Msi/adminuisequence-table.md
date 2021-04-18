---
description: Nella tabella AdminUISequence sono elencate le azioni che il programma di installazione chiama in sequenza quando viene eseguita l'azione di amministrazione di primo livello e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Tabella AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311069"
---
# <a name="adminuisequence-table"></a><span data-ttu-id="266aa-103">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="266aa-103">AdminUISequence Table</span></span>

<span data-ttu-id="266aa-104">Nella tabella AdminUISequence sono elencate le azioni che il programma di installazione chiama in sequenza quando viene eseguita l' [azione di amministrazione](admin-action.md) di primo livello e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta.</span><span class="sxs-lookup"><span data-stu-id="266aa-104">The AdminUISequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="266aa-105">Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato su interfaccia utente di base o nessuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="266aa-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="266aa-106">Vedere [informazioni sull'interfaccia utente](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="266aa-107">Le azioni amministrative nella sequenza di installazione fino all' [azione InstallValidate](installvalidate-action.md)e alle finestre di dialogo di uscita si trovano nella tabella AdminUISequence.</span><span class="sxs-lookup"><span data-stu-id="266aa-107">ADMIN actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the AdminUISequence table.</span></span> <span data-ttu-id="266aa-108">Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione si trovano nella [tabella AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-108">All actions from the InstallValidate through the end of the install sequence are in the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="266aa-109">Poiché la tabella AdminExecuteSequence deve essere autonoma, contiene anche tutte le azioni di inizializzazione necessarie, ad esempio [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-109">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span> <span data-ttu-id="266aa-110">Include anche l' [azione ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-110">It also has the [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="266aa-111">Le colonne sono identiche a quelle della [tabella InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-111">The columns are identical to those of the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="266aa-112">La tabella AdminUISequence include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="266aa-112">The AdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="266aa-113">Colonna</span><span class="sxs-lookup"><span data-stu-id="266aa-113">Column</span></span>    | <span data-ttu-id="266aa-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="266aa-114">Type</span></span>                         | <span data-ttu-id="266aa-115">Chiave</span><span class="sxs-lookup"><span data-stu-id="266aa-115">Key</span></span> | <span data-ttu-id="266aa-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="266aa-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="266aa-117">Azione</span><span class="sxs-lookup"><span data-stu-id="266aa-117">Action</span></span>    | [<span data-ttu-id="266aa-118">Identificatore</span><span class="sxs-lookup"><span data-stu-id="266aa-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="266aa-119">S</span><span class="sxs-lookup"><span data-stu-id="266aa-119">Y</span></span>   | <span data-ttu-id="266aa-120">N</span><span class="sxs-lookup"><span data-stu-id="266aa-120">N</span></span>        |
| <span data-ttu-id="266aa-121">Condizione</span><span class="sxs-lookup"><span data-stu-id="266aa-121">Condition</span></span> | [<span data-ttu-id="266aa-122">Condition</span><span class="sxs-lookup"><span data-stu-id="266aa-122">Condition</span></span>](condition.md)   | <span data-ttu-id="266aa-123">N</span><span class="sxs-lookup"><span data-stu-id="266aa-123">N</span></span>   | <span data-ttu-id="266aa-124">S</span><span class="sxs-lookup"><span data-stu-id="266aa-124">Y</span></span>        |
| <span data-ttu-id="266aa-125">Sequenza</span><span class="sxs-lookup"><span data-stu-id="266aa-125">Sequence</span></span>  | [<span data-ttu-id="266aa-126">Integer</span><span class="sxs-lookup"><span data-stu-id="266aa-126">Integer</span></span>](integer.md)       | <span data-ttu-id="266aa-127">N</span><span class="sxs-lookup"><span data-stu-id="266aa-127">N</span></span>   | <span data-ttu-id="266aa-128">S</span><span class="sxs-lookup"><span data-stu-id="266aa-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="266aa-129">Colonne</span><span class="sxs-lookup"><span data-stu-id="266aa-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="266aa-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="266aa-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="266aa-131">Nome dell'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="266aa-131">Name of the action to execute.</span></span> <span data-ttu-id="266aa-132">Si tratta di un'azione standard, di una procedura guidata dell'interfaccia utente o di un'azione personalizzata elencata nella [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-132">This is either a standard action, a user interface wizard, or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="266aa-133">Chiave della tabella primaria.</span><span class="sxs-lookup"><span data-stu-id="266aa-133">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="266aa-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="266aa-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="266aa-135">Espressione logica.</span><span class="sxs-lookup"><span data-stu-id="266aa-135">Logical expression.</span></span> <span data-ttu-id="266aa-136">Se l'espressione restituisce false, l'azione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="266aa-136">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="266aa-137">Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="266aa-137">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="266aa-138">Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-138">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="266aa-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="266aa-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="266aa-140">Un valore positivo indica la posizione della sequenza dell'azione.</span><span class="sxs-lookup"><span data-stu-id="266aa-140">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="266aa-141">I valori negativi seguenti indicano che l'azione viene chiamata se il programma di installazione restituisce il flag di terminazione.</span><span class="sxs-lookup"><span data-stu-id="266aa-141">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="266aa-142">Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione.</span><span class="sxs-lookup"><span data-stu-id="266aa-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="266aa-143">Più azioni possono avere flag di terminazione, ma devono essere flag diversi.</span><span class="sxs-lookup"><span data-stu-id="266aa-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="266aa-144">I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="266aa-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="266aa-145">Flag di terminazione</span><span class="sxs-lookup"><span data-stu-id="266aa-145">Termination flag</span></span>          | <span data-ttu-id="266aa-146">Valore</span><span class="sxs-lookup"><span data-stu-id="266aa-146">Value</span></span> | <span data-ttu-id="266aa-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="266aa-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="266aa-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="266aa-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="266aa-149">-1</span><span class="sxs-lookup"><span data-stu-id="266aa-149">-1</span></span>    | <span data-ttu-id="266aa-150">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="266aa-150">Successful completion.</span></span> <span data-ttu-id="266aa-151">Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="266aa-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="266aa-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="266aa-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="266aa-153">-2</span><span class="sxs-lookup"><span data-stu-id="266aa-153">-2</span></span>    | <span data-ttu-id="266aa-154">L'utente termina l'installazione.</span><span class="sxs-lookup"><span data-stu-id="266aa-154">User terminates install.</span></span> <span data-ttu-id="266aa-155">Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="266aa-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="266aa-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="266aa-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="266aa-157">-3</span><span class="sxs-lookup"><span data-stu-id="266aa-157">-3</span></span>    | <span data-ttu-id="266aa-158">Terminazione irreversibile.</span><span class="sxs-lookup"><span data-stu-id="266aa-158">Fatal exit terminates.</span></span> <span data-ttu-id="266aa-159">Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="266aa-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="266aa-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="266aa-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="266aa-161">-4</span><span class="sxs-lookup"><span data-stu-id="266aa-161">-4</span></span>    | <span data-ttu-id="266aa-162">L'installazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="266aa-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="266aa-163">Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai chiamata.</span><span class="sxs-lookup"><span data-stu-id="266aa-163">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="266aa-164">Convalida</span><span class="sxs-lookup"><span data-stu-id="266aa-164">Validation</span></span>

<dl>

[<span data-ttu-id="266aa-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="266aa-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="266aa-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="266aa-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="266aa-167">ICE12</span><span class="sxs-lookup"><span data-stu-id="266aa-167">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="266aa-168">ICE13</span><span class="sxs-lookup"><span data-stu-id="266aa-168">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="266aa-169">ICE20</span><span class="sxs-lookup"><span data-stu-id="266aa-169">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="266aa-170">ICE26</span><span class="sxs-lookup"><span data-stu-id="266aa-170">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="266aa-171">ICE27</span><span class="sxs-lookup"><span data-stu-id="266aa-171">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="266aa-172">ICE28</span><span class="sxs-lookup"><span data-stu-id="266aa-172">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="266aa-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="266aa-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="266aa-174">ICE75</span><span class="sxs-lookup"><span data-stu-id="266aa-174">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="266aa-175">ICE79</span><span class="sxs-lookup"><span data-stu-id="266aa-175">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="266aa-176">ICE82</span><span class="sxs-lookup"><span data-stu-id="266aa-176">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="266aa-177">ICE84</span><span class="sxs-lookup"><span data-stu-id="266aa-177">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="266aa-178">ICE86</span><span class="sxs-lookup"><span data-stu-id="266aa-178">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="266aa-179">ICE96</span><span class="sxs-lookup"><span data-stu-id="266aa-179">ICE96</span></span>](ice96.md)  
[<span data-ttu-id="266aa-180">ICEM04</span><span class="sxs-lookup"><span data-stu-id="266aa-180">ICEM04</span></span>](icem04.md)  
</dl>

 

 



