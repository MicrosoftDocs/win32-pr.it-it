---
description: ControlEvents sono analoghi ai messaggi di Microsoft Windows nelle applicazioni basate su Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Panoramica di ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885109"
---
# <a name="controlevent-overview"></a><span data-ttu-id="1994d-103">Panoramica di ControlEvent</span><span class="sxs-lookup"><span data-stu-id="1994d-103">ControlEvent Overview</span></span>

<span data-ttu-id="1994d-104">ControlEvents sono analoghi ai messaggi di Microsoft Windows nelle applicazioni basate su Win32.</span><span class="sxs-lookup"><span data-stu-id="1994d-104">ControlEvents are analogous to Microsoft Windows messages in Win32-based applications.</span></span> <span data-ttu-id="1994d-105">Tuttavia, invece di creare una funzione di callback per ricevere i messaggi di Windows e inviare messaggi di Windows con la funzione [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , il programma di installazione dell'interfaccia utente e i controlli pubblicano [ControlEvents](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-105">However, rather than creating a callback function to receive Windows messages and sending Windows messages with the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function, the user interface (UI) installer and controls publish [ControlEvents](control-events.md).</span></span> <span data-ttu-id="1994d-106">È possibile specificare altri controlli e il programma di installazione per sottoscrivere ControlEvents specifici che modificheranno gli attributi del controllo Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="1994d-106">Other controls and the installer can be specified to subscribe to particular ControlEvents that will then change attributes of the subscribing control.</span></span> <span data-ttu-id="1994d-107">Per aggiungere controlli di lavoro alle finestre di dialogo, l'autore dell'interfaccia utente specifica la pubblicazione di ControlEvents nella [tabella ControlEvent](controlevent-table.md) e sottoscrive i controlli a ControlEvents nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-107">To add working controls to dialog boxes, the author of the UI specifies the publication of ControlEvents in the [ControlEvent table](controlevent-table.md) and subscribes controls to ControlEvents in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="1994d-108">Il programma di installazione pubblicherà gli eventi seguenti nei controlli di sottoscrizione elencati nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-108">The installer will publish the following events to subscribing controls listed in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="1994d-109">Un controllo [ProgressBar](progressbar-control.md) o un [controllo Billboard](billboard-control.md) in genere sottoscrive lo stato di avanzamento, il resto viene sottoscritto dai [controlli testo](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-109">A [ProgressBar control](progressbar-control.md) or [Billboard control](billboard-control.md) typically subscribes to SetProgress, the rest are subscribed to by [Text controls](text-control.md).</span></span>

[<span data-ttu-id="1994d-110">ControlEvent ActionData</span><span class="sxs-lookup"><span data-stu-id="1994d-110">ActionData ControlEvent</span></span>](actiondata-controlevent.md)

[<span data-ttu-id="1994d-111">ControlEvent ActionText</span><span class="sxs-lookup"><span data-stu-id="1994d-111">ActionText ControlEvent</span></span>](actiontext-controlevent.md)

[<span data-ttu-id="1994d-112">ControlEvent di avanzamento</span><span class="sxs-lookup"><span data-stu-id="1994d-112">SetProgress ControlEvent</span></span>](setprogress-controlevent.md)

[<span data-ttu-id="1994d-113">ControlEvent TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="1994d-113">TimeRemaining ControlEvent</span></span>](timeremaining-controlevent.md)

[<span data-ttu-id="1994d-114">ControlEvent ScriptInProgress</span><span class="sxs-lookup"><span data-stu-id="1994d-114">ScriptInProgress ControlEvent</span></span>](scriptinprogress-controlevent.md)

<span data-ttu-id="1994d-115">Gli eventi seguenti vengono pubblicati dal controllo quando la selezione dell'elemento viene spostata in un [controllo SelectionTree](selectiontree-control.md) o nell' [elenco di directory](directorylist-control.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-115">The following events are published by the control when the item selection is moved in a [SelectionTree control](selectiontree-control.md) or [DirectoryList Control](directorylist-control.md).</span></span> <span data-ttu-id="1994d-116">I controlli di sottoscrizione devono essere posizionati nella stessa finestra di dialogo ed elencati nella tabella EventMapping.</span><span class="sxs-lookup"><span data-stu-id="1994d-116">Subscribing controls must be located on the same dialog box and listed in the EventMapping table.</span></span>

[<span data-ttu-id="1994d-117">ControlEvent IgnoreChange</span><span class="sxs-lookup"><span data-stu-id="1994d-117">IgnoreChange ControlEvent</span></span>](ignorechange-controlevent.md)

[<span data-ttu-id="1994d-118">ControlEvent SelectionDescription</span><span class="sxs-lookup"><span data-stu-id="1994d-118">SelectionDescription ControlEvent</span></span>](selectiondescription-controlevent.md)

[<span data-ttu-id="1994d-119">ControlEvent SelectionSize</span><span class="sxs-lookup"><span data-stu-id="1994d-119">SelectionSize ControlEvent</span></span>](selectionsize-controlevent.md)

[<span data-ttu-id="1994d-120">ControlEvent SelectionPath</span><span class="sxs-lookup"><span data-stu-id="1994d-120">SelectionPath ControlEvent</span></span>](selectionpath-controlevent.md)

[<span data-ttu-id="1994d-121">ControlEvent SelectionAction</span><span class="sxs-lookup"><span data-stu-id="1994d-121">SelectionAction ControlEvent</span></span>](selectionaction-controlevent.md)

[<span data-ttu-id="1994d-122">ControlEvent SelectionNoItems</span><span class="sxs-lookup"><span data-stu-id="1994d-122">SelectionNoItems ControlEvent</span></span>](selectionnoitems-controlevent.md)

<span data-ttu-id="1994d-123">I ControlEvents seguenti possono essere pubblicati a discrezione di un utente interagendo con un [controllo pulsante](pushbutton-control.md) o un [controllo CheckBox](checkbox-control.md) in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1994d-123">The following ControlEvents can be published at the discretion of a user by interacting with a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) on a dialog box.</span></span> <span data-ttu-id="1994d-124">Il controllo CheckBox può pubblicare solo gli eventi AddLocal, AddSource, Remove, DoAction e SetProperty.</span><span class="sxs-lookup"><span data-stu-id="1994d-124">The Checkbox control can only publish the AddLocal, AddSource, Remove, DoAction, and SetProperty events.</span></span> <span data-ttu-id="1994d-125">Con Windows Installer versioni fornite con Windows Server 2003 e versioni successive, il [controllo SelectionTree](selectiontree-control.md) può pubblicare DoAction, ControlEvent e SetProperty ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="1994d-125">With Windows Installer versions that shipped with Windows Server 2003 and later, the [SelectionTree control](selectiontree-control.md) can publish the DoAction, ControlEvent and SetProperty ControlEvents.</span></span> <span data-ttu-id="1994d-126">L'autore dell'interfaccia utente dovrebbe elencare ControlEvent nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-126">The author of the UI should list the ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="1994d-127">Il gestore dell'interfaccia utente del programma di installazione è il Sottoscrittore di questi eventi.</span><span class="sxs-lookup"><span data-stu-id="1994d-127">The UI handler of the installer is the subscriber to these events.</span></span>

[<span data-ttu-id="1994d-128">ControlEvent AddLocal</span><span class="sxs-lookup"><span data-stu-id="1994d-128">AddLocal ControlEvent</span></span>](addlocal-controlevent.md)

[<span data-ttu-id="1994d-129">ControlEvent AddSource</span><span class="sxs-lookup"><span data-stu-id="1994d-129">AddSource ControlEvent</span></span>](addsource-controlevent.md)

[<span data-ttu-id="1994d-130">ControlEvent CheckExistingTargetPath</span><span class="sxs-lookup"><span data-stu-id="1994d-130">CheckExistingTargetPath ControlEvent</span></span>](checkexistingtargetpath-controlevent.md)

[<span data-ttu-id="1994d-131">ControlEvent CheckTargetPath</span><span class="sxs-lookup"><span data-stu-id="1994d-131">CheckTargetPath ControlEvent</span></span>](checktargetpath-controlevent.md)

[<span data-ttu-id="1994d-132">ControlEvent DoAction</span><span class="sxs-lookup"><span data-stu-id="1994d-132">DoAction ControlEvent</span></span>](doaction-controlevent.md)

[<span data-ttu-id="1994d-133">ControlEvent EnableRollback</span><span class="sxs-lookup"><span data-stu-id="1994d-133">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

[<span data-ttu-id="1994d-134">ControlEvent EndDialog</span><span class="sxs-lookup"><span data-stu-id="1994d-134">EndDialog ControlEvent</span></span>](enddialog-controlevent.md)

[<span data-ttu-id="1994d-135">ControlEvent NewDialog</span><span class="sxs-lookup"><span data-stu-id="1994d-135">NewDialog ControlEvent</span></span>](newdialog-controlevent.md)

[<span data-ttu-id="1994d-136">Reinstallare ControlEvent</span><span class="sxs-lookup"><span data-stu-id="1994d-136">Reinstall ControlEvent</span></span>](reinstall-controlevent.md)

[<span data-ttu-id="1994d-137">ControlEvent ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="1994d-137">ReinstallMode ControlEvent</span></span>](reinstallmode-controlevent.md)

[<span data-ttu-id="1994d-138">Rimuovere ControlEvent</span><span class="sxs-lookup"><span data-stu-id="1994d-138">Remove ControlEvent</span></span>](remove-controlevent.md)

[<span data-ttu-id="1994d-139">Reimposta ControlEvent</span><span class="sxs-lookup"><span data-stu-id="1994d-139">Reset ControlEvent</span></span>](reset-controlevent.md)

[<span data-ttu-id="1994d-140">ControlEvent SetInstallLevel</span><span class="sxs-lookup"><span data-stu-id="1994d-140">SetInstallLevel ControlEvent</span></span>](setinstalllevel-controlevent.md)

[<span data-ttu-id="1994d-141">Proprietà ControlEvent</span><span class="sxs-lookup"><span data-stu-id="1994d-141">SetProperty ControlEvent</span></span>](setproperty-controlevent.md)

[<span data-ttu-id="1994d-142">ControlEvent SetTargetPath</span><span class="sxs-lookup"><span data-stu-id="1994d-142">SetTargetPath ControlEvent</span></span>](settargetpath-controlevent.md)

[<span data-ttu-id="1994d-143">ControlEvent SpawnDialog</span><span class="sxs-lookup"><span data-stu-id="1994d-143">SpawnDialog ControlEvent</span></span>](spawndialog-controlevent.md)

[<span data-ttu-id="1994d-144">ControlEvent SpawnWaitDialog</span><span class="sxs-lookup"><span data-stu-id="1994d-144">SpawnWaitDialog ControlEvent</span></span>](spawnwaitdialog-controlevent.md)

[<span data-ttu-id="1994d-145">ControlEvent ValidateProductID</span><span class="sxs-lookup"><span data-stu-id="1994d-145">ValidateProductID ControlEvent</span></span>](validateproductid-controlevent.md)

<span data-ttu-id="1994d-146">Un [controllo pulsante](pushbutton-control.md) può pubblicare gli eventi seguenti in un controllo [SelectionTree](selectiontree-control.md) o in un controllo [directory](directorylist-control.md) di sottoscrizione che si trova nella stessa finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1994d-146">A [PushButton control](pushbutton-control.md) can publish the following events to a subscribing [SelectionTree control](selectiontree-control.md) or [DirectoryList control](directorylist-control.md) located in the same dialog box.</span></span> <span data-ttu-id="1994d-147">Il controllo pulsante deve essere elencato nella tabella ControlEvent e i controlli di sottoscrizione devono essere elencati nella tabella EventMapping.</span><span class="sxs-lookup"><span data-stu-id="1994d-147">The PushButton Control should be listed in the ControlEvent table and the subscribing controls should be listed in the EventMapping table.</span></span>

[<span data-ttu-id="1994d-148">ControlEvent SelectionBrowse</span><span class="sxs-lookup"><span data-stu-id="1994d-148">SelectionBrowse ControlEvent</span></span>](selectionbrowse-controlevent.md)

[<span data-ttu-id="1994d-149">ControlEvent DirectoryListUp</span><span class="sxs-lookup"><span data-stu-id="1994d-149">DirectoryListUp ControlEvent</span></span>](directorylistup-controlevent.md)

[<span data-ttu-id="1994d-150">ControlEvent DirectoryListNew</span><span class="sxs-lookup"><span data-stu-id="1994d-150">DirectoryListNew ControlEvent</span></span>](directorylistnew-controlevent.md)

[<span data-ttu-id="1994d-151">ControlEvent DirectoryListOpen</span><span class="sxs-lookup"><span data-stu-id="1994d-151">DirectoryListOpen ControlEvent</span></span>](directorylistopen-controlevent.md)

<span data-ttu-id="1994d-152">Gli eventi di controllo richiedono in genere che l'interfaccia utente venga eseguita a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1994d-152">Control events generally require that the UI be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="1994d-153">La maggior parte delle ControlEvents non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md) perché questi livelli visualizzano solo finestre di dialogo non modali.</span><span class="sxs-lookup"><span data-stu-id="1994d-153">Most ControlEvents will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md) because these levels only display modeless dialog boxes.</span></span> <span data-ttu-id="1994d-154">Gli eventi ActionText, AddSource, seprogress, TimeRemaining e ScriptInProgress sono eccezioni e funzioneranno in un'interfaccia utente ridotta o di base.</span><span class="sxs-lookup"><span data-stu-id="1994d-154">The ActionText, AddSource, SetProgress, TimeRemaining, and ScriptInProgress events are exceptions and will work in reduced or basic UI.</span></span> <span data-ttu-id="1994d-155">Per ulteriori informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-155">For more information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="1994d-156">È possibile eseguire [azioni personalizzate](custom-actions.md) pubblicando un ControlEvent da un [controllo pulsante](pushbutton-control.md) o una [casella di controllo](checkbox-control.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-156">You can run [custom actions](custom-actions.md) by publishing a ControlEvent from a [PushButton control](pushbutton-control.md) or [Checkbox control](checkbox-control.md).</span></span> <span data-ttu-id="1994d-157">Aggiungere un record alla [tabella ControlEvent](controlevent-table.md) con i nomi della finestra di dialogo e il controllo per la pubblicazione di ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="1994d-157">Add a record to the [ControlEvent table](controlevent-table.md) with the names of the dialog and the control publishing the ControlEvent.</span></span> <span data-ttu-id="1994d-158">Questo controllo deve pubblicare un [ControlEvent DoAction](doaction-controlevent.md) che invia una notifica al programma di installazione per eseguire l'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="1994d-158">This control should publish a [DoAction ControlEvent](doaction-controlevent.md) notifying the installer to run the custom action.</span></span> <span data-ttu-id="1994d-159">Nei sistemi Windows XP o versioni precedenti non è possibile eseguire un'azione personalizzata pubblicando un ControlEvent da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-159">On Windows XP or earlier systems, you cannot run a custom action by publishing a ControlEvent from a [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="1994d-160">Per ulteriori informazioni su ControlEvents particolari, vedere l'elenco di [ControlEvents](control-events.md) standard in informazioni di [riferimento sull'interfaccia utente](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1994d-160">For a more information about particular ControlEvents, see the list of standard [ControlEvents](control-events.md) in [User Interface Reference](user-interface-reference.md).</span></span>

 

 
