---
description: Nella tabella AdvtExecuteSequence sono elencate le azioni che il programma di installazione chiama quando viene eseguita l'azione di annuncio di primo livello.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabella AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881149"
---
# <a name="advtexecutesequence-table"></a><span data-ttu-id="0801b-103">Tabella AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="0801b-103">AdvtExecuteSequence Table</span></span>

<span data-ttu-id="0801b-104">Nella tabella AdvtExecuteSequence sono elencate le azioni che il programma di installazione chiama quando viene eseguita l' [azione di annuncio](advertise-action.md) di primo livello.</span><span class="sxs-lookup"><span data-stu-id="0801b-104">The AdvtExecuteSequence table lists actions the installer calls when the top-level [ADVERTISE action](advertise-action.md) is executed.</span></span>

<span data-ttu-id="0801b-105">Nella tabella AdvtExecuteSequence è possibile utilizzare solo le azioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0801b-105">Only the following actions can be used in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="0801b-106">Non è possibile usare azioni personalizzate in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="0801b-106">Custom actions cannot be used in this table.</span></span>

[<span data-ttu-id="0801b-107">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="0801b-107">CostFinalize</span></span>](costfinalize-action.md)

[<span data-ttu-id="0801b-108">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="0801b-108">CostInitialize</span></span>](costinitialize-action.md)

[<span data-ttu-id="0801b-109">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="0801b-109">CreateShortcuts</span></span>](createshortcuts-action.md)

[<span data-ttu-id="0801b-110">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="0801b-110">InstallFinalize</span></span>](installfinalize-action.md)

[<span data-ttu-id="0801b-111">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="0801b-111">InstallInitialize</span></span>](installinitialize-action.md)

[<span data-ttu-id="0801b-112">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="0801b-112">InstallValidate</span></span>](installvalidate-action.md)

[<span data-ttu-id="0801b-113">MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="0801b-113">MsiPublishAssemblies</span></span>](msipublishassemblies-action.md)

[<span data-ttu-id="0801b-114">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="0801b-114">PublishComponents</span></span>](publishcomponents-action.md)

[<span data-ttu-id="0801b-115">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="0801b-115">PublishFeatures</span></span>](publishfeatures-action.md)

[<span data-ttu-id="0801b-116">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="0801b-116">PublishProduct</span></span>](publishproduct-action.md)

[<span data-ttu-id="0801b-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="0801b-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)

[<span data-ttu-id="0801b-118">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="0801b-118">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)

[<span data-ttu-id="0801b-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="0801b-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

[<span data-ttu-id="0801b-120">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="0801b-120">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="0801b-121">Le colonne sono identiche a quelle della [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="0801b-121">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="0801b-122">La tabella AdvtExecuteSequence include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="0801b-122">The AdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="0801b-123">Colonna</span><span class="sxs-lookup"><span data-stu-id="0801b-123">Column</span></span>    | <span data-ttu-id="0801b-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="0801b-124">Type</span></span>                         | <span data-ttu-id="0801b-125">Chiave</span><span class="sxs-lookup"><span data-stu-id="0801b-125">Key</span></span> | <span data-ttu-id="0801b-126">Nullable</span><span class="sxs-lookup"><span data-stu-id="0801b-126">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="0801b-127">Azione</span><span class="sxs-lookup"><span data-stu-id="0801b-127">Action</span></span>    | [<span data-ttu-id="0801b-128">Identificatore</span><span class="sxs-lookup"><span data-stu-id="0801b-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="0801b-129">S</span><span class="sxs-lookup"><span data-stu-id="0801b-129">Y</span></span>   | <span data-ttu-id="0801b-130">N</span><span class="sxs-lookup"><span data-stu-id="0801b-130">N</span></span>        |
| <span data-ttu-id="0801b-131">Condizione</span><span class="sxs-lookup"><span data-stu-id="0801b-131">Condition</span></span> | [<span data-ttu-id="0801b-132">Condition</span><span class="sxs-lookup"><span data-stu-id="0801b-132">Condition</span></span>](condition.md)   | <span data-ttu-id="0801b-133">N</span><span class="sxs-lookup"><span data-stu-id="0801b-133">N</span></span>   | <span data-ttu-id="0801b-134">S</span><span class="sxs-lookup"><span data-stu-id="0801b-134">Y</span></span>        |
| <span data-ttu-id="0801b-135">Sequenza</span><span class="sxs-lookup"><span data-stu-id="0801b-135">Sequence</span></span>  | [<span data-ttu-id="0801b-136">Integer</span><span class="sxs-lookup"><span data-stu-id="0801b-136">Integer</span></span>](integer.md)       | <span data-ttu-id="0801b-137">N</span><span class="sxs-lookup"><span data-stu-id="0801b-137">N</span></span>   | <span data-ttu-id="0801b-138">S</span><span class="sxs-lookup"><span data-stu-id="0801b-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0801b-139">Colonne</span><span class="sxs-lookup"><span data-stu-id="0801b-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0801b-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="0801b-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="0801b-141">Nome dell' [azione standard](standard-actions.md) che deve essere eseguita dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="0801b-141">Name of the [standard action](standard-actions.md) the installer is to execute.</span></span> <span data-ttu-id="0801b-142">Si tratta della chiave primaria della tabella.</span><span class="sxs-lookup"><span data-stu-id="0801b-142">This is the primary key of the table.</span></span>

</dd> <dt>

<span data-ttu-id="0801b-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="0801b-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="0801b-144">Espressione logica.</span><span class="sxs-lookup"><span data-stu-id="0801b-144">Logical expression.</span></span> <span data-ttu-id="0801b-145">Se l'espressione restituisce false, l'azione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0801b-145">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="0801b-146">Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="0801b-146">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="0801b-147">Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="0801b-147">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="0801b-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="0801b-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="0801b-149">Un valore positivo indica la posizione della sequenza dell'azione.</span><span class="sxs-lookup"><span data-stu-id="0801b-149">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="0801b-150">I valori negativi seguenti indicano che l'azione viene chiamata se il programma di installazione restituisce il flag di terminazione.</span><span class="sxs-lookup"><span data-stu-id="0801b-150">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="0801b-151">Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione.</span><span class="sxs-lookup"><span data-stu-id="0801b-151">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="0801b-152">Più azioni possono avere flag di terminazione, ma devono essere flag diversi.</span><span class="sxs-lookup"><span data-stu-id="0801b-152">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="0801b-153">I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="0801b-153">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="0801b-154">Flag di terminazione</span><span class="sxs-lookup"><span data-stu-id="0801b-154">Termination flag</span></span>          | <span data-ttu-id="0801b-155">Valore</span><span class="sxs-lookup"><span data-stu-id="0801b-155">Value</span></span> | <span data-ttu-id="0801b-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0801b-156">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0801b-157">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="0801b-157">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="0801b-158">-1</span><span class="sxs-lookup"><span data-stu-id="0801b-158">-1</span></span>    | <span data-ttu-id="0801b-159">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="0801b-159">Successful completion.</span></span> <span data-ttu-id="0801b-160">Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="0801b-160">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="0801b-161">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="0801b-161">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="0801b-162">-2</span><span class="sxs-lookup"><span data-stu-id="0801b-162">-2</span></span>    | <span data-ttu-id="0801b-163">L'utente termina l'installazione.</span><span class="sxs-lookup"><span data-stu-id="0801b-163">User terminates install.</span></span> <span data-ttu-id="0801b-164">Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="0801b-164">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="0801b-165">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="0801b-165">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="0801b-166">-3</span><span class="sxs-lookup"><span data-stu-id="0801b-166">-3</span></span>    | <span data-ttu-id="0801b-167">Terminazione irreversibile.</span><span class="sxs-lookup"><span data-stu-id="0801b-167">Fatal exit terminates.</span></span> <span data-ttu-id="0801b-168">Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="0801b-168">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="0801b-169">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="0801b-169">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="0801b-170">-4</span><span class="sxs-lookup"><span data-stu-id="0801b-170">-4</span></span>    | <span data-ttu-id="0801b-171">L'installazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="0801b-171">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="0801b-172">Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai chiamata.</span><span class="sxs-lookup"><span data-stu-id="0801b-172">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="0801b-173">Convalida</span><span class="sxs-lookup"><span data-stu-id="0801b-173">Validation</span></span>

<dl>

[<span data-ttu-id="0801b-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="0801b-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0801b-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="0801b-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0801b-176">ICE12</span><span class="sxs-lookup"><span data-stu-id="0801b-176">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="0801b-177">ICE13</span><span class="sxs-lookup"><span data-stu-id="0801b-177">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="0801b-178">ICE27</span><span class="sxs-lookup"><span data-stu-id="0801b-178">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="0801b-179">ICE46</span><span class="sxs-lookup"><span data-stu-id="0801b-179">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="0801b-180">ICE72</span><span class="sxs-lookup"><span data-stu-id="0801b-180">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="0801b-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="0801b-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="0801b-182">ICE82</span><span class="sxs-lookup"><span data-stu-id="0801b-182">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="0801b-183">ICE83</span><span class="sxs-lookup"><span data-stu-id="0801b-183">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="0801b-184">ICE84</span><span class="sxs-lookup"><span data-stu-id="0801b-184">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="0801b-185">ICE86</span><span class="sxs-lookup"><span data-stu-id="0801b-185">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="0801b-186">ICEM04</span><span class="sxs-lookup"><span data-stu-id="0801b-186">ICEM04</span></span>](icem04.md)  
</dl>

 

 



