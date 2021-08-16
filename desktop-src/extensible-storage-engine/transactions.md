---
description: 'Altre informazioni su: Transazioni (Windows eventi)'
title: Transazioni (eventi di Windows)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e223c95d7f8af5a4350786891d58b72c508443e459990d413d5b46bc2e12a2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107056"
---
# <a name="transactions-windows-events"></a>Transazioni (eventi di Windows)


_**Si applica a:** Windows | Windows Server_

## <a name="transactions"></a>Transazioni

Le transazioni ESE sono unità logiche di elaborazione che controllano il modo in cui un'applicazione vede e modifica le righe nel database. L'applicazione può usare punti di salvataggio delle transazioni per determinare se mantenere o eliminare un particolare set di modifiche al database. Tutte le transazioni in ESE sono atomiche, coerenti, isolate e durevoli (ACID), come descritto di seguito:

  - **Atomico:** Tutti gli aggiornamenti nella transazione vengono visualizzati nel database o vengono eliminati.

<!-- end list -->

  - **Coerente:** Il database verrà sempre avviato in uno stato legale e terminerà sempre in un altro stato legale. Per le applicazioni ESE, il motore di database controlla alcuni vincoli semplici, ad esempio l'univocità di un indice univoco, ma l'applicazione stessa definirà quasi tutti gli altri aspetti di ciò che significa che il database sia in uno stato valido.

<!-- end list -->

  - **Isolamento:** Le transazioni sono isolate dagli aggiornamenti da altre sessioni. Una transazione non visualizza mai un set parziale di modifiche apportate da un'altra transazione.

<!-- end list -->

  - **Durevole:** Dopo che il motore di database ha riconosciuto che è stato eseguito il commit di una transazione, le relative modifiche sono persistenti nel database. La durabilità di una transazione può essere facoltativamente derogata per motivi di prestazioni.

Le transazioni vengono eseguite entro i limiti delle chiamate a [JetBeginTransaction](./jetbegintransaction-function.md) e [JetCommitTransaction](./jetcommittransaction-function.md) [o JetRollback.](./jetrollback-function.md) Quando l'applicazione immette la transazione, il database risulta bloccato nell'istanza nel momento in cui inizia la transazione. Questo processo è detto isolamento dello snapshot. Se la transazione viene terminata chiamando [JetRollback](./jetrollback-function.md), nessuna delle operazioni eseguite nella transazione viene eseguita nel database. Se il processo o il computer si arresta in modo anomalo prima della chiamata a [JetCommitTransaction,](./jetcommittransaction-function.md) è uguale alla chiamata [a JetRollback.](./jetrollback-function.md)

In questa procedura viene illustrato come avviare ed eseguire il commit di una transazione che legge e aggiorna i dati in un database.

### <a name="to-start-and-commit-a-transaction"></a>Per avviare ed eseguire il commit di una transazione

1.  Chiamare [JetBeginTransaction o](./jetbegintransaction-function.md) [JetBeginTransaction2 con](./jetbegintransaction2-function.md) l'ID sessione per avviare la transazione.

2.  Spostare il cursore nel record desiderato chiamando [JetMove](./jetmove-function.md) con JET_MoveFirst specificato nel *parametro cRow.* Per altre informazioni su come spostare il cursore, vedere [l'argomento Indicizzazione nell'argomento Tabella](./indexing-in-the-table.md) .

3.  Chiamare [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sul record corrente con JET_ColInfo specificato nel *parametro InfoLevel* per recuperare l'ID colonna per la colonna. L'ID colonna viene restituito [nella JET_COLUMNDEF](./jet-columndef-structure.md) struttura .

4.  Chiamare [JetSetColumn con](./jetsetcolumn-function.md) l'ID di sessione, l'ID tabella e l'ID di colonna della colonna aggiornata. I dati della colonna sono contenuti nel *parametro pvData.*

5.  Chiamare [JetCommitTransaction per](./jetcommittransaction-function.md) eseguire il commit della transazione nel database.

Il modo in cui un motore di database ESE implementa l'isolamento dello snapshot presenta alcune importanti differenze rispetto ai modelli tradizionali di isolamento e blocco dei database relazionali. Quando una transazione legge una riga, può sempre accedere alla riga senza errori o in attesa del rilascio di un blocco da parte di altre sessioni. Quando una transazione tenta di aggiornare una riga, avrà esito positivo se è la prima sessione ad aggiornare tale riga, che è il primo writer a essere in grado di eseguire la scrittura. Se la sessione non è il primo writer, avrà immediatamente esito negativo con un errore di conflitto di scrittura. La sessione deve quindi interrompere la transazione, attendere (in genere tramite un ritardo casuale), che l'altra transazione eseeguirà il commit delle modifiche, quindi ripetere la transazione. Il motore di database non farà in modo che la sessione attenda automaticamente il completamento dell'aggiornamento dell'altra transazione. In genere, una transazione verifica se può aggiornare una riga all'interno della [chiamata a JetUpdate.](./jetupdate-function.md) Se non riesce a bloccare la riga per l'aggiornamento, [JetUpdate avrà](./jetupdate-function.md) esito negativo con JET_errWriteConflict.

Le sessioni sono limitate a un thread dal momento in cui la transazione inizia fino alla fine della transazione. È consigliabile eseguire tutte le operazioni di aggiornamento e recupero in una transazione. ESE supporta anche le modifiche dello schema, ad esempio la creazione di tabelle e l'aggiunta di colonne all'interno della transazione. Sia l'aggiornamento che le modifiche dello schema possono essere eseguiti nella stessa transazione. Al termine della transazione con [JetCommitTransaction](./jetcommittransaction-function.md), l'aggiornamento viene registrato nel file di log delle transazioni. Questi file possono essere usati per mantenere uno stato coerente a livello logico in caso di chiusura imprevista del processo o arresto del sistema.

Le transazioni possono essere annidate fino a 7 livelli con chiamate corrispondenti [a JetBeginTransaction](./jetbegintransaction-function.md) e [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) annidate l'una all'interno dell'altra. In questo modo l'applicazione può eseguire il rollback di una parte della transazione senza dover eseguire il back-out dell'intera transazione. La chiamata annidata [a JetCommitTransaction](./jetcommittransaction-function.md) indica che questo livello di elaborazione è stato completato. Tuttavia, non viene eseguito il commit della transazione nel database fino alla chiamata più esterna per eseguire il commit della [transazione con JetCommitTransaction.](./jetcommittransaction-function.md)

Le colonne di aggiornamento del deposito possono essere aggiornate contemporaneamente da più sessioni senza errori con Jet_errWriteConflict. La [funzione JetEscrowUpdate](./jetescrowupdate-function.md) può essere chiamata solo su colonne del deposito, colonne create con Jet_bitColumnEscrowUpdate.
