---
description: La tabella EventMapping elenca i controlli che sottoscriveno alcuni eventi di controllo ed elenca l'attributo da modificare quando l'evento viene pubblicato da un altro controllo o dal Windows Installer.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Tabella EventMapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f17380e3e91669926ef50532c36fec71f44d61eb2ed7273d053defe45fa874e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963111"
---
# <a name="eventmapping-table"></a>Tabella EventMapping

La tabella EventMapping elenca i controlli che sottoscriveno alcuni eventi di controllo ed elenca l'attributo da modificare quando l'evento viene pubblicato da un altro controllo o dal Windows Installer.

La tabella EventMapping include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Finestra di dialogo\_  | [Identificatore](identifier.md) | S   | N        |
| controllo\_ | [Identificatore](identifier.md) | S   | N        |
| Evento     | [Identificatore](identifier.md) | S   | N        |
| Attributo | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_
</dt> <dd>

Chiave esterna alla prima colonna della tabella [di dialogo](dialog-table.md). Questo campo e il campo \_ Controllo identificano insieme un controllo.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_
</dt> <dd>

Chiave esterna alla seconda colonna della tabella [di controllo](control-table.md). Questo campo e il campo \_ Dialogo identificano insieme un controllo.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Questo campo è un identificatore che specifica il tipo di evento sottoscritto dal controllo . Per altre informazioni, vedere [Cenni preliminari su ControlEvent.](controlevent-overview.md)

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo
</dt> <dd>

Nome dell'attributo Control impostato quando viene ricevuto \_ l'evento nella colonna Event. L'argomento dell'evento viene passato come argomento della chiamata all'attributo per modificare questo attributo del controllo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [tabella ControlEvent](controlevent-table.md) specifica gli eventi del controllo che vengono avviati quando un utente interagisce con un controllo [PushButton](pushbutton-control.md), [un controllo CheckBox](checkbox-control.md)o [un controllo SelectionTree](selectiontree-control.md). Questi sono gli unici controlli che un utente può usare per avviare gli eventi di controllo.

Più controlli in una finestra di dialogo possono sottoscrivere lo stesso evento.

L'elenco seguente identifica gli usi tipici per la tabella EventMapping:

-   Per sottoscrivere un controllo di testo a [un oggetto ActionText ControlEvent,](actiontext-controlevent.md) [ActionData ControlEvent,](actiondata-controlevent.md) [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) o [TimeRemaining ControlEvent](timeremaining-controlevent.md) pubblicato dal programma di Windows Installer. [](text-control.md)
-   Per sottoscrivere [un controllo ProgressBar o](progressbar-control.md) Un controllo Barra di [avanzamento](billboard-control.md) a un [oggetto SetProgress ControlEvent](setprogress-controlevent.md).
-   Per sottoscrivere [un controllo DirectoryCombo](directorycombo-control.md) a [un controllo IgnoreChange ControlEvent](ignorechange-controlevent.md).
-   Per disabilitare automaticamente [un controllo PushButton](pushbutton-control.md) che si trova nella stessa finestra di dialogo con [un controllo SelectionTree](selectiontree-control.md). Per disabilitare il pulsante push quando non sono elencate funzionalità nel controllo [SelectionTree](selectiontree-control.md), usare la tabella EventMapping per sottoscrivere il controllo PushButton a [un controllo SelectionNoItems ControlEvent](selectionnoitems-controlevent.md). Immettere **Abilita** nel campo Attributi della tabella EventMapping.
-   Per visualizzare un [controllo Testo](text-control.md) che mostra il percorso di installazione per la funzionalità selezionata in un [controllo SelectionTree](selectiontree-control.md) nella stessa finestra di dialogo. Usare la tabella EventMapping per sottoscrivere il controllo [Text](text-control.md) sia a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) che [a SelectionPath ControlEvent](selectionpath-controlevent.md) pubblicati dal [controllo SelectionTree](selectiontree-control.md).
-   Per visualizzare [](text-control.md) un controllo di testo che mostra una descrizione dell'elemento evidenziato in un [controllo SelectionTree](selectiontree-control.md) che si trova nella stessa finestra di dialogo, usare la tabella EventMapping per sottoscrivere il controllo text [](text-control.md) a [selectionDescription ControlEvent,](selectiondescription-controlevent.md) [SelectionSize ControlEvent](selectionsize-controlevent.md) o [SelectionAction ControlEvent.](selectionaction-controlevent.md) Immettere **Testo** nel campo Attributo della tabella EventMapping.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



