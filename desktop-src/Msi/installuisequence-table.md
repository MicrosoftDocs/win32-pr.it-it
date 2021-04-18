---
description: Nella tabella InstallUISequence sono elencate le azioni che vengono eseguite quando viene eseguita l'azione di installazione di livello superiore e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Tabella InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317128"
---
# <a name="installuisequence-table"></a><span data-ttu-id="137e8-103">Tabella InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="137e8-103">InstallUISequence Table</span></span>

<span data-ttu-id="137e8-104">Nella tabella InstallUISequence sono elencate le azioni che vengono eseguite quando viene eseguita l' [azione di installazione](install-action.md) di livello superiore e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta.</span><span class="sxs-lookup"><span data-stu-id="137e8-104">The InstallUISequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="137e8-105">Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato su interfaccia utente di base o nessuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="137e8-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="137e8-106">Vedere [informazioni sull'interfaccia utente](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="137e8-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="137e8-107">Le azioni della sequenza di installazione fino all' [azione InstallValidate](installvalidate-action.md)e le finestre di dialogo di uscita si trovano nella tabella InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="137e8-107">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and the exit dialog boxes, are located in the InstallUISequence table.</span></span> <span data-ttu-id="137e8-108">Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione si trovano nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="137e8-108">All actions from the InstallValidate through the end of the install sequence are in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="137e8-109">Poiché è necessario che la tabella InstallExecuteSequence sia autonoma, sono necessarie azioni di inizializzazione, ad esempio [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md), [CostFinalize secondo](costfinalize-action.md)e [ExecuteAction Action](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="137e8-109">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and the [CostFinalize](costfinalize-action.md), and [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="137e8-110">La tabella InstallUISequence include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="137e8-110">The InstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="137e8-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="137e8-111">Column</span></span>    | <span data-ttu-id="137e8-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="137e8-112">Type</span></span>                         | <span data-ttu-id="137e8-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="137e8-113">Key</span></span> | <span data-ttu-id="137e8-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="137e8-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="137e8-115">Azione</span><span class="sxs-lookup"><span data-stu-id="137e8-115">Action</span></span>    | [<span data-ttu-id="137e8-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="137e8-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="137e8-117">S</span><span class="sxs-lookup"><span data-stu-id="137e8-117">Y</span></span>   | <span data-ttu-id="137e8-118">N</span><span class="sxs-lookup"><span data-stu-id="137e8-118">N</span></span>        |
| <span data-ttu-id="137e8-119">Condizione</span><span class="sxs-lookup"><span data-stu-id="137e8-119">Condition</span></span> | [<span data-ttu-id="137e8-120">Condition</span><span class="sxs-lookup"><span data-stu-id="137e8-120">Condition</span></span>](condition.md)   | <span data-ttu-id="137e8-121">N</span><span class="sxs-lookup"><span data-stu-id="137e8-121">N</span></span>   | <span data-ttu-id="137e8-122">S</span><span class="sxs-lookup"><span data-stu-id="137e8-122">Y</span></span>        |
| <span data-ttu-id="137e8-123">Sequenza</span><span class="sxs-lookup"><span data-stu-id="137e8-123">Sequence</span></span>  | [<span data-ttu-id="137e8-124">Integer</span><span class="sxs-lookup"><span data-stu-id="137e8-124">Integer</span></span>](integer.md)       | <span data-ttu-id="137e8-125">N</span><span class="sxs-lookup"><span data-stu-id="137e8-125">N</span></span>   | <span data-ttu-id="137e8-126">S</span><span class="sxs-lookup"><span data-stu-id="137e8-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="137e8-127">Colonne</span><span class="sxs-lookup"><span data-stu-id="137e8-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="137e8-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="137e8-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="137e8-129">Nome dell'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="137e8-129">Name of the action to execute.</span></span> <span data-ttu-id="137e8-130">Si tratta di un'azione predefinita, un'azione personalizzata o una procedura guidata dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="137e8-130">This is either a built-in action, a custom action, or a user interface wizard.</span></span>

<span data-ttu-id="137e8-131">Chiave della tabella primaria.</span><span class="sxs-lookup"><span data-stu-id="137e8-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="137e8-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="137e8-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="137e8-133">Questo campo contiene un'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="137e8-133">This field contains a conditional expression.</span></span> <span data-ttu-id="137e8-134">Se l'espressione restituisce false, l'azione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="137e8-134">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="137e8-135">Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="137e8-135">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="137e8-136">Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="137e8-136">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="137e8-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="137e8-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="137e8-138">Il numero in questa colonna determina la posizione della sequenza in cui viene eseguita l'azione.</span><span class="sxs-lookup"><span data-stu-id="137e8-138">The number in this column determines the sequence position in which this action is run.</span></span>

<span data-ttu-id="137e8-139">Un valore positivo rappresenta la posizione della sequenza.</span><span class="sxs-lookup"><span data-stu-id="137e8-139">A positive value represents the sequence position.</span></span> <span data-ttu-id="137e8-140">Un valore null indica che l'azione non viene mai eseguita.</span><span class="sxs-lookup"><span data-stu-id="137e8-140">A Null value indicates that the action is never run.</span></span> <span data-ttu-id="137e8-141">I seguenti valori negativi indicano che questa azione viene eseguita se il programma di installazione restituisce il flag di terminazione associato.</span><span class="sxs-lookup"><span data-stu-id="137e8-141">The following negative values indicate that this action is executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="137e8-142">Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione.</span><span class="sxs-lookup"><span data-stu-id="137e8-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="137e8-143">Più azioni possono avere flag di terminazione, ma devono essere flag diversi.</span><span class="sxs-lookup"><span data-stu-id="137e8-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="137e8-144">I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="137e8-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="137e8-145">Flag di terminazione</span><span class="sxs-lookup"><span data-stu-id="137e8-145">Termination flag</span></span>          | <span data-ttu-id="137e8-146">Valore</span><span class="sxs-lookup"><span data-stu-id="137e8-146">Value</span></span> | <span data-ttu-id="137e8-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="137e8-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="137e8-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="137e8-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="137e8-149">-1</span><span class="sxs-lookup"><span data-stu-id="137e8-149">-1</span></span>    | <span data-ttu-id="137e8-150">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="137e8-150">Successful completion.</span></span> <span data-ttu-id="137e8-151">Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="137e8-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="137e8-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="137e8-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="137e8-153">-2</span><span class="sxs-lookup"><span data-stu-id="137e8-153">-2</span></span>    | <span data-ttu-id="137e8-154">L'utente termina l'installazione.</span><span class="sxs-lookup"><span data-stu-id="137e8-154">User terminates install.</span></span> <span data-ttu-id="137e8-155">Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="137e8-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="137e8-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="137e8-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="137e8-157">-3</span><span class="sxs-lookup"><span data-stu-id="137e8-157">-3</span></span>    | <span data-ttu-id="137e8-158">Terminazione irreversibile.</span><span class="sxs-lookup"><span data-stu-id="137e8-158">Fatal exit terminates.</span></span> <span data-ttu-id="137e8-159">Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="137e8-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="137e8-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="137e8-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="137e8-161">-4</span><span class="sxs-lookup"><span data-stu-id="137e8-161">-4</span></span>    | <span data-ttu-id="137e8-162">L'installazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="137e8-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="137e8-163">Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai eseguita.</span><span class="sxs-lookup"><span data-stu-id="137e8-163">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="137e8-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="137e8-164">Remarks</span></span>

<span data-ttu-id="137e8-165">Il testo localizzato associato per la visualizzazione o la registrazione dello stato di avanzamento è specificato nella [tabella ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="137e8-165">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="137e8-166">Per un esempio di una tabella di sequenza, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="137e8-166">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="137e8-167">Convalida</span><span class="sxs-lookup"><span data-stu-id="137e8-167">Validation</span></span>

<dl>

[<span data-ttu-id="137e8-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="137e8-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="137e8-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="137e8-169">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="137e8-170">ICE12</span><span class="sxs-lookup"><span data-stu-id="137e8-170">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="137e8-171">ICE13</span><span class="sxs-lookup"><span data-stu-id="137e8-171">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="137e8-172">ICE20</span><span class="sxs-lookup"><span data-stu-id="137e8-172">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="137e8-173">ICE26</span><span class="sxs-lookup"><span data-stu-id="137e8-173">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="137e8-174">ICE27</span><span class="sxs-lookup"><span data-stu-id="137e8-174">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="137e8-175">ICE28</span><span class="sxs-lookup"><span data-stu-id="137e8-175">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="137e8-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="137e8-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="137e8-177">ICE75</span><span class="sxs-lookup"><span data-stu-id="137e8-177">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="137e8-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="137e8-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="137e8-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="137e8-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="137e8-180">ICE86</span><span class="sxs-lookup"><span data-stu-id="137e8-180">ICE86</span></span>](ice86.md)  
</dl>

 

 



