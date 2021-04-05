---
description: La tabella ControlCondition consente a un autore di specificare azioni speciali da applicare ai controlli in base al risultato di un'istruzione condizionale. Se ad esempio si usa questa tabella, l'autore può scegliere di nascondere un controllo in base alla proprietà VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabella ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967909"
---
# <a name="controlcondition-table"></a><span data-ttu-id="36a3f-104">Tabella ControlCondition</span><span class="sxs-lookup"><span data-stu-id="36a3f-104">ControlCondition Table</span></span>

<span data-ttu-id="36a3f-105">La tabella ControlCondition consente a un autore di specificare azioni speciali da applicare ai controlli in base al risultato di un'istruzione condizionale.</span><span class="sxs-lookup"><span data-stu-id="36a3f-105">The ControlCondition table enables an author to specify special actions to be applied to controls based on the result of a conditional statement.</span></span> <span data-ttu-id="36a3f-106">Se ad esempio si usa questa tabella, l'autore può scegliere di nascondere un controllo in base alla proprietà [**VersionNT**](versionnt.md) .</span><span class="sxs-lookup"><span data-stu-id="36a3f-106">For example, using this table the author could choose to hide a control based on the [**VersionNT**](versionnt.md) property.</span></span>

<span data-ttu-id="36a3f-107">La tabella ControlCondition include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="36a3f-107">The ControlCondition table has the following columns.</span></span>



| <span data-ttu-id="36a3f-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="36a3f-108">Column</span></span>    | <span data-ttu-id="36a3f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="36a3f-109">Type</span></span>                         | <span data-ttu-id="36a3f-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="36a3f-110">Key</span></span> | <span data-ttu-id="36a3f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="36a3f-111">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="36a3f-112">Finestra di dialogo\_</span><span class="sxs-lookup"><span data-stu-id="36a3f-112">Dialog\_</span></span>  | [<span data-ttu-id="36a3f-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="36a3f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="36a3f-114">S</span><span class="sxs-lookup"><span data-stu-id="36a3f-114">Y</span></span>   | <span data-ttu-id="36a3f-115">N</span><span class="sxs-lookup"><span data-stu-id="36a3f-115">N</span></span>        |
| <span data-ttu-id="36a3f-116">controllo\_</span><span class="sxs-lookup"><span data-stu-id="36a3f-116">Control\_</span></span> | [<span data-ttu-id="36a3f-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="36a3f-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="36a3f-118">S</span><span class="sxs-lookup"><span data-stu-id="36a3f-118">Y</span></span>   | <span data-ttu-id="36a3f-119">N</span><span class="sxs-lookup"><span data-stu-id="36a3f-119">N</span></span>        |
| <span data-ttu-id="36a3f-120">Azione</span><span class="sxs-lookup"><span data-stu-id="36a3f-120">Action</span></span>    | [<span data-ttu-id="36a3f-121">Text</span><span class="sxs-lookup"><span data-stu-id="36a3f-121">Text</span></span>](text.md)             | <span data-ttu-id="36a3f-122">S</span><span class="sxs-lookup"><span data-stu-id="36a3f-122">Y</span></span>   | <span data-ttu-id="36a3f-123">N</span><span class="sxs-lookup"><span data-stu-id="36a3f-123">N</span></span>        |
| <span data-ttu-id="36a3f-124">Condizione</span><span class="sxs-lookup"><span data-stu-id="36a3f-124">Condition</span></span> | [<span data-ttu-id="36a3f-125">Condition</span><span class="sxs-lookup"><span data-stu-id="36a3f-125">Condition</span></span>](condition.md)   | <span data-ttu-id="36a3f-126">S</span><span class="sxs-lookup"><span data-stu-id="36a3f-126">Y</span></span>   | <span data-ttu-id="36a3f-127">N</span><span class="sxs-lookup"><span data-stu-id="36a3f-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="36a3f-128">Colonne</span><span class="sxs-lookup"><span data-stu-id="36a3f-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="36a3f-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_</span><span class="sxs-lookup"><span data-stu-id="36a3f-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="36a3f-130">Chiave esterna per la prima colonna della tabella della [finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="36a3f-130">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="36a3f-131">La combinazione di questo campo con il campo del controllo \_ identifica un controllo univoco.</span><span class="sxs-lookup"><span data-stu-id="36a3f-131">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="36a3f-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_</span><span class="sxs-lookup"><span data-stu-id="36a3f-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="36a3f-133">Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="36a3f-133">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="36a3f-134">Combinando questo campo \_ , il campo finestra di dialogo identifica un controllo univoco.</span><span class="sxs-lookup"><span data-stu-id="36a3f-134">Combining this field the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="36a3f-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="36a3f-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="36a3f-136">Azione da intraprendere sul controllo.</span><span class="sxs-lookup"><span data-stu-id="36a3f-136">The action that is to be taken on the control.</span></span> <span data-ttu-id="36a3f-137">Le azioni possibili sono illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="36a3f-137">The possible actions are shown in the following table.</span></span>



| <span data-ttu-id="36a3f-138">Valore</span><span class="sxs-lookup"><span data-stu-id="36a3f-138">Value</span></span>   | <span data-ttu-id="36a3f-139">Significato</span><span class="sxs-lookup"><span data-stu-id="36a3f-139">Meaning</span></span>                     |
|---------|-----------------------------|
| <span data-ttu-id="36a3f-140">Predefinito</span><span class="sxs-lookup"><span data-stu-id="36a3f-140">Default</span></span> | <span data-ttu-id="36a3f-141">Impostare il controllo come predefinito.</span><span class="sxs-lookup"><span data-stu-id="36a3f-141">Set control as the default.</span></span> |
| <span data-ttu-id="36a3f-142">Disabilita</span><span class="sxs-lookup"><span data-stu-id="36a3f-142">Disable</span></span> | <span data-ttu-id="36a3f-143">Disabilitare il controllo.</span><span class="sxs-lookup"><span data-stu-id="36a3f-143">Disable the control.</span></span>        |
| <span data-ttu-id="36a3f-144">Abilitare</span><span class="sxs-lookup"><span data-stu-id="36a3f-144">Enable</span></span>  | <span data-ttu-id="36a3f-145">Abilitare il controllo.</span><span class="sxs-lookup"><span data-stu-id="36a3f-145">Enable the control.</span></span>         |
| <span data-ttu-id="36a3f-146">Nascondi</span><span class="sxs-lookup"><span data-stu-id="36a3f-146">Hide</span></span>    | <span data-ttu-id="36a3f-147">Nascondere il controllo.</span><span class="sxs-lookup"><span data-stu-id="36a3f-147">Hide the control.</span></span>           |
| <span data-ttu-id="36a3f-148">Mostra</span><span class="sxs-lookup"><span data-stu-id="36a3f-148">Show</span></span>    | <span data-ttu-id="36a3f-149">Visualizzare il controllo.</span><span class="sxs-lookup"><span data-stu-id="36a3f-149">Display the control.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="36a3f-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="36a3f-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="36a3f-151">Istruzione condizionale che specifica le condizioni in base alle quali deve essere attivata l'azione.</span><span class="sxs-lookup"><span data-stu-id="36a3f-151">A conditional statement that specifies under which conditions the action should be triggered.</span></span> <span data-ttu-id="36a3f-152">Questa colonna non può essere lasciata vuota.</span><span class="sxs-lookup"><span data-stu-id="36a3f-152">This column may not be left blank.</span></span> <span data-ttu-id="36a3f-153">Se questa istruzione non restituisce TRUE, l'azione non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="36a3f-153">If this statement does not evaluate to TRUE, the action does not take place.</span></span> <span data-ttu-id="36a3f-154">Se è impostato su 1, l'azione viene sempre applicata.</span><span class="sxs-lookup"><span data-stu-id="36a3f-154">If it is set to 1, the action is always applied.</span></span> <span data-ttu-id="36a3f-155">Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="36a3f-155">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36a3f-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="36a3f-156">Remarks</span></span>

<span data-ttu-id="36a3f-157">Se si desidera nascondere e disabilitare un controllo [pulsante](pushbutton-control.md) o una [casella di controllo](checkbox-control.md) in base a un'istruzione condizionale nel campo condizione della tabella ControlCondition, è necessario utilizzare quattro record per ogni controllo per disabilitare e nascondere il controllo.</span><span class="sxs-lookup"><span data-stu-id="36a3f-157">If you want to hide and disable a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) based on a conditional statement in the Condition field of the ControlCondition table, you should use four records for each control to disable as well as hide the control.</span></span> <span data-ttu-id="36a3f-158">È ancora possibile accedere ai controlli pulsante o CheckBox che sono rimasti nascosti solo tramite i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="36a3f-158">PushButton or CheckBox controls that have only been hidden can still be accessed by shortcut keys.</span></span>

<span data-ttu-id="36a3f-159">Ad esempio, i record seguenti nascondono e disabilitano controla nella finestra di dialogo quando il prodotto è installato.</span><span class="sxs-lookup"><span data-stu-id="36a3f-159">For example, the following records hide and disable ControlA on DialogA when the product is installed.</span></span> <span data-ttu-id="36a3f-160">Il controllo sarà visibile e attivato quando il prodotto non è installato.</span><span class="sxs-lookup"><span data-stu-id="36a3f-160">The control will be visible and enabled when the product is not installed.</span></span>



| <span data-ttu-id="36a3f-161">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="36a3f-161">Dialog</span></span>  | <span data-ttu-id="36a3f-162">Control</span><span class="sxs-lookup"><span data-stu-id="36a3f-162">Control</span></span>  | <span data-ttu-id="36a3f-163">Azione</span><span class="sxs-lookup"><span data-stu-id="36a3f-163">Action</span></span>  | <span data-ttu-id="36a3f-164">Condizione</span><span class="sxs-lookup"><span data-stu-id="36a3f-164">Condition</span></span>                      |
|---------|----------|---------|--------------------------------|
| <span data-ttu-id="36a3f-165">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="36a3f-165">DialogA</span></span> | <span data-ttu-id="36a3f-166">ControlA</span><span class="sxs-lookup"><span data-stu-id="36a3f-166">ControlA</span></span> | <span data-ttu-id="36a3f-167">Nascondi</span><span class="sxs-lookup"><span data-stu-id="36a3f-167">Hide</span></span>    | [<span data-ttu-id="36a3f-168">**Installato**</span><span class="sxs-lookup"><span data-stu-id="36a3f-168">**Installed**</span></span>](installed.md) |
| <span data-ttu-id="36a3f-169">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="36a3f-169">DialogA</span></span> | <span data-ttu-id="36a3f-170">ControlA</span><span class="sxs-lookup"><span data-stu-id="36a3f-170">ControlA</span></span> | <span data-ttu-id="36a3f-171">Disabilita</span><span class="sxs-lookup"><span data-stu-id="36a3f-171">Disable</span></span> | <span data-ttu-id="36a3f-172">Installato</span><span class="sxs-lookup"><span data-stu-id="36a3f-172">Installed</span></span>                      |
| <span data-ttu-id="36a3f-173">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="36a3f-173">DialogA</span></span> | <span data-ttu-id="36a3f-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="36a3f-174">ControlA</span></span> | <span data-ttu-id="36a3f-175">Mostra</span><span class="sxs-lookup"><span data-stu-id="36a3f-175">Show</span></span>    | <span data-ttu-id="36a3f-176">NON installato</span><span class="sxs-lookup"><span data-stu-id="36a3f-176">NOT Installed</span></span>                  |
| <span data-ttu-id="36a3f-177">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="36a3f-177">DialogA</span></span> | <span data-ttu-id="36a3f-178">ControlA</span><span class="sxs-lookup"><span data-stu-id="36a3f-178">ControlA</span></span> | <span data-ttu-id="36a3f-179">Abilitare</span><span class="sxs-lookup"><span data-stu-id="36a3f-179">Enable</span></span>  | <span data-ttu-id="36a3f-180">NON installato</span><span class="sxs-lookup"><span data-stu-id="36a3f-180">NOT Installed</span></span>                  |



 

## <a name="validation"></a><span data-ttu-id="36a3f-181">Convalida</span><span class="sxs-lookup"><span data-stu-id="36a3f-181">Validation</span></span>

<dl>

[<span data-ttu-id="36a3f-182">ICE03</span><span class="sxs-lookup"><span data-stu-id="36a3f-182">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="36a3f-183">ICE06</span><span class="sxs-lookup"><span data-stu-id="36a3f-183">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="36a3f-184">ICE17</span><span class="sxs-lookup"><span data-stu-id="36a3f-184">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="36a3f-185">ICE32</span><span class="sxs-lookup"><span data-stu-id="36a3f-185">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="36a3f-186">ICE46</span><span class="sxs-lookup"><span data-stu-id="36a3f-186">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="36a3f-187">ICE79</span><span class="sxs-lookup"><span data-stu-id="36a3f-187">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="36a3f-188">ICE86</span><span class="sxs-lookup"><span data-stu-id="36a3f-188">ICE86</span></span>](ice86.md)  
</dl>

 

 



