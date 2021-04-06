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
# <a name="controlevent-overview"></a>Panoramica di ControlEvent

ControlEvents sono analoghi ai messaggi di Microsoft Windows nelle applicazioni basate su Win32. Tuttavia, invece di creare una funzione di callback per ricevere i messaggi di Windows e inviare messaggi di Windows con la funzione [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , il programma di installazione dell'interfaccia utente e i controlli pubblicano [ControlEvents](control-events.md). È possibile specificare altri controlli e il programma di installazione per sottoscrivere ControlEvents specifici che modificheranno gli attributi del controllo Sottoscrittore. Per aggiungere controlli di lavoro alle finestre di dialogo, l'autore dell'interfaccia utente specifica la pubblicazione di ControlEvents nella [tabella ControlEvent](controlevent-table.md) e sottoscrive i controlli a ControlEvents nella [tabella EventMapping](eventmapping-table.md).

Il programma di installazione pubblicherà gli eventi seguenti nei controlli di sottoscrizione elencati nella [tabella EventMapping](eventmapping-table.md). Un controllo [ProgressBar](progressbar-control.md) o un [controllo Billboard](billboard-control.md) in genere sottoscrive lo stato di avanzamento, il resto viene sottoscritto dai [controlli testo](text-control.md).

[ControlEvent ActionData](actiondata-controlevent.md)

[ControlEvent ActionText](actiontext-controlevent.md)

[ControlEvent di avanzamento](setprogress-controlevent.md)

[ControlEvent TimeRemaining](timeremaining-controlevent.md)

[ControlEvent ScriptInProgress](scriptinprogress-controlevent.md)

Gli eventi seguenti vengono pubblicati dal controllo quando la selezione dell'elemento viene spostata in un [controllo SelectionTree](selectiontree-control.md) o nell' [elenco di directory](directorylist-control.md). I controlli di sottoscrizione devono essere posizionati nella stessa finestra di dialogo ed elencati nella tabella EventMapping.

[ControlEvent IgnoreChange](ignorechange-controlevent.md)

[ControlEvent SelectionDescription](selectiondescription-controlevent.md)

[ControlEvent SelectionSize](selectionsize-controlevent.md)

[ControlEvent SelectionPath](selectionpath-controlevent.md)

[ControlEvent SelectionAction](selectionaction-controlevent.md)

[ControlEvent SelectionNoItems](selectionnoitems-controlevent.md)

I ControlEvents seguenti possono essere pubblicati a discrezione di un utente interagendo con un [controllo pulsante](pushbutton-control.md) o un [controllo CheckBox](checkbox-control.md) in una finestra di dialogo. Il controllo CheckBox può pubblicare solo gli eventi AddLocal, AddSource, Remove, DoAction e SetProperty. Con Windows Installer versioni fornite con Windows Server 2003 e versioni successive, il [controllo SelectionTree](selectiontree-control.md) può pubblicare DoAction, ControlEvent e SetProperty ControlEvents. L'autore dell'interfaccia utente dovrebbe elencare ControlEvent nella [tabella ControlEvent](controlevent-table.md). Il gestore dell'interfaccia utente del programma di installazione è il Sottoscrittore di questi eventi.

[ControlEvent AddLocal](addlocal-controlevent.md)

[ControlEvent AddSource](addsource-controlevent.md)

[ControlEvent CheckExistingTargetPath](checkexistingtargetpath-controlevent.md)

[ControlEvent CheckTargetPath](checktargetpath-controlevent.md)

[ControlEvent DoAction](doaction-controlevent.md)

[ControlEvent EnableRollback](enablerollback-controlevent.md)

[ControlEvent EndDialog](enddialog-controlevent.md)

[ControlEvent NewDialog](newdialog-controlevent.md)

[Reinstallare ControlEvent](reinstall-controlevent.md)

[ControlEvent ReinstallMode](reinstallmode-controlevent.md)

[Rimuovere ControlEvent](remove-controlevent.md)

[Reimposta ControlEvent](reset-controlevent.md)

[ControlEvent SetInstallLevel](setinstalllevel-controlevent.md)

[Proprietà ControlEvent](setproperty-controlevent.md)

[ControlEvent SetTargetPath](settargetpath-controlevent.md)

[ControlEvent SpawnDialog](spawndialog-controlevent.md)

[ControlEvent SpawnWaitDialog](spawnwaitdialog-controlevent.md)

[ControlEvent ValidateProductID](validateproductid-controlevent.md)

Un [controllo pulsante](pushbutton-control.md) può pubblicare gli eventi seguenti in un controllo [SelectionTree](selectiontree-control.md) o in un controllo [directory](directorylist-control.md) di sottoscrizione che si trova nella stessa finestra di dialogo. Il controllo pulsante deve essere elencato nella tabella ControlEvent e i controlli di sottoscrizione devono essere elencati nella tabella EventMapping.

[ControlEvent SelectionBrowse](selectionbrowse-controlevent.md)

[ControlEvent DirectoryListUp](directorylistup-controlevent.md)

[ControlEvent DirectoryListNew](directorylistnew-controlevent.md)

[ControlEvent DirectoryListOpen](directorylistopen-controlevent.md)

Gli eventi di controllo richiedono in genere che l'interfaccia utente venga eseguita a livello di [*interfaccia utente completo*](f-gly.md) . La maggior parte delle ControlEvents non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md) perché questi livelli visualizzano solo finestre di dialogo non modali. Gli eventi ActionText, AddSource, seprogress, TimeRemaining e ScriptInProgress sono eccezioni e funzioneranno in un'interfaccia utente ridotta o di base. Per ulteriori informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).

È possibile eseguire [azioni personalizzate](custom-actions.md) pubblicando un ControlEvent da un [controllo pulsante](pushbutton-control.md) o una [casella di controllo](checkbox-control.md). Aggiungere un record alla [tabella ControlEvent](controlevent-table.md) con i nomi della finestra di dialogo e il controllo per la pubblicazione di ControlEvent. Questo controllo deve pubblicare un [ControlEvent DoAction](doaction-controlevent.md) che invia una notifica al programma di installazione per eseguire l'azione personalizzata. Nei sistemi Windows XP o versioni precedenti non è possibile eseguire un'azione personalizzata pubblicando un ControlEvent da un [controllo SelectionTree](selectiontree-control.md).

Per ulteriori informazioni su ControlEvents particolari, vedere l'elenco di [ControlEvents](control-events.md) standard in informazioni di [riferimento sull'interfaccia utente](user-interface-reference.md).

 

 
