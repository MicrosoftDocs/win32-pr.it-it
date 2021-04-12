---
description: 'Altre informazioni su: funzione JetBeginTransaction'
title: Funzione JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342666"
---
# <a name="jetbegintransaction-function"></a>Funzione JetBeginTransaction


_**Si applica a:** Windows | Windows Server_

## <a name="jetbegintransaction-function"></a>Funzione JetBeginTransaction

La funzione **JetBeginTransaction** fa sì che una sessione entri in una transazione e crei un nuovo punto di salvataggio. Questa funzione può essere chiamata più volte in una singola sessione per provocare la creazione di punti di salvataggio aggiuntivi. Questi punti di salvataggio possono essere utilizzati per conservare o annullare selettivamente le modifiche apportate allo stato del database.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep</p></td>
<td><p>Impossibile avviare una nuova transazione perché la sessione si trova già nella profondità massima del punto di salvataggio consentita dal motore di database.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, la sessione specificata si troverà all'interno di una transazione. Se la sessione si trovava in precedenza all'interno di una transazione, viene creato un nuovo punto di salvataggio.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Il motore di database fornisce un modello di isolamento dello snapshot per le transazioni. Ciò significa che, quando una sessione entra per la prima volta in uno stato transazionale, la sessione visualizzerà l'intero database bloccato nel tempo all'inizio della transazione. Una sessione non deve leggere il blocco dei dati perché può sempre accedere alla versione appropriata di tali dati. Ciò significa che una sessione che aggiorna i dati non bloccherà mai una sessione diversa dalla lettura dei dati.

Un'altra implicazione dell'utilizzo dell'isolamento dello snapshot è il modello di blocco utilizzato per gli aggiornamenti. Il motore di database assegnerà un blocco di scrittura su una determinata parte di dati alla prima sessione che la richiede. Questo blocco di scrittura viene rilasciato quando viene eseguito il commit o l'interruzione completa della transazione in modo che la sessione non si trovi più in una transazione. Mentre una sessione include un blocco di scrittura, qualsiasi altra sessione che richiede lo stesso blocco di scrittura non verrà bloccata fino a quando non sarà disponibile il blocco di scrittura. La seconda sessione avrà invece immediatamente esito negativo con JET_errWriteConflict. Per risolvere questo conflitto, è necessario che la seconda sessione interrompa (o Esegui il commit) la transazione, attenda un periodo di tempo limitato per la prima sessione per eseguire il commit o interrompere la transazione e quindi riavviarla.

A supporto dell'isolamento dello snapshot, il motore di database archivia tutte le versioni di tutti i dati modificati in memoria dal momento in cui è stata avviata per la prima volta la transazione attiva meno recente in una sessione. Questa operazione ha implicazioni importanti per l'applicazione. Qualsiasi comportamento che causa la compilazione di un numero elevato di versioni in memoria può causare l'esaurimento delle dimensioni massime dell'archivio versione (vedere [JET_paramMaxVerPages](./resource-parameters.md) nei [parametri di sistema](./extensible-storage-engine-system-parameters.md) per ulteriori informazioni). Questo comportamento include, tuttavia, non è limitato a aggiornamenti di dimensioni molto elevate in una singola transazione e transazioni con esecuzione prolungata. Di conseguenza, è molto importante configurare correttamente le dimensioni dell'archivio versioni per il carico transazionale previsto dell'applicazione. È anche importante prestare molta attenzione a limitare il numero di aggiornamenti eseguiti in una singola transazione. Inoltre, è importante fare in modo che le transazioni vengano eseguite nel minor tempo possibile in scenari con carico elevato.

È consigliabile che l'applicazione sia sempre nel contesto di una transazione quando si chiamano le API ESE che recuperano o aggiornano i dati. Se questa operazione non viene eseguita, il motore di database eseguirà automaticamente il wrapping di ogni chiamata API ESE di questo tipo in una transazione per conto dell'applicazione. Il costo di queste transazioni molto brevi può essere aggiunto rapidamente in alcuni casi.

Il comportamento predefinito del motore consiste nel limitare l'uso di una sessione allo stesso thread dal momento in cui la prima chiamata a **JetBeginTransaction** viene effettuata fino al momento in cui viene effettuata la chiamata corrispondente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) . Questo comportamento può essere modificato per rimuovere questa restrizione impostando un contesto di sessione personalizzato usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

Il motore di database supporta inoltre le modifiche dello schema transazionale. È ad esempio possibile avviare una nuova transazione, creare una tabella, aggiungere alcune colonne, creare un indice o due, quindi interrompere la transazione. Gli elementi dello schema appena aggiunti verranno rimossi dal database. È inoltre possibile combinare le modifiche dello schema e gli aggiornamenti ordinari del database nella stessa transazione.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
