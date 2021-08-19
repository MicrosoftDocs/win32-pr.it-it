---
description: L'esempio seguente illustra come creare una finestra di messaggio condizionale che viene visualizzata e avvisa l'utente che un'attività in background è ancora in esecuzione ogni volta che l'utente attiva un controllo visualizzato in modo prematuro.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Creazione di un oggetto "Please Wait . . ." Finestra di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f7abc26254b9656ca3d522fa7458ded30fbf09cc20a39a9f960e7509bee8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086361"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Creazione di un'istruzione condizionale "Please Wait..." Finestra di messaggio

L'esempio seguente illustra come creare una finestra di messaggio condizionale che viene visualizzata e avvisa l'utente che un'attività in background è ancora in esecuzione ogni volta che l'utente attiva un controllo visualizzato in modo prematuro.

L'esempio illustra anche come usare in genere [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) per proteggere un controllo che attiva un'azione dipendente dal completamento di un'attività in background.

In questo esempio, durante il processo di installazione viene visualizzata  una finestra di dialogo di selezione contenente tre controlli pulsante push con etichetta Installa ora **,** Avanti e Costo disco. [](selection-dialog.md) Tuttavia, il programma di installazione esegue anche un'attività di costing dello spazio su disco in background durante la visualizzazione di questa finestra di dialogo. L'autore vuole proteggere questi pulsanti dall'attivazione e vuole che venga visualizzata una finestra di messaggio "Please wait" (Attendere) se l'utente fa clic su uno dei pulsanti prima del completamento della determinazione dei costi. L'autore vuole anche che questa finestra di messaggio contenga un **pulsante** Annulla e scompaia non appena l'attività in background è stata completata.

**Per visualizzare una finestra di dialogo in cui viene chiesto all'utente di attendere il completamento della determinazione dei costi del disco in background**

1.  Usare le funzionalità di creazione del programma di installazione per aggiungere una nuova finestra di dialogo modale, denominata **WaitForCosting**, nella [tabella Dialog](dialog-table.md). Nella finestra di dialogo dovrebbe essere visualizzata una stringa di testo che indica "Attendere il completamento della determinazione dei costi dello spazio su disco".
2.  Aggiungere un singolo controllo pulsante push a questa finestra di dialogo, con l'etichetta **Cancel,** tramite la creazione nella [tabella Control](control-table.md).
3.  Collegare il **pulsante** Annulla a un ControlEvent che chiude la finestra di dialogo **WaitForCosting** mediante la creazione di [un evento ControlEvent EndDialog](enddialog-controlevent.md) nella [tabella ControlEvent](controlevent-table.md). Impostare l'argomento dell'evento EndDialog Control su Exit.
4.  Collegare un oggetto [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) ai controlli pulsante **esistente** Installa ora **,** Avanti e Costo disco visualizzati nella finestra di [dialogo Selezione.](selection-dialog.md) Impostare l'argomento di controlEvent nella tabella ControlEvent come finestra di dialogo **WaitForCosting** e impostare l'espressione nella colonna Condizione della tabella su [**CostingComplete**](costingcomplete.md) =1.

 

 



