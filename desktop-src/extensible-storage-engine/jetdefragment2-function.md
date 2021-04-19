---
description: 'Altre informazioni su: funzione JetDefragment2'
title: JetDefragment2 (funzione)
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323810"
---
# <a name="jetdefragment2-function"></a>JetDefragment2 (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>JetDefragment2 (funzione)

La funzione **JetDefragment2** consente di avviare e arrestare le attività di deframmentazione del database che consentono di migliorare l'organizzazione dei dati all'interno di un database, con un parametro di callback disponibile per segnalare lo stato della deframmentazione. Questa operazione viene eseguita per limitare la crescita del database utilizzando l'allocazione dei dischi esistente in modo più efficiente all'interno del database. Consente inoltre di ridurre working set assicurando che i dati vengano compressi in modo più accurato. Infine, può migliorare le prestazioni dell'applicazione velocizzando le operazioni comuni tramite una migliore organizzazione dei dati.

**Windows XP:**  **JetDefragment2** è stato introdotto in Windows XP.

**JetDefragment2** contiene anche un parametro della funzione di callback che viene usato per segnalare lo stato di avanzamento del processo di deframmentazione.

La deframmentazione del database è un'operazione online e non interrompe le normali attività del database, ad esempio le operazioni di query o gli aggiornamenti dei dati. **JetDefragment2** non esegue inoltre una copia di tutti i dati esistenti. Al contrario, deframmenta un database sul posto. Infine, **JetDefragment2** ripristina lo spazio interno del database per riutilizzarlo, ma non rilascia spazio in eccesso al sistema operativo file System.

Il formato risultante dei dati può essere molto più efficiente, ma in genere non è ottimale. La deframmentazione è limitata a rilasciare le pagine del database per riutilizzarle che contengono dati che sono già stati eliminati logicamente. La deframmentazione rende inoltre disponibili le pagine del database da riutilizzare in alcuni casi combinando i dati di due pagine quando possono essere inseriti in una singola pagina.

Questa operazione è diversa da [JetCompact](./jetcompact-function.md) , che rende una copia di un database di sola lettura in un formato altamente ottimale.

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*dbid*

Database da deframmentare.

*szTableName*

Parametro non utilizzato. La deframmentazione viene eseguita per l'intero database descritto dall'ID del database specificato.

*pcPasses*

Quando si avvia un'attività di deframmentazione in linea, questo parametro di input facoltativo imposta il numero massimo di passaggi di deframmentazione. Quando si arresta un'attività di deframmentazione in linea, questo buffer di output facoltativo viene impostato sul numero di passaggi eseguiti.

Quando questo parametro è impostato su NULL, il numero di sessioni di deframmentazione in linea è illimitato.

*pcSeconds*

Quando si avvia un'attività di deframmentazione in linea, questo parametro di input facoltativo imposta il tempo massimo per la deframmentazione. Quando si arresta un'attività di deframmentazione in linea, questo buffer di output facoltativo viene impostato sul periodo di tempo utilizzato per la deframmentazione.

Quando questo parametro è impostato su NULL o se *pcSeconds* punta a un valore negativo, il tempo massimo per la deframmentazione è illimitato.

*callback*

Funzione di callback che la deframmentazione chiama regolarmente per segnalare lo stato di avanzamento.

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
<td><p>Questa opzione consente di deframmentare la porzione di spazio disponibile nell'allocazione dello spazio del database ESE. Lo spazio del database è suddiviso in due tipi, spazio di proprietà e spazio disponibile. Lo spazio di proprietà viene allocato a una tabella o a un indice, mentre lo spazio disponibile è pronto per l'utilizzo rispettivamente nella tabella o nell'indice. Lo spazio disponibile è molto più dinamico nel comportamento e richiede la deframmentazione in linea in modo più che spazio di proprietà o dati di tabella o di indice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Questa opzione viene usata per avviare una nuova attività di deframmentazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Questa opzione viene utilizzata per arrestare un'attività di deframmentazione avviata esistente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBTree</p></td>
<td><p>Questa opzione viene utilizzata per deframmentare un albero B.</p></td>
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

La deframmentazione in linea viene controllata sia dall'impostazione di un parametro sia da questa API. Il valore predefinito del parametro di sistema è JET_OnlineDefragAll, ovvero la deframmentazione è abilitata per tutte le strutture di dati supportate. Tuttavia, utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md), è possibile disabilitare la deframmentazione in linea o abilitarla selettivamente solo per gli alberi dello spazio del database, solo per i database, solo per i file di flusso o una combinazione di queste opzioni. Se l'impostazione di sistema per la deframmentazione in linea è di un'impostazione obsoleta, **JetDefragment2** considererà l'impostazione come JET_OnlineDefragAll.

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
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
<td><p>Implementato come <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
