---
description: La tabella ControlEvent consente all'autore di specificare gli eventi del controllo avviati quando un utente interagisce con un controllo pulsante, un controllo CheckBox o un controllo SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Tabella ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885106"
---
# <a name="controlevent-table"></a><span data-ttu-id="ddb1a-103">Tabella ControlEvent</span><span class="sxs-lookup"><span data-stu-id="ddb1a-103">ControlEvent Table</span></span>

<span data-ttu-id="ddb1a-104">La tabella ControlEvent consente all'autore di specificare gli [eventi del controllo](control-events.md) avviati quando un utente interagisce con un [controllo pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-104">The ControlEvent table allows the author to specify the [Control Events](control-events.md) started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="ddb1a-105">Questi sono gli unici controlli che gli utenti possono usare per avviare gli eventi di controllo.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-105">These are the only controls users can use to initiate control events.</span></span> <span data-ttu-id="ddb1a-106">Ogni controllo può pubblicare più eventi di controllo.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-106">Each control can publish multiple control events.</span></span> <span data-ttu-id="ddb1a-107">Il programma di installazione avvia ogni evento nell'ordine specificato nella colonna ordering.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-107">The installer starts each event in the order specified in the Ordering column.</span></span> <span data-ttu-id="ddb1a-108">Un controllo pulsante di push, ad esempio, può pubblicare eventi per avviare una transizione a un'altra finestra di dialogo, uscire dalla sequenza della finestra di dialogo e avviare l'installazione del file.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-108">For example, a push button control can publish events to initiate a transition to another dialog box, exit the dialog box sequence, and begin file installation.</span></span>

<span data-ttu-id="ddb1a-109">L'eccezione da tenere presente è che ogni controllo può pubblicare un [NewDialog](newdialog-controlevent.md) o un evento [SpawnDialog](spawndialog-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb1a-109">The exception to note is that each control can publish a most one [NewDialog](newdialog-controlevent.md) or one [SpawnDialog](spawndialog-controlevent.md) event.</span></span> <span data-ttu-id="ddb1a-110">Se è necessario creare più eventi di controllo NewDialog e SpawnDialog in questa tabella, includere anche le istruzioni condizionali nei campi condizione che assicurano la pubblicazione al massimo un evento.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-110">If you need to author multiple NewDialog and SpawnDialog control events in this table, also include conditional statements in the Condition fields that ensure at most one event is published.</span></span> <span data-ttu-id="ddb1a-111">Se per lo stesso controllo sono selezionati più eventi di controllo NewDialog e SpawnDialog, solo l'evento con il valore più grande nella colonna ordering viene pubblicato quando il controllo è attivato.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-111">If multiple NewDialog and SpawnDialog control events are selected for the same control, only the event with the largest value in the Ordering column gets published when the control is activated.</span></span>

<span data-ttu-id="ddb1a-112">La tabella ControlEvent include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-112">The ControlEvent table has the following columns.</span></span>



| <span data-ttu-id="ddb1a-113">Colonna</span><span class="sxs-lookup"><span data-stu-id="ddb1a-113">Column</span></span>    | <span data-ttu-id="ddb1a-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddb1a-114">Type</span></span>                         | <span data-ttu-id="ddb1a-115">Chiave</span><span class="sxs-lookup"><span data-stu-id="ddb1a-115">Key</span></span> | <span data-ttu-id="ddb1a-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="ddb1a-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ddb1a-117">Finestra di dialogo\_</span><span class="sxs-lookup"><span data-stu-id="ddb1a-117">Dialog\_</span></span>  | [<span data-ttu-id="ddb1a-118">Identificatore</span><span class="sxs-lookup"><span data-stu-id="ddb1a-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="ddb1a-119">S</span><span class="sxs-lookup"><span data-stu-id="ddb1a-119">Y</span></span>   | <span data-ttu-id="ddb1a-120">N</span><span class="sxs-lookup"><span data-stu-id="ddb1a-120">N</span></span>        |
| <span data-ttu-id="ddb1a-121">controllo\_</span><span class="sxs-lookup"><span data-stu-id="ddb1a-121">Control\_</span></span> | [<span data-ttu-id="ddb1a-122">Identificatore</span><span class="sxs-lookup"><span data-stu-id="ddb1a-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="ddb1a-123">S</span><span class="sxs-lookup"><span data-stu-id="ddb1a-123">Y</span></span>   | <span data-ttu-id="ddb1a-124">N</span><span class="sxs-lookup"><span data-stu-id="ddb1a-124">N</span></span>        |
| <span data-ttu-id="ddb1a-125">Evento</span><span class="sxs-lookup"><span data-stu-id="ddb1a-125">Event</span></span>     | [<span data-ttu-id="ddb1a-126">Formattato</span><span class="sxs-lookup"><span data-stu-id="ddb1a-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ddb1a-127">S</span><span class="sxs-lookup"><span data-stu-id="ddb1a-127">Y</span></span>   | <span data-ttu-id="ddb1a-128">N</span><span class="sxs-lookup"><span data-stu-id="ddb1a-128">N</span></span>        |
| <span data-ttu-id="ddb1a-129">Argomento</span><span class="sxs-lookup"><span data-stu-id="ddb1a-129">Argument</span></span>  | [<span data-ttu-id="ddb1a-130">Formattato</span><span class="sxs-lookup"><span data-stu-id="ddb1a-130">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ddb1a-131">S</span><span class="sxs-lookup"><span data-stu-id="ddb1a-131">Y</span></span>   | <span data-ttu-id="ddb1a-132">N</span><span class="sxs-lookup"><span data-stu-id="ddb1a-132">N</span></span>        |
| <span data-ttu-id="ddb1a-133">Condizione</span><span class="sxs-lookup"><span data-stu-id="ddb1a-133">Condition</span></span> | [<span data-ttu-id="ddb1a-134">Condition</span><span class="sxs-lookup"><span data-stu-id="ddb1a-134">Condition</span></span>](condition.md)   | <span data-ttu-id="ddb1a-135">S</span><span class="sxs-lookup"><span data-stu-id="ddb1a-135">Y</span></span>   | <span data-ttu-id="ddb1a-136">S</span><span class="sxs-lookup"><span data-stu-id="ddb1a-136">Y</span></span>        |
| <span data-ttu-id="ddb1a-137">Ordering</span><span class="sxs-lookup"><span data-stu-id="ddb1a-137">Ordering</span></span>  | [<span data-ttu-id="ddb1a-138">Integer</span><span class="sxs-lookup"><span data-stu-id="ddb1a-138">Integer</span></span>](integer.md)       | <span data-ttu-id="ddb1a-139">N</span><span class="sxs-lookup"><span data-stu-id="ddb1a-139">N</span></span>   | <span data-ttu-id="ddb1a-140">S</span><span class="sxs-lookup"><span data-stu-id="ddb1a-140">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ddb1a-141">Colonne</span><span class="sxs-lookup"><span data-stu-id="ddb1a-141">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ddb1a-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_</span><span class="sxs-lookup"><span data-stu-id="ddb1a-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="ddb1a-143">Chiave esterna per la prima colonna della tabella della [finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-143">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="ddb1a-144">La combinazione di questo campo con il campo del controllo \_ identifica un controllo univoco.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-144">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="ddb1a-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_</span><span class="sxs-lookup"><span data-stu-id="ddb1a-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="ddb1a-146">Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-146">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="ddb1a-147">Combinando questo campo con il campo finestra di dialogo viene \_ identificato un controllo univoco.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-147">Combining this field with the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="ddb1a-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento</span><span class="sxs-lookup"><span data-stu-id="ddb1a-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="ddb1a-149">Identificatore che specifica il tipo di evento che deve essere eseguita quando l'utente interagisce con il controllo specificato dalla finestra di dialogo \_ e dal controllo \_ .</span><span class="sxs-lookup"><span data-stu-id="ddb1a-149">An identifier that specifies the type of event that should take place when the user interacts with the control specified by Dialog\_ and Control\_.</span></span> <span data-ttu-id="ddb1a-150">Per un elenco di valori possibili, vedere [Panoramica di ControlEvent](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-150">For a list of possible values see [ControlEvent Overview](controlevent-overview.md).</span></span>

<span data-ttu-id="ddb1a-151">Per impostare una proprietà con un controllo, inserire \[ il \_ nome \] della proprietà in questo campo e il nuovo valore nel campo argomento.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-151">To set a property with a control, put \[Property\_Name\] in this field and the new value in the argument field.</span></span> <span data-ttu-id="ddb1a-152">Inserire {} nel campo argument per immettere il valore null.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-152">Put { } into the argument field to enter the null value.</span></span>

</dd> <dt>

<span data-ttu-id="ddb1a-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argomento</span><span class="sxs-lookup"><span data-stu-id="ddb1a-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="ddb1a-154">Valore utilizzato come modificatore quando si attiva un particolare evento.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-154">A value used as a modifier when triggering a particular event.</span></span>

<span data-ttu-id="ddb1a-155">Ad esempio, l'argomento di [NewDialog ControlEvent](newdialog-controlevent.md) o [SpawnDialog ControlEvent](spawndialog-controlevent.md) è il nome della finestra di dialogo e l'argomento dell' [azione di installazione](install-action.md) è un numero che definisce il livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-155">For example, the argument of the [NewDialog ControlEvent](newdialog-controlevent.md) or the [SpawnDialog ControlEvent](spawndialog-controlevent.md) is the name of the dialog box and the argument of the [Install action](install-action.md) is a number defining the install level.</span></span>

</dd> <dt>

<span data-ttu-id="ddb1a-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="ddb1a-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="ddb1a-157">Istruzione condizionale che determina se il programma di installazione attiva l'evento nella colonna evento.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-157">A conditional statement that determines whether the installer activates the event in the Event column.</span></span> <span data-ttu-id="ddb1a-158">Il programma di installazione attiva l'evento se l'istruzione condizionale nel campo condizione restituisce true.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-158">The installer triggers the event if the conditional statement in the Condition field evaluates to True.</span></span> <span data-ttu-id="ddb1a-159">Inserire quindi un valore 1 in questa colonna per assicurarsi che l'evento venga attivato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-159">Therefore put a 1 in this column to ensure that the installer triggers the event.</span></span> <span data-ttu-id="ddb1a-160">Il programma di installazione non attiva l'evento se il campo condizione contiene un'istruzione che restituisce false.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-160">The installer does not trigger the event if the Condition field contains a statement that evaluates to False.</span></span> <span data-ttu-id="ddb1a-161">Il programma di installazione non attiva un evento con uno spazio vuoto nel campo condizione, a meno che nessun altro evento del controllo restituisca true.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-161">The installer does not trigger an event with a blank in the Condition field unless no other events of the control evaluate to True.</span></span> <span data-ttu-id="ddb1a-162">Se nessuno dei campi della condizione per il controllo denominato nel campo del controllo \_ restituisce true, il programma di installazione attiva l'evento con un campo di condizione vuoto e se più di un campo di condizione è vuoto, attiva l'unico evento con il valore più grande nel campo di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-162">If none of the Condition fields for the control named in the Control\_ field evaluate to True, the installer triggers the one event having a blank Condition field, and if more than one Condition field is blank it triggers the one event of these with the largest value in the Ordering field.</span></span> <span data-ttu-id="ddb1a-163">Vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-163">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb1a-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordinare</span><span class="sxs-lookup"><span data-stu-id="ddb1a-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="ddb1a-165">Integer usato per ordinare diversi eventi collegati allo stesso controllo.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-165">An integer used to order several events tied to the same control.</span></span> <span data-ttu-id="ddb1a-166">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-166">This must be a non-negative number.</span></span> <span data-ttu-id="ddb1a-167">Questo campo può essere lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-167">This field may be left blank.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddb1a-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddb1a-168">Remarks</span></span>

<span data-ttu-id="ddb1a-169">La [tabella EventMapping](eventmapping-table.md) elenca i controlli che sottoscrivono un evento di controllo ed elenca l'attributo del controllo da modificare quando l'evento viene pubblicato da un altro controllo o dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-169">The [EventMapping table](eventmapping-table.md) lists the controls that subscribe to some control event and lists the control attribute to be changed when that event is published by the another control or the installer.</span></span>

<span data-ttu-id="ddb1a-170">In Windows XP o nei sistemi operativi precedenti, gli utenti possono pubblicare un evento di controllo solo interagendo con un controllo [CheckBox](checkbox-control.md) o un [controllo pulsante](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-170">On Windows XP or earlier operating systems, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md) or [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="ddb1a-171">Con Windows Server 2003, gli utenti possono pubblicare un evento di controllo solo interagendo con un controllo [CheckBox](checkbox-control.md), un [controllo SelectionTree](selectiontree-control.md)e un [controllo pulsante](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-171">With Windows Server 2003, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md), [SelectionTree Control](selectiontree-control.md), and [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="ddb1a-172">L'elenco di altri controlli nel \_ campo del controllo non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-172">Listing other controls in the Control\_ field has no effect.</span></span>

## <a name="validation"></a><span data-ttu-id="ddb1a-173">Convalida</span><span class="sxs-lookup"><span data-stu-id="ddb1a-173">Validation</span></span>

<dl>

[<span data-ttu-id="ddb1a-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="ddb1a-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ddb1a-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="ddb1a-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ddb1a-176">ICE17</span><span class="sxs-lookup"><span data-stu-id="ddb1a-176">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="ddb1a-177">ICE20</span><span class="sxs-lookup"><span data-stu-id="ddb1a-177">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="ddb1a-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="ddb1a-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ddb1a-179">ICE44</span><span class="sxs-lookup"><span data-stu-id="ddb1a-179">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="ddb1a-180">ICE46</span><span class="sxs-lookup"><span data-stu-id="ddb1a-180">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ddb1a-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="ddb1a-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="ddb1a-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="ddb1a-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



