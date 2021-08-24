---
description: La tabella ControlEvent consente all'autore di specificare gli eventi di controllo avviati quando un utente interagisce con un controllo PushButton, un controllo CheckBox o un controllo SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Tabella ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fec4837fa7d98289495bbb0773ae7260f957485cd87214dabf1999b1e1a876c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693001"
---
# <a name="controlevent-table"></a>Tabella ControlEvent

La tabella ControlEvent consente all'autore di specificare gli eventi di controllo avviati quando un utente interagisce con un controllo [PushButton,](pushbutton-control.md) [un controllo CheckBox](checkbox-control.md)o [un controllo SelectionTree.](selectiontree-control.md) [](control-events.md) Questi sono gli unici controlli che gli utenti possono usare per avviare gli eventi di controllo. Ogni controllo può pubblicare più eventi di controllo. Il programma di installazione avvia ogni evento nell'ordine specificato nella colonna Ordinamento. Ad esempio, un controllo pulsante di comando può pubblicare eventi per avviare una transizione a un'altra finestra di dialogo, uscire dalla sequenza della finestra di dialogo e avviare l'installazione del file.

L'eccezione da notare è che ogni controllo può pubblicare più di un [evento NewDialog](newdialog-controlevent.md) o [un evento SpawnDialog.](spawndialog-controlevent.md) Se è necessario creare più eventi di controllo NewDialog e SpawnDialog in questa tabella, includere anche istruzioni condizionali nei campi Condizione che assicurano che sia pubblicato al massimo un evento. Se vengono selezionati più eventi di controllo NewDialog e SpawnDialog per lo stesso controllo, solo l'evento con il valore più grande nella colonna Ordinamento viene pubblicato quando il controllo viene attivato.

La tabella ControlEvent include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Finestra di dialogo\_  | [Identificatore](identifier.md) | S   | N        |
| controllo\_ | [Identificatore](identifier.md) | S   | N        |
| Event     | [Formattato](formatted.md)   | S   | N        |
| Argomento  | [Formattato](formatted.md)   | S   | N        |
| Condition | [Condition](condition.md)   | S   | S        |
| Ordering  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_
</dt> <dd>

Chiave esterna alla prima colonna della tabella [Dialog](dialog-table.md). La combinazione di questo campo con il \_ campo Controllo identifica un controllo univoco.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_
</dt> <dd>

Chiave esterna alla seconda colonna della tabella [Control](control-table.md). La combinazione di questo campo con il campo \_ Dialog identifica un controllo univoco.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Identificatore che specifica il tipo di evento che deve verificarsi quando l'utente interagisce con il controllo specificato da Dialog \_ e \_ Control. Per un elenco dei valori possibili, vedere [Cenni preliminari su ControlEvent.](controlevent-overview.md)

Per impostare una proprietà con un controllo , inserire \[ Nome proprietà in questo campo e il nuovo valore nel campo \_ \] dell'argomento. Inserire { } nel campo dell'argomento per immettere il valore Null.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>discussione
</dt> <dd>

Valore utilizzato come modificatore quando si attiva un evento specifico.

Ad esempio, l'argomento di [NewDialog ControlEvent](newdialog-controlevent.md) o [SpawnDialog ControlEvent](spawndialog-controlevent.md) è il nome della finestra di dialogo e l'argomento dell'azione [Installa](install-action.md) è un numero che definisce il livello di installazione.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Istruzione condizionale che determina se il programma di installazione attiva l'evento nella colonna Evento. Il programma di installazione attiva l'evento se l'istruzione condizionale nel campo Condizione restituisce True. Inserire quindi 1 in questa colonna per assicurarsi che il programma di installazione attiverà l'evento. Il programma di installazione non attiva l'evento se il campo Condizione contiene un'istruzione che restituisce False. Il programma di installazione non attiva un evento con un valore vuoto nel campo Condizione a meno che nessun altro evento del controllo restituirà True. Se nessuno dei campi Condizione per il controllo denominato nel campo Controllo restituisce True, il programma di installazione attiva l'evento con un campo Condizione vuoto e, se più di un campo Condizione è vuoto, attiva l'unico evento con il valore più grande nel campo \_ Ordinamento. Vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordinare
</dt> <dd>

Intero utilizzato per ordinare diversi eventi associati allo stesso controllo. Deve essere un numero non negativo. Questo campo può essere lasciato vuoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [tabella EventMapping](eventmapping-table.md) elenca i controlli che sottoscriveno un evento del controllo ed elenca l'attributo del controllo da modificare quando tale evento viene pubblicato da un altro controllo o dal programma di installazione.

In Windows XP o sistemi operativi precedenti, gli utenti possono pubblicare [](checkbox-control.md) un evento di controllo solo interagendo con un controllo Checkbox o [un controllo Pushbutton.](pushbutton-control.md) Con Windows Server 2003, gli utenti possono pubblicare un evento del controllo solo interagendo con un controllo [Checkbox,](checkbox-control.md) [un controllo SelectionTree e](selectiontree-control.md)un controllo [Pushbutton.](pushbutton-control.md) L'elenco di altri controlli \_ nel campo Controllo non ha alcun effetto.

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

 

 



