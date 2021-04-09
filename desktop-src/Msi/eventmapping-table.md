---
description: La tabella EventMapping elenca i controlli che sottoscrivono alcuni eventi di controllo ed elenca l'attributo da modificare quando l'evento viene pubblicato da un altro controllo o dal Windows Installer.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Tabella EventMapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880882"
---
# <a name="eventmapping-table"></a><span data-ttu-id="5ae51-103">Tabella EventMapping</span><span class="sxs-lookup"><span data-stu-id="5ae51-103">EventMapping Table</span></span>

<span data-ttu-id="5ae51-104">La tabella EventMapping elenca i controlli che sottoscrivono alcuni eventi di controllo ed elenca l'attributo da modificare quando l'evento viene pubblicato da un altro controllo o dal Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5ae51-104">The EventMapping Table lists the controls that subscribe to some control events, and lists the attribute to be changed when the event is published by another control or the Windows Installer.</span></span>

<span data-ttu-id="5ae51-105">La tabella EventMapping include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ae51-105">The EventMapping Table has the following columns.</span></span>



| <span data-ttu-id="5ae51-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="5ae51-106">Column</span></span>    | <span data-ttu-id="5ae51-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ae51-107">Type</span></span>                         | <span data-ttu-id="5ae51-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="5ae51-108">Key</span></span> | <span data-ttu-id="5ae51-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="5ae51-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="5ae51-110">Finestra di dialogo\_</span><span class="sxs-lookup"><span data-stu-id="5ae51-110">Dialog\_</span></span>  | [<span data-ttu-id="5ae51-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5ae51-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ae51-112">S</span><span class="sxs-lookup"><span data-stu-id="5ae51-112">Y</span></span>   | <span data-ttu-id="5ae51-113">N</span><span class="sxs-lookup"><span data-stu-id="5ae51-113">N</span></span>        |
| <span data-ttu-id="5ae51-114">controllo\_</span><span class="sxs-lookup"><span data-stu-id="5ae51-114">Control\_</span></span> | [<span data-ttu-id="5ae51-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5ae51-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ae51-116">S</span><span class="sxs-lookup"><span data-stu-id="5ae51-116">Y</span></span>   | <span data-ttu-id="5ae51-117">N</span><span class="sxs-lookup"><span data-stu-id="5ae51-117">N</span></span>        |
| <span data-ttu-id="5ae51-118">Evento</span><span class="sxs-lookup"><span data-stu-id="5ae51-118">Event</span></span>     | [<span data-ttu-id="5ae51-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5ae51-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ae51-120">S</span><span class="sxs-lookup"><span data-stu-id="5ae51-120">Y</span></span>   | <span data-ttu-id="5ae51-121">N</span><span class="sxs-lookup"><span data-stu-id="5ae51-121">N</span></span>        |
| <span data-ttu-id="5ae51-122">Attributo</span><span class="sxs-lookup"><span data-stu-id="5ae51-122">Attribute</span></span> | [<span data-ttu-id="5ae51-123">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5ae51-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ae51-124">N</span><span class="sxs-lookup"><span data-stu-id="5ae51-124">N</span></span>   | <span data-ttu-id="5ae51-125">N</span><span class="sxs-lookup"><span data-stu-id="5ae51-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5ae51-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="5ae51-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5ae51-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_</span><span class="sxs-lookup"><span data-stu-id="5ae51-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="5ae51-128">Chiave esterna per la prima colonna della tabella della [finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-128">An external key to the first column of the [Dialog Table](dialog-table.md).</span></span> <span data-ttu-id="5ae51-129">Questo campo e il campo di controllo \_ identificano un controllo.</span><span class="sxs-lookup"><span data-stu-id="5ae51-129">This field and the Control\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="5ae51-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_</span><span class="sxs-lookup"><span data-stu-id="5ae51-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="5ae51-131">Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-131">An external key to the second column of the [Control Table](control-table.md).</span></span> <span data-ttu-id="5ae51-132">Questo campo e il campo della finestra di dialogo \_ identificano un controllo.</span><span class="sxs-lookup"><span data-stu-id="5ae51-132">This field and the Dialog\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="5ae51-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento</span><span class="sxs-lookup"><span data-stu-id="5ae51-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="5ae51-134">Questo campo è un identificatore che specifica il tipo di evento sottoscritto dal controllo.</span><span class="sxs-lookup"><span data-stu-id="5ae51-134">This field is an identifier that specifies the type of event that is subscribed to by the control.</span></span> <span data-ttu-id="5ae51-135">Per altre informazioni, vedere [Panoramica di ControlEvent](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-135">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ae51-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo</span><span class="sxs-lookup"><span data-stu-id="5ae51-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="5ae51-137">Nome dell'attributo del controllo \_ impostato quando viene ricevuto l'evento nella colonna dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5ae51-137">The name of the Control\_ attribute that is set when the event in the Event column is received.</span></span> <span data-ttu-id="5ae51-138">L'argomento dell'evento viene passato come argomento della chiamata di attributo per modificare questo attributo del controllo.</span><span class="sxs-lookup"><span data-stu-id="5ae51-138">The Argument of the event is passed as the argument of the attribute call to change this attribute of the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ae51-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ae51-139">Remarks</span></span>

<span data-ttu-id="5ae51-140">La [tabella ControlEvent](controlevent-table.md) specifica gli eventi di controllo che vengono avviati quando un utente interagisce con un [controllo pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-140">The [ControlEvent Table](controlevent-table.md) specifies the control events that are started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="5ae51-141">Questi sono gli unici controlli che un utente può usare per avviare gli eventi di controllo.</span><span class="sxs-lookup"><span data-stu-id="5ae51-141">These are the only controls that a user can use to initiate control events.</span></span>

<span data-ttu-id="5ae51-142">Più di un controllo in una finestra di dialogo può sottoscrivere lo stesso evento.</span><span class="sxs-lookup"><span data-stu-id="5ae51-142">More than one control on a dialog box can subscribe to the same event.</span></span>

<span data-ttu-id="5ae51-143">Nell'elenco seguente vengono identificati gli utilizzi tipici della tabella EventMapping:</span><span class="sxs-lookup"><span data-stu-id="5ae51-143">The following list identifies the typical uses for the EventMapping Table:</span></span>

-   <span data-ttu-id="5ae51-144">Per sottoscrivere [un controllo di testo](text-control.md) a un [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) o [TimeRemaining](timeremaining-controlevent.md) ControlEvent pubblicato dal Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5ae51-144">To subscribe a [Text Control](text-control.md) to an [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) or [TimeRemaining ControlEvent](timeremaining-controlevent.md) published by the Windows Installer.</span></span>
-   <span data-ttu-id="5ae51-145">Per sottoscrivere un controllo [ProgressBar](progressbar-control.md) o un [controllo Billboard](billboard-control.md) a un [ControlEvent di avanzamento](setprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-145">To subscribe a [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) to a [SetProgress ControlEvent](setprogress-controlevent.md).</span></span>
-   <span data-ttu-id="5ae51-146">Per sottoscrivere un [controllo DirectoryCombo](directorycombo-control.md) a un [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-146">To subscribe a [DirectoryCombo Control](directorycombo-control.md) to an [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span></span>
-   <span data-ttu-id="5ae51-147">Per disabilitare automaticamente un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo con un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-147">To automatically disable a [PushButton Control](pushbutton-control.md) located on the same dialog with a [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="5ae51-148">Per disabilitare il pulsante push quando nessuna funzionalità è elencata nel [controllo SelectionTree](selectiontree-control.md), usare la tabella EventMapping per sottoscrivere il controllo pulsante a un [ControlEvent SelectionNoItems](selectionnoitems-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-148">To disable the push button when no features are listed in the [SelectionTree Control](selectiontree-control.md), use the EventMapping Table to subscribe the PushButton control to a [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md).</span></span> <span data-ttu-id="5ae51-149">Immettere **Enable** nel campo Attributes della tabella EventMapping.</span><span class="sxs-lookup"><span data-stu-id="5ae51-149">Enter **Enable** in the Attributes field of the EventMapping Table.</span></span>
-   <span data-ttu-id="5ae51-150">Per visualizzare un [controllo di testo](text-control.md) che mostra il percorso di installazione per la funzionalità selezionata in un [controllo SelectionTree](selectiontree-control.md) nella stessa finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5ae51-150">To display a [Text Control](text-control.md) that shows the path to the installation location for the feature that is selected in a [SelectionTree Control](selectiontree-control.md) on the same dialog.</span></span> <span data-ttu-id="5ae51-151">Usare la tabella EventMapping per sottoscrivere [il controllo di testo](text-control.md) in [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) e [SelectionPath ControlEvent](selectionpath-controlevent.md) pubblicati dal [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="5ae51-151">Use the EventMapping Table to subscribe the [Text Control](text-control.md) to both a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) and [SelectionPath ControlEvent](selectionpath-controlevent.md) published by the [SelectionTree Control](selectiontree-control.md).</span></span>
-   <span data-ttu-id="5ae51-152">Per visualizzare un [controllo testo](text-control.md) che mostra una descrizione dell'elemento evidenziato in un [controllo SelectionTree](selectiontree-control.md) che si trova nella stessa finestra di dialogo, usare la tabella EventMapping per sottoscrivere il [controllo di testo](text-control.md) a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) o [SelectionAction](selectionaction-controlevent.md)ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="5ae51-152">To display a [Text Control](text-control.md) that shows a description of the item highlighted in a [SelectionTree Control](selectiontree-control.md) located on the same dialog, use the EventMapping Table to subscribe the [Text Control](text-control.md) to a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) or [SelectionAction ControlEvent](selectionaction-controlevent.md).</span></span> <span data-ttu-id="5ae51-153">Immettere il **testo** nel campo attributo della tabella EventMapping.</span><span class="sxs-lookup"><span data-stu-id="5ae51-153">Enter **Text** in the Attribute field of the EventMapping Table.</span></span>

## <a name="validation"></a><span data-ttu-id="5ae51-154">Convalida</span><span class="sxs-lookup"><span data-stu-id="5ae51-154">Validation</span></span>

<dl>

[<span data-ttu-id="5ae51-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="5ae51-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5ae51-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="5ae51-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5ae51-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="5ae51-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



