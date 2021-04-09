---
description: Nella tabella InstallExecuteSequence sono elencate le azioni che vengono eseguite quando viene eseguita l'azione di installazione di livello superiore.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Tabella InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878986"
---
# <a name="installexecutesequence-table"></a><span data-ttu-id="cd197-103">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="cd197-103">InstallExecuteSequence Table</span></span>

<span data-ttu-id="cd197-104">Nella tabella InstallExecuteSequence sono elencate le azioni che vengono eseguite quando viene eseguita l' [azione di installazione](install-action.md) di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cd197-104">The InstallExecuteSequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed.</span></span>

<span data-ttu-id="cd197-105">Le azioni nella sequenza di installazione fino all' [azione InstallValidate](installvalidate-action.md)e a tutte le finestre di dialogo di uscita si trovano nella [tabella InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd197-105">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="cd197-106">Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione si trovano nella tabella InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="cd197-106">All actions from the InstallValidate through the end of the install sequence are in the InstallExecuteSequence table.</span></span> <span data-ttu-id="cd197-107">Poiché è necessario che la tabella InstallExecuteSequence sia autonoma, sono necessarie azioni di inizializzazione, ad esempio [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cd197-107">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="cd197-108">Le [azioni personalizzate](custom-actions.md) che richiedono un'interfaccia utente devono usare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anziché le finestre di dialogo Create con la [tabella della finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd197-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="cd197-109">La tabella InstallExecuteSequence include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd197-109">The InstallExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="cd197-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="cd197-110">Column</span></span>    | <span data-ttu-id="cd197-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd197-111">Type</span></span>                         | <span data-ttu-id="cd197-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="cd197-112">Key</span></span> | <span data-ttu-id="cd197-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="cd197-113">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="cd197-114">Azione</span><span class="sxs-lookup"><span data-stu-id="cd197-114">Action</span></span>    | [<span data-ttu-id="cd197-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="cd197-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="cd197-116">S</span><span class="sxs-lookup"><span data-stu-id="cd197-116">Y</span></span>   | <span data-ttu-id="cd197-117">N</span><span class="sxs-lookup"><span data-stu-id="cd197-117">N</span></span>        |
| <span data-ttu-id="cd197-118">Condizione</span><span class="sxs-lookup"><span data-stu-id="cd197-118">Condition</span></span> | [<span data-ttu-id="cd197-119">Condition</span><span class="sxs-lookup"><span data-stu-id="cd197-119">Condition</span></span>](condition.md)   | <span data-ttu-id="cd197-120">N</span><span class="sxs-lookup"><span data-stu-id="cd197-120">N</span></span>   | <span data-ttu-id="cd197-121">S</span><span class="sxs-lookup"><span data-stu-id="cd197-121">Y</span></span>        |
| <span data-ttu-id="cd197-122">Sequenza</span><span class="sxs-lookup"><span data-stu-id="cd197-122">Sequence</span></span>  | [<span data-ttu-id="cd197-123">Integer</span><span class="sxs-lookup"><span data-stu-id="cd197-123">Integer</span></span>](integer.md)       | <span data-ttu-id="cd197-124">N</span><span class="sxs-lookup"><span data-stu-id="cd197-124">N</span></span>   | <span data-ttu-id="cd197-125">S</span><span class="sxs-lookup"><span data-stu-id="cd197-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cd197-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="cd197-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cd197-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="cd197-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="cd197-128">Nome dell'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="cd197-128">Name of the action to execute.</span></span> <span data-ttu-id="cd197-129">Si tratta di un'azione predefinita o di un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="cd197-129">This is either a built-in action or a custom action.</span></span>

<span data-ttu-id="cd197-130">Chiave della tabella primaria.</span><span class="sxs-lookup"><span data-stu-id="cd197-130">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="cd197-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="cd197-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="cd197-132">Questo campo contiene un'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="cd197-132">This field contains a conditional expression.</span></span> <span data-ttu-id="cd197-133">Se l'espressione restituisce false, l'azione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="cd197-133">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="cd197-134">Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="cd197-134">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="cd197-135">Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cd197-135">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd197-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="cd197-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="cd197-137">Numero che determina la posizione della sequenza in cui deve essere eseguita l'azione.</span><span class="sxs-lookup"><span data-stu-id="cd197-137">Number that determines the sequence position in which this action is to be executed.</span></span>

<span data-ttu-id="cd197-138">Un valore positivo rappresenta la posizione della sequenza.</span><span class="sxs-lookup"><span data-stu-id="cd197-138">A positive value represents the sequence position.</span></span> <span data-ttu-id="cd197-139">Un valore null indica che l'azione non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="cd197-139">A Null value indicates that the action is not executed.</span></span> <span data-ttu-id="cd197-140">I seguenti valori negativi indicano che questa azione deve essere eseguita se il programma di installazione restituisce il flag di terminazione associato.</span><span class="sxs-lookup"><span data-stu-id="cd197-140">The following negative values indicate that this action is to be executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="cd197-141">Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione.</span><span class="sxs-lookup"><span data-stu-id="cd197-141">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="cd197-142">Più azioni possono avere flag di terminazione, ma devono essere flag diversi.</span><span class="sxs-lookup"><span data-stu-id="cd197-142">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="cd197-143">I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cd197-143">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="cd197-144">Flag di terminazione</span><span class="sxs-lookup"><span data-stu-id="cd197-144">Termination flag</span></span>          | <span data-ttu-id="cd197-145">Valore</span><span class="sxs-lookup"><span data-stu-id="cd197-145">Value</span></span> | <span data-ttu-id="cd197-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd197-146">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd197-147">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="cd197-147">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="cd197-148">-1</span><span class="sxs-lookup"><span data-stu-id="cd197-148">-1</span></span>    | <span data-ttu-id="cd197-149">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="cd197-149">Successful completion.</span></span> <span data-ttu-id="cd197-150">Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="cd197-150">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="cd197-151">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="cd197-151">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="cd197-152">-2</span><span class="sxs-lookup"><span data-stu-id="cd197-152">-2</span></span>    | <span data-ttu-id="cd197-153">L'utente termina l'installazione.</span><span class="sxs-lookup"><span data-stu-id="cd197-153">User terminates install.</span></span> <span data-ttu-id="cd197-154">Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="cd197-154">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="cd197-155">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="cd197-155">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="cd197-156">-3</span><span class="sxs-lookup"><span data-stu-id="cd197-156">-3</span></span>    | <span data-ttu-id="cd197-157">Terminazione irreversibile.</span><span class="sxs-lookup"><span data-stu-id="cd197-157">Fatal exit terminates.</span></span> <span data-ttu-id="cd197-158">Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="cd197-158">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="cd197-159">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="cd197-159">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="cd197-160">-4</span><span class="sxs-lookup"><span data-stu-id="cd197-160">-4</span></span>    | <span data-ttu-id="cd197-161">L'installazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="cd197-161">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="cd197-162">Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai eseguita.</span><span class="sxs-lookup"><span data-stu-id="cd197-162">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd197-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd197-163">Remarks</span></span>

<span data-ttu-id="cd197-164">Il testo localizzato per la visualizzazione o la registrazione dello stato di avanzamento è specificato nella [tabella ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd197-164">Localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="cd197-165">Per un esempio di una tabella di sequenza, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd197-165">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="cd197-166">Convalida</span><span class="sxs-lookup"><span data-stu-id="cd197-166">Validation</span></span>

<dl>

[<span data-ttu-id="cd197-167">ICE03</span><span class="sxs-lookup"><span data-stu-id="cd197-167">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cd197-168">ICE06</span><span class="sxs-lookup"><span data-stu-id="cd197-168">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cd197-169">ICE12</span><span class="sxs-lookup"><span data-stu-id="cd197-169">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="cd197-170">ICE13</span><span class="sxs-lookup"><span data-stu-id="cd197-170">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="cd197-171">ICE26</span><span class="sxs-lookup"><span data-stu-id="cd197-171">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="cd197-172">ICE27</span><span class="sxs-lookup"><span data-stu-id="cd197-172">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="cd197-173">ICE28</span><span class="sxs-lookup"><span data-stu-id="cd197-173">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="cd197-174">ICE46</span><span class="sxs-lookup"><span data-stu-id="cd197-174">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="cd197-175">ICE63</span><span class="sxs-lookup"><span data-stu-id="cd197-175">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="cd197-176">ICE75</span><span class="sxs-lookup"><span data-stu-id="cd197-176">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="cd197-177">ICE77</span><span class="sxs-lookup"><span data-stu-id="cd197-177">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="cd197-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="cd197-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="cd197-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="cd197-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="cd197-180">ICE83</span><span class="sxs-lookup"><span data-stu-id="cd197-180">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="cd197-181">ICE84</span><span class="sxs-lookup"><span data-stu-id="cd197-181">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="cd197-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="cd197-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



