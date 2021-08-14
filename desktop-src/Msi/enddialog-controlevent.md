---
description: Questo evento notifica al programma di installazione di rimuovere una finestra di dialogo modale. In tutti i casi il programma di installazione rimuove la finestra di dialogo presente.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f6e61ab12f072e31d6e4efc5f3d2b27ef8629c933baad65fb101b1078ca1f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378253"
---
# <a name="enddialog-controlevent"></a>EndDialog ControlEvent

Questo evento notifica al programma di installazione di rimuovere una finestra di dialogo modale. In tutti i casi il programma di installazione rimuove la finestra di dialogo presente.

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

La tabella seguente elenca l'azione dell'evento risultante da argomenti diversi immessi nella [tabella ControlEvent](controlevent-table.md).



| Argomento | Azione del programma di installazione                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esci     | La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore UserExit. Questo argomento non può essere usato in una finestra di dialogo figlio di un'altra finestra di dialogo. |
| Riprova    | La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore Suspend. Questo argomento non può essere usato in una finestra di dialogo figlio di un'altra finestra di dialogo.  |
| Ignora   | La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore Finished. Questo argomento non può essere usato in una finestra di dialogo figlio di un'altra finestra di dialogo. |
| Return   | Il controllo torna all'elemento padre della finestra di dialogo corrente oppure, se non è presente alcun elemento padre, il controllo torna al programma di installazione con il valore Success.                                 |



 

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nelle finestre di dialogo normali la colonna Argomento della tabella [ControlEvent](controlevent-table.md) può essere "Return", "Exit", "Retry" o "Ignore".

Nelle finestre di dialogo di errore la colonna Argument della tabella [ControlEvent](controlevent-table.md) può essere "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes" o "ErrorNo".

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella [tabella ControlEvent](controlevent-table.md) per chiudere una finestra di dialogo.

 

 



