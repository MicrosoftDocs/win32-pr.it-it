---
description: Nell'esempio seguente viene illustrato come creare una finestra di messaggio condizionale che viene visualizzata e avvisa l'utente che un'attività in background è ancora in esecuzione ogni volta che l'utente attiva un controllo visualizzato in modo anomalo.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Creazione di un'attesa. . ." MessageBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528866"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Creazione di un condizionale "attendere..." MessageBox

Nell'esempio seguente viene illustrato come creare una finestra di messaggio condizionale che viene visualizzata e avvisa l'utente che un'attività in background è ancora in esecuzione ogni volta che l'utente attiva un controllo visualizzato in modo anomalo.

Nell'esempio viene inoltre illustrato il modo in cui il [ControlEvent SpawnWaitDialog](spawnwaitdialog-controlevent.md) può essere utilizzato in genere per proteggere un controllo che attiva un'azione dipendente dal completamento di un'attività in background.

In questo esempio una [finestra di dialogo di selezione](selection-dialog.md) contenente tre controlli pulsante di comando con etichetta **Installa ora**, **Avanti** e **costo disco** viene visualizzata all'utente durante il processo di installazione. Tuttavia, il programma di installazione esegue anche un'attività di costo dello spazio su disco in background durante la visualizzazione di questa finestra di dialogo. L'autore vuole proteggere questi pulsanti dall'attivazione e vuole che venga visualizzata la finestra di messaggio "Attendi" per visualizzare se l'utente fa clic su uno dei pulsanti prima che i costi siano stati completati. L'autore desidera inoltre che questa finestra di messaggio contenga un pulsante **Annulla** e scomparirà non appena l'attività in background viene completata.

**Per visualizzare una finestra di dialogo in cui viene chiesto all'utente di attendere il completamento dei costi del disco in background**

1.  Utilizzare le funzionalità di creazione del programma di installazione per aggiungere una nuova finestra di dialogo modale, denominata **WaitForCosting**, nella [tabella della finestra di dialogo](dialog-table.md). Nella finestra di dialogo dovrebbe essere visualizzata una stringa di testo con la dicitura "attendere che i costi dello spazio su disco siano completati".
2.  Aggiungere un singolo controllo pulsante di push a questa finestra di dialogo, con etichetta **Annulla**, creandolo nella [tabella dei controlli](control-table.md).
3.  Collegare il pulsante **Annulla** push a un ControlEvent che chiude la finestra di dialogo **WaitForCosting** mediante la creazione di un [ControlEvent EndDialog](enddialog-controlevent.md) nella [tabella ControlEvent](controlevent-table.md). Impostare l'argomento dell'evento di controllo EndDialog su Exit.
4.  Collegare un [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) ai pulsanti **Installa ora**, **Avanti** e costo del **disco** per i pulsanti di comando visualizzati nella finestra di [dialogo di selezione](selection-dialog.md) . Impostare l'argomento di questo ControlEvent nella tabella ControlEvent in modo che sia la finestra di dialogo **WaitForCosting** e impostare l'espressione nella colonna condizione della tabella su: [**CostingComplete**](costingcomplete.md) = 1.

 

 



