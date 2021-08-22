---
description: ControlEvents è analogo ai messaggi Windows Microsoft nelle applicazioni basate su Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Cenni preliminari su ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2736c93a728e2419f2ac9c722be2149e6e3ac681c95428f3383570262eb583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045141"
---
# <a name="controlevent-overview"></a>Cenni preliminari su ControlEvent

ControlEvents è analogo ai messaggi Windows Microsoft nelle applicazioni basate su Win32. Tuttavia, anziché creare una funzione di callback per ricevere Windows messaggi e inviare Windows messaggi con la funzione [SendMessage,](/windows/win32/api/winuser/nf-winuser-sendmessage) il programma di installazione dell'interfaccia utente e i controlli pubblicano [ControlEvents](control-events.md). È possibile specificare altri controlli e il programma di installazione per sottoscrivere specifici ControlEvent che modificheranno quindi gli attributi del controllo di sottoscrizione. Per aggiungere controlli di lavoro alle finestre di dialogo, l'autore dell'interfaccia utente specifica la pubblicazione di ControlEvents nella tabella [ControlEvent](controlevent-table.md) e sottoscrive i controlli a ControlEvents nella [tabella EventMapping](eventmapping-table.md).

Il programma di installazione pubblicherà gli eventi seguenti nei controlli di sottoscrizione elencati nella [tabella EventMapping](eventmapping-table.md). Un [controllo ProgressBar o](progressbar-control.md) un controllo [Barra](billboard-control.md) di avanzamento in genere sottoscrive SetProgress, il resto viene sottoscritto dai controlli [Text](text-control.md).

[ActionData ControlEvent](actiondata-controlevent.md)

[ActionText ControlEvent](actiontext-controlevent.md)

[SetProgress ControlEvent](setprogress-controlevent.md)

[TimeRemaining ControlEvent](timeremaining-controlevent.md)

[ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)

Gli eventi seguenti vengono pubblicati dal controllo quando la selezione dell'elemento viene spostata in un [controllo SelectionTree](selectiontree-control.md) o [in un controllo DirectoryList](directorylist-control.md). I controlli di sottoscrizione devono trovarsi nella stessa finestra di dialogo ed elencati nella tabella EventMapping.

[IgnoreChange ControlEvent](ignorechange-controlevent.md)

[Controllo SelectionDescriptionEvent](selectiondescription-controlevent.md)

[SelectionSize ControlEvent](selectionsize-controlevent.md)

[SelectionPath ControlEvent](selectionpath-controlevent.md)

[SelectionAction ControlEvent](selectionaction-controlevent.md)

[SelectionNoItems ControlEvent](selectionnoitems-controlevent.md)

Gli eventi ControlEvent seguenti possono essere pubblicati a discrezione di un utente interagendo con un controllo [PushButton](pushbutton-control.md) o [CheckBox](checkbox-control.md) in una finestra di dialogo. Il controllo Checkbox può pubblicare solo gli eventi AddLocal, AddSource, Remove, DoAction e SetProperty. Con Windows installer fornite con Windows Server 2003 e versioni successive, il controllo [SelectionTree](selectiontree-control.md) può pubblicare gli eventi DoAction, ControlEvent e SetProperty ControlEvents. L'autore dell'interfaccia utente deve elencare ControlEvent nella [tabella ControlEvent](controlevent-table.md). Il gestore dell'interfaccia utente del programma di installazione è il sottoscrittore di questi eventi.

[AddLocal ControlEvent](addlocal-controlevent.md)

[AddSource ControlEvent](addsource-controlevent.md)

[CheckExistingTargetPath ControlEvent](checkexistingtargetpath-controlevent.md)

[CheckTargetPath ControlEvent](checktargetpath-controlevent.md)

[DoAction ControlEvent](doaction-controlevent.md)

[EnableRollback ControlEvent](enablerollback-controlevent.md)

[EndDialog ControlEvent](enddialog-controlevent.md)

[NewDialog ControlEvent](newdialog-controlevent.md)

[Reinstallare ControlEvent](reinstall-controlevent.md)

[ReinstallMode ControlEvent](reinstallmode-controlevent.md)

[Rimuovere ControlEvent](remove-controlevent.md)

[Reimposta ControlEvent](reset-controlevent.md)

[Evento di controllo SetInstallLevel](setinstalllevel-controlevent.md)

[Evento di controllo SetProperty](setproperty-controlevent.md)

[SetTargetPath ControlEvent](settargetpath-controlevent.md)

[SpawnDialog ControlEvent](spawndialog-controlevent.md)

[SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent](validateproductid-controlevent.md)

Un [controllo PushButton](pushbutton-control.md) può pubblicare gli eventi seguenti in un controllo [SelectionTree](selectiontree-control.md) o [DirectoryList](directorylist-control.md) che si trova nella stessa finestra di dialogo. Il controllo PushButton deve essere elencato nella tabella ControlEvent e i controlli di sottoscrizione devono essere elencati nella tabella EventMapping.

[SelectionBrowse ControlEvent](selectionbrowse-controlevent.md)

[Controllo DirectoryListUpEvent](directorylistup-controlevent.md)

[DirectoryListNew ControlEvent](directorylistnew-controlevent.md)

[Controllo DirectoryListOpenEvent](directorylistopen-controlevent.md)

Gli eventi di controllo richiedono in genere che l'interfaccia utente sia eseguita a [*livello completo dell'interfaccia*](f-gly.md) utente. La maggior parte degli eventi ControlEvent non funziona con [*un'interfaccia*](r-gly.md) utente ridotta o un'interfaccia utente di base [*perché*](b-gly.md) questi livelli visualizzano solo finestre di dialogo non modali. Gli eventi ActionText, AddSource, SetProgress, TimeRemaining e ScriptInProgress sono eccezioni e funzioneranno nell'interfaccia utente ridotta o di base. Per altre informazioni sui livelli dell'interfaccia utente, [vedere Interfaccia utente Livelli](user-interface-levels.md).

È possibile eseguire [azioni personalizzate pubblicando](custom-actions.md) un controlEvent da un [controllo PushButton o](pushbutton-control.md) da un controllo [Checkbox.](checkbox-control.md) Aggiungere un record alla tabella [ControlEvent con](controlevent-table.md) i nomi della finestra di dialogo e il controllo che pubblica ControlEvent. Questo controllo deve pubblicare un [oggetto DoAction ControlEvent](doaction-controlevent.md) che notifica al programma di installazione di eseguire l'azione personalizzata. Nei Windows XP o precedenti non è possibile eseguire un'azione personalizzata pubblicando un controlevent da [un controllo SelectionTree](selectiontree-control.md).

Per altre informazioni su controlEvent specifici, vedere l'elenco degli eventi [ControlEvent](control-events.md) standard in [Interfaccia utente riferimento](user-interface-reference.md).

 

 
