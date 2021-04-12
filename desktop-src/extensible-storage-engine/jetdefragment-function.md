---
description: 'Altre informazioni su: funzione JetDefragment'
title: JetDefragment (funzione)
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349936"
---
# <a name="jetdefragment-function"></a>JetDefragment (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetdefragment-function"></a>JetDefragment (funzione)

La funzione **JetDefragment** avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database. Questa operazione viene eseguita per limitare la crescita del database utilizzando l'allocazione dei dischi esistente in modo più efficiente all'interno del database. Consente inoltre di ridurre working set assicurando che i dati vengano compressi in modo più accurato. Infine, può migliorare le prestazioni dell'applicazione velocizzando le operazioni comuni tramite una migliore organizzazione dei dati.

La deframmentazione del database è un'operazione online e non interrompe le normali attività di database, ad esempio le operazioni di query o gli aggiornamenti dei dati. **JetDefragment** non esegue inoltre una copia di tutti i dati esistenti. Al contrario, deframmenta un database sul posto. Infine, **JetDefragment** ripristina lo spazio interno del database per riutilizzarlo, ma non rilascia spazio in eccesso al sistema operativo file System.

Il formato risultante dei dati può essere molto più efficiente, ma in genere non è ottimale. La deframmentazione è limitata a rilasciare le pagine del database per riutilizzarle che contengono dati che sono già stati eliminati logicamente. La deframmentazione rende inoltre disponibili le pagine del database da riutilizzare in alcuni casi combinando i dati di due pagine quando possono essere inseriti in una singola pagina.

Questa operazione è diversa da [JetCompact](./jetcompact-function.md) , che rende una copia di un database di sola lettura in un formato altamente ottimale.

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*dbid*

Database che verrà deframmentato.

*szTableName*

Parametro non utilizzato. La deframmentazione viene eseguita per l'intero database descritto dall'ID del database specificato.

*pcPasses*

Quando si avvia un'attività di deframmentazione in linea, questo parametro di input imposta il numero massimo di passaggi di deframmentazione. Quando si arresta un'attività di deframmentazione in linea, questo buffer di output viene impostato sul numero di passaggi eseguiti.

Quando questo parametro è impostato su NULL, il numero di sessioni di deframmentazione in linea è illimitato.

*pcSeconds*

Quando si avvia un'attività di deframmentazione in linea, questo parametro di input imposta il tempo massimo per la deframmentazione. Quando si arresta un'attività di deframmentazione in linea, questo buffer di output viene impostato sul periodo di tempo utilizzato per la deframmentazione.

Quando questo parametro è impostato su NULL o se *pcSeconds* punta a un valore negativo, il tempo massimo per la deframmentazione è illimitato.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDefragmentAvailSpaceTreesOnly</p></td>
<td><p>Deframmenta la porzione di spazio disponibile nell'allocazione dello spazio del database ESE. Lo spazio del database è suddiviso in due tipi, spazio di proprietà e spazio disponibile. Lo spazio di proprietà viene allocato a una tabella o a un indice, mentre lo spazio disponibile è pronto per l'utilizzo rispettivamente nella tabella o nell'indice. Lo spazio disponibile è molto più dinamico nel comportamento e richiede la deframmentazione in linea più che lo spazio di proprietà o i dati di tabella o di indice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Avvia una nuova attività di deframmentazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Arresta un'attività di deframmentazione.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>Il database scelto per la deframmentazione è di sola lettura e non può essere aggiornato in alcun modo, inclusa la deframmentazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>La sessione specificata si trova nello stato pronto per il commit e non può avviare nuovi aggiornamenti fino a quando non viene eseguito il commit o il rollback della transazione corrente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>L'ID del database specificato non corrisponde a un database noto nell'istanza di.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La sessione specificata ha solo privilegi di sola lettura e non può avviare un'attività che può eseguire un aggiornamento, inclusa la deframmentazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragAlreadyRunning</p></td>
<td><p>È stata passata l'opzione JET_bitDefragmentBatchStart, ma un'attività di deframmentazione sta già eseguendo la deframmentazione nel database specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>È stata passata l'opzione JET_bitDefragmentBatchStop, ma l'attività di deframmentazione non è attualmente in esecuzione.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, viene eseguita l'azione richiesta di avvio di un'attività di deframmentazione per i dati specificati con le opzioni specificate oppure viene eseguita l'azione di arresto di un'attività di deframmentazione esistente.

In caso di errore, l'azione richiesta di avvio o arresto di un processo di deframmentazione in linea non viene eseguita. Non si verificano altri effetti collaterali.

#### <a name="remarks"></a>Commenti

La deframmentazione in linea viene controllata sia dall'impostazione di un parametro sia da questa API. Il valore predefinito del parametro di sistema è JET_OnlineDefragAll, ovvero la deframmentazione è abilitata per tutte le strutture di dati supportate. Tuttavia, utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md), è possibile disabilitare la deframmentazione in linea o abilitarla selettivamente solo per gli alberi dello spazio del database, solo per i database, solo per i file di flusso o una combinazione di queste opzioni. Se l'impostazione di sistema per la deframmentazione in linea è impostata su un'impostazione obsoleta, **JetDefragment** considererà l'impostazione come JET_OnlineDefragAll.

È possibile eseguire al massimo un'attività per ogni database. L'attività viene eseguita come thread nel processo che ospita ESE.

La sessione utilizzata per avviare l'attività di deframmentazione in linea può essere successivamente utilizzata per le operazioni di database mentre l'attività di deframmentazione continua, perché l'attività di deframmentazione alloca la propria sessione. La sessione specificata viene utilizzata solo per verificare le autorizzazioni associate alla sessione di avvio dell'attività e non viene effettivamente utilizzata per le operazioni di deframmentazione.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetDefragmentW</strong> (Unicode) e <strong>JetDefragmentA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment2](./jetdefragment2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
