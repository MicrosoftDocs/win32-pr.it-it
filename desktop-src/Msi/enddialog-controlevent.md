---
description: Questo evento notifica al programma di installazione di rimuovere una finestra di dialogo modale. In tutti i casi il programma di installazione rimuove la finestra di dialogo corrente.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: ControlEvent EndDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231878"
---
# <a name="enddialog-controlevent"></a>ControlEvent EndDialog

Questo evento notifica al programma di installazione di rimuovere una finestra di dialogo modale. In tutti i casi il programma di installazione rimuove la finestra di dialogo corrente.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

La tabella seguente elenca l'azione dell'evento risultante da argomenti diversi immessi nella [tabella ControlEvent](controlevent-table.md).



| Argomento | Azione eseguita dal programma di installazione                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esci     | La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore UserExit. Questo argomento non può essere utilizzato in una finestra di dialogo figlio di un'altra finestra di dialogo. |
| Riprova    | La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore Suspend. Questo argomento non può essere utilizzato in una finestra di dialogo figlio di un'altra finestra di dialogo.  |
| Ignora   | La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore terminato. Questo argomento non può essere utilizzato in una finestra di dialogo figlio di un'altra finestra di dialogo. |
| Return   | Il controllo torna all'elemento padre della finestra di dialogo presente o, se non è presente alcun elemento padre, il controllo torna al programma di installazione con il valore di operazione riuscita.                                 |



 

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nelle finestre di dialogo normali la colonna Argument della [tabella ControlEvent](controlevent-table.md) può essere "Return", "Exit", "Retry" o "ignore".

Nelle finestre di dialogo di errore la colonna Argument della [tabella ControlEvent](controlevent-table.md) può essere "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes" o "errorno".

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per chiudere una finestra di dialogo.

 

 



