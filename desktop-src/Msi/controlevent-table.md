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
# <a name="controlevent-table"></a>Tabella ControlEvent

La tabella ControlEvent consente all'autore di specificare gli [eventi del controllo](control-events.md) avviati quando un utente interagisce con un [controllo pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md). Questi sono gli unici controlli che gli utenti possono usare per avviare gli eventi di controllo. Ogni controllo può pubblicare più eventi di controllo. Il programma di installazione avvia ogni evento nell'ordine specificato nella colonna ordering. Un controllo pulsante di push, ad esempio, può pubblicare eventi per avviare una transizione a un'altra finestra di dialogo, uscire dalla sequenza della finestra di dialogo e avviare l'installazione del file.

L'eccezione da tenere presente è che ogni controllo può pubblicare un [NewDialog](newdialog-controlevent.md) o un evento [SpawnDialog](spawndialog-controlevent.md) . Se è necessario creare più eventi di controllo NewDialog e SpawnDialog in questa tabella, includere anche le istruzioni condizionali nei campi condizione che assicurano la pubblicazione al massimo un evento. Se per lo stesso controllo sono selezionati più eventi di controllo NewDialog e SpawnDialog, solo l'evento con il valore più grande nella colonna ordering viene pubblicato quando il controllo è attivato.

La tabella ControlEvent include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Finestra di dialogo\_  | [Identificatore](identifier.md) | S   | N        |
| controllo\_ | [Identificatore](identifier.md) | S   | N        |
| Evento     | [Formattato](formatted.md)   | S   | N        |
| Argomento  | [Formattato](formatted.md)   | S   | N        |
| Condizione | [Condition](condition.md)   | S   | S        |
| Ordering  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_
</dt> <dd>

Chiave esterna per la prima colonna della tabella della [finestra di dialogo](dialog-table.md). La combinazione di questo campo con il campo del controllo \_ identifica un controllo univoco.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_
</dt> <dd>

Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md). Combinando questo campo con il campo finestra di dialogo viene \_ identificato un controllo univoco.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Identificatore che specifica il tipo di evento che deve essere eseguita quando l'utente interagisce con il controllo specificato dalla finestra di dialogo \_ e dal controllo \_ . Per un elenco di valori possibili, vedere [Panoramica di ControlEvent](controlevent-overview.md).

Per impostare una proprietà con un controllo, inserire \[ il \_ nome \] della proprietà in questo campo e il nuovo valore nel campo argomento. Inserire {} nel campo argument per immettere il valore null.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argomento
</dt> <dd>

Valore utilizzato come modificatore quando si attiva un particolare evento.

Ad esempio, l'argomento di [NewDialog ControlEvent](newdialog-controlevent.md) o [SpawnDialog ControlEvent](spawndialog-controlevent.md) è il nome della finestra di dialogo e l'argomento dell' [azione di installazione](install-action.md) è un numero che definisce il livello di installazione.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Istruzione condizionale che determina se il programma di installazione attiva l'evento nella colonna evento. Il programma di installazione attiva l'evento se l'istruzione condizionale nel campo condizione restituisce true. Inserire quindi un valore 1 in questa colonna per assicurarsi che l'evento venga attivato dal programma di installazione. Il programma di installazione non attiva l'evento se il campo condizione contiene un'istruzione che restituisce false. Il programma di installazione non attiva un evento con uno spazio vuoto nel campo condizione, a meno che nessun altro evento del controllo restituisca true. Se nessuno dei campi della condizione per il controllo denominato nel campo del controllo \_ restituisce true, il programma di installazione attiva l'evento con un campo di condizione vuoto e se più di un campo di condizione è vuoto, attiva l'unico evento con il valore più grande nel campo di ordinamento. Vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordinare
</dt> <dd>

Integer usato per ordinare diversi eventi collegati allo stesso controllo. Deve essere un numero non negativo. Questo campo può essere lasciato vuoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [tabella EventMapping](eventmapping-table.md) elenca i controlli che sottoscrivono un evento di controllo ed elenca l'attributo del controllo da modificare quando l'evento viene pubblicato da un altro controllo o dal programma di installazione.

In Windows XP o nei sistemi operativi precedenti, gli utenti possono pubblicare un evento di controllo solo interagendo con un controllo [CheckBox](checkbox-control.md) o un [controllo pulsante](pushbutton-control.md). Con Windows Server 2003, gli utenti possono pubblicare un evento di controllo solo interagendo con un controllo [CheckBox](checkbox-control.md), un [controllo SelectionTree](selectiontree-control.md)e un [controllo pulsante](pushbutton-control.md). L'elenco di altri controlli nel \_ campo del controllo non ha alcun effetto.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



