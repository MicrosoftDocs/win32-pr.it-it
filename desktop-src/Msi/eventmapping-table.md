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
# <a name="eventmapping-table"></a>Tabella EventMapping

La tabella EventMapping elenca i controlli che sottoscrivono alcuni eventi di controllo ed elenca l'attributo da modificare quando l'evento viene pubblicato da un altro controllo o dal Windows Installer.

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

Chiave esterna per la prima colonna della tabella della [finestra di dialogo](dialog-table.md). Questo campo e il campo di controllo \_ identificano un controllo.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_
</dt> <dd>

Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md). Questo campo e il campo della finestra di dialogo \_ identificano un controllo.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Questo campo è un identificatore che specifica il tipo di evento sottoscritto dal controllo. Per altre informazioni, vedere [Panoramica di ControlEvent](controlevent-overview.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo
</dt> <dd>

Nome dell'attributo del controllo \_ impostato quando viene ricevuto l'evento nella colonna dell'evento. L'argomento dell'evento viene passato come argomento della chiamata di attributo per modificare questo attributo del controllo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [tabella ControlEvent](controlevent-table.md) specifica gli eventi di controllo che vengono avviati quando un utente interagisce con un [controllo pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md). Questi sono gli unici controlli che un utente può usare per avviare gli eventi di controllo.

Più di un controllo in una finestra di dialogo può sottoscrivere lo stesso evento.

Nell'elenco seguente vengono identificati gli utilizzi tipici della tabella EventMapping:

-   Per sottoscrivere [un controllo di testo](text-control.md) a un [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) o [TimeRemaining](timeremaining-controlevent.md) ControlEvent pubblicato dal Windows Installer.
-   Per sottoscrivere un controllo [ProgressBar](progressbar-control.md) o un [controllo Billboard](billboard-control.md) a un [ControlEvent di avanzamento](setprogress-controlevent.md).
-   Per sottoscrivere un [controllo DirectoryCombo](directorycombo-control.md) a un [IgnoreChange ControlEvent](ignorechange-controlevent.md).
-   Per disabilitare automaticamente un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo con un [controllo SelectionTree](selectiontree-control.md). Per disabilitare il pulsante push quando nessuna funzionalità è elencata nel [controllo SelectionTree](selectiontree-control.md), usare la tabella EventMapping per sottoscrivere il controllo pulsante a un [ControlEvent SelectionNoItems](selectionnoitems-controlevent.md). Immettere **Enable** nel campo Attributes della tabella EventMapping.
-   Per visualizzare un [controllo di testo](text-control.md) che mostra il percorso di installazione per la funzionalità selezionata in un [controllo SelectionTree](selectiontree-control.md) nella stessa finestra di dialogo. Usare la tabella EventMapping per sottoscrivere [il controllo di testo](text-control.md) in [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) e [SelectionPath ControlEvent](selectionpath-controlevent.md) pubblicati dal [controllo SelectionTree](selectiontree-control.md).
-   Per visualizzare un [controllo testo](text-control.md) che mostra una descrizione dell'elemento evidenziato in un [controllo SelectionTree](selectiontree-control.md) che si trova nella stessa finestra di dialogo, usare la tabella EventMapping per sottoscrivere il [controllo di testo](text-control.md) a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) o [SelectionAction](selectionaction-controlevent.md)ControlEvent. Immettere il **testo** nel campo attributo della tabella EventMapping.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



