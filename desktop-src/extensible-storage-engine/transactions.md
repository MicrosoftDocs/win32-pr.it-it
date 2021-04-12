---
description: 'Altre informazioni su: transazioni (eventi di Windows)'
title: Transazioni (eventi di Windows)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 90b5b566f5ff961ce7b0ae3725f580e1f39c041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346956"
---
# <a name="transactions-windows-events"></a>Transazioni (eventi di Windows)


_**Si applica a:** Windows | Windows Server_

## <a name="transactions"></a>Transazioni

Le transazioni ESE sono unità logiche di elaborazione che controllano il modo in cui un'applicazione rileva e modifica le righe nel database. L'applicazione può utilizzare i punti di salvataggio delle transazioni per determinare se conservare o eliminare un particolare set di modifiche al database. Tutte le transazioni in ESE sono atomiche, coerenti, isolate e durevoli (ACID), come descritto di seguito:

  - **Atomic:** Tutti gli aggiornamenti nella transazione vengono visualizzati nel database o vengono eliminati.

<!-- end list -->

  - **Coerente:** Il database viene sempre avviato in uno stato valido e termina sempre con un altro stato valido. Per le applicazioni ESE, il motore di database controllerà alcuni vincoli semplici, ad esempio l'univocità di un indice univoco, ma l'applicazione stessa definirà quasi tutti gli altri aspetti del modo in cui il database si trova in uno stato valido.

<!-- end list -->

  - **Isolamento:** Le transazioni sono isolate dagli aggiornamenti da altre sessioni. Una transazione non visualizzerà mai un set parziale di modifiche apportate da un'altra transazione.

<!-- end list -->

  - **Durevole:** Dopo che il motore di database ha confermato che è stato eseguito il commit di una transazione, le modifiche sono persistenti nel database. La durabilità di una transazione può essere facoltativamente rinunciata per motivi di prestazioni.

Le transazioni vengono eseguite entro i limiti delle chiamate a [JetBeginTransaction](./jetbegintransaction-function.md) e [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md). Quando l'applicazione immette la transazione, il database viene visualizzato bloccato nell'istanza nel momento in cui inizia la transazione. Questa operazione è denominata isolamento dello snapshot. Se la transazione viene terminata chiamando [JetRollback](./jetrollback-function.md), nessuna delle operazioni eseguite nella transazione viene sottoposta a commit nel database. Se il processo o il computer si arresta in modo anomalo prima della chiamata a [JetCommitTransaction](./jetcommittransaction-function.md) , equivale alla chiamata a [JetRollback](./jetrollback-function.md).

Questa procedura illustra come avviare ed eseguire il commit di una transazione che legge e aggiorna i dati in un database.

### <a name="to-start-and-commit-a-transaction"></a>Per avviare ed eseguire il commit di una transazione

1.  Chiamare [JetBeginTransaction](./jetbegintransaction-function.md) o [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) con l'ID sessione per avviare la transazione.

2.  Spostare il cursore sul record desiderato chiamando [JetMove](./jetmove-function.md) con JET_MoveFirst specificato nel parametro *Crow* . Per ulteriori informazioni su come spostare il cursore, vedere l'argomento [indicizzazione nell'](./indexing-in-the-table.md) argomento della tabella.

3.  Chiamare [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sul record corrente con JET_ColInfo specificato nel parametro *InfoLevel* per recuperare l'ID di colonna per la colonna. L'ID di colonna viene restituito nella struttura [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Chiamare [JetSetColumn](./jetsetcolumn-function.md) con l'ID di sessione, l'ID di tabella e l'ID di colonna della colonna aggiornata. I dati della colonna sono contenuti nel parametro *pvData* .

5.  Chiamare [JetCommitTransaction](./jetcommittransaction-function.md) per eseguire il commit della transazione nel database.

Il modo in cui un motore di database ESE implementa l'isolamento dello snapshot presenta alcune differenze importanti rispetto ai modelli tradizionali di isolamento e blocco del database relazionale. Quando una transazione legge una riga, può accedere sempre alla riga senza avere esito negativo o attendere che altre sessioni rilascino un blocco. Quando una transazione tenta di aggiornare una riga, avrà esito positivo se è la prima sessione per aggiornare la riga, ovvero il primo writer WINS. Se la sessione non è il primo writer, avrà immediatamente esito negativo con un errore di conflitto di scrittura. La sessione deve quindi interrompere la transazione, attendere (in genere tramite un ritardo casuale) per eseguire il commit delle modifiche da parte dell'altra transazione, quindi ripetere la transazione. Il motore di database non farà in modo che tale sessione attenda automaticamente il completamento dell'aggiornamento dell'altra transazione. In genere, una transazione verifica se è possibile aggiornare una riga all'interno della chiamata [JetUpdate](./jetupdate-function.md) . Se non è possibile bloccare la riga per l'aggiornamento, [JetUpdate](./jetupdate-function.md) avrà esito negativo con JET_errWriteConflict.

Le sessioni sono limitate a un thread dal momento in cui la transazione inizia fino alla fine della transazione. È consigliabile eseguire tutte le operazioni di aggiornamento e recupero in una transazione. ESE supporta inoltre modifiche dello schema, ad esempio la creazione di tabelle e l'aggiunta di colonne all'interno della transazione. È possibile eseguire le modifiche di aggiornamento e dello schema nella stessa transazione. Al termine della transazione con [JetCommitTransaction](./jetcommittransaction-function.md), l'aggiornamento viene registrato nel file di log delle transazioni. Questi file possono essere utilizzati per mantenere uno stato logicamente coerente in caso di interruzione imprevista di un processo o di arresto del sistema.

Le transazioni possono essere annidate fino a 7 livelli con chiamate corrispondenti a [JetBeginTransaction](./jetbegintransaction-function.md) e [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) annidate l'una all'altra. Ciò consente all'applicazione di eseguire il rollback di una parte della transazione senza dover eseguire il rollback dell'intera transazione. La chiamata nidificata a [JetCommitTransaction](./jetcommittransaction-function.md) indica che questo livello di elaborazione è stato completato; Tuttavia, non viene eseguito il commit della transazione nel database fino a quando la chiamata più esterna non esegue il commit della transazione con [JetCommitTransaction](./jetcommittransaction-function.md).

È possibile aggiornare le colonne di aggiornamento del deposito simultaneamente da più sessioni senza errori Jet_errWriteConflict. La funzione [JetEscrowUpdate](./jetescrowupdate-function.md) può essere chiamata solo su colonne escrow, che sono state create con Jet_bitColumnEscrowUpdate.
