---
description: Altre informazioni sulla funzione JetDefragment2
title: Funzione JetDefragment2
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
ms.openlocfilehash: 08e6cf618be4f3bf7f6eee1b903559db579973c0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984984"
---
# <a name="jetdefragment2-function"></a>Funzione JetDefragment2


_**Si applica a:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>Funzione JetDefragment2

La **funzione JetDefragment2** avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database, con un parametro di callback disponibile per segnalare lo stato di avanzamento della deframmentazione. Questa operazione viene eseguita per limitare l'aumento delle dimensioni del database usando l'allocazione dei dischi esistente in modo più efficiente all'interno del database. Può anche ridurre i working set assicurando che i dati sono più imballati. Infine, può migliorare le prestazioni dell'applicazione accelerando le operazioni comuni tramite una migliore organizzazione dei dati.

**Windows XP:****JetDefragment2** è stato introdotto in Windows XP.  

**JetDefragment2** contiene anche un parametro della funzione di callback usato per segnalare lo stato del processo di deframmentazione.

La deframmentazione del database è un'operazione online e non interrompe la normale attività del database, ad esempio operazioni di query o aggiornamenti dei dati. **JetDefragment2** non crea inoltre una copia di tutti i dati esistenti. Al contrario, deframmenta un database sul posto. Infine, **JetDefragment2** recupera lo spazio interno del database per il nuovo utilizzo, ma non rilascia spazio in eccesso al sistema operativo file system.

Il formato risultante dei dati può essere molto più efficiente, ma non è in genere ottimale. La deframmentazione è limitata al rilascio di pagine di database per il nuovo utilizzo che contengono dati già eliminati logicamente. La deframmentazione rende anche disponibili le pagine di database per il nuovo uso in alcuni casi combinando i dati di due pagine quando possono essere adattati a una singola pagina.

Questa operazione è diversa [da JetCompact,](./jetcompact-function.md) che rende una copia di un database di sola lettura in un formato altamente ottimale.

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

*Dbid*

Database da deframmentare.

*szTableName*

A *volte szTableName* è obbligatorio e talvolta non è consentito:

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Deve essere `NULL`. |
| `JET_bitDefragmentBTree` | Specifica il nome della tabella/BTree da deframmentare. |
| *Altro* | Deve essere `NULL`. |
 
La deframmentazione viene eseguita per l'intero database descritto dall'ID database specificato.

*pcPasses*

Quando si avvia un'attività di deframmentazione online, questo parametro di input facoltativo imposta il numero massimo di passaggi di deframmentazione. Quando si arresta un'attività di deframmentazione online, questo buffer di output facoltativo viene impostato sul numero di passaggi eseguiti.

Quando questo parametro è impostato su NULL, il numero di passaggi di deframmentazione online è illimitato.

*pcSeconds*

Quando si avvia un'attività di deframmentazione online, questo parametro di input facoltativo imposta il tempo massimo per la deframmentazione. Quando si arresta un'attività di deframmentazione online, questo buffer di output facoltativo viene impostato sul periodo di tempo usato per la deframmentazione.

Quando questo parametro è impostato su NULL o *se pcSeconds* punta a un valore negativo, il tempo massimo per la deframmentazione è illimitato.

*callback*

Funzione di callback che la deframmentazione chiama regolarmente per segnalare lo stato di avanzamento.

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Deve essere `NULL`. |
| `JET_bitDefragmentBTree` | Deve essere `NULL`. |
| *Altro* | facoltativo.


*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitDefragmentAvailSpaceTreesOnly</p> | <p>Questa opzione viene usata per deframmentare la parte di spazio disponibile dell'allocazione dello spazio del database ESE. Lo spazio del database è suddiviso in due tipi, lo spazio di proprietà e lo spazio disponibile. Lo spazio di proprietà viene allocato a una tabella o a un indice, mentre lo spazio disponibile è pronto per l'uso rispettivamente all'interno della tabella o dell'indice. Lo spazio disponibile è molto più dinamico nel comportamento e richiede più deframmentazione online rispetto allo spazio di proprietà, alla tabella o ai dati dell'indice.</p> | 
| <p>JET_bitDefragmentBatchStart</p> | <p>Questa opzione viene usata per avviare una nuova attività di deframmentazione.</p> | 
| <p>JET_bitDefragmentBatchStop</p> | <p>Questa opzione viene usata per arrestare un'attività di deframmentazione avviata esistente.</p> | 
| <p>JET_bitDefragmentBTree</p> | <p>Questa opzione viene usata per deframmentare un albero B, specificato da szTableName.</p> | 
| <p>JET_bitDefragmentBTreeBatch</p> | <p>Questa opzione viene usata per chiamare OLD2 sull'intero database.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Il database scelto per la deframmentazione è di sola lettura e non può essere aggiornato in alcun modo, inclusa la deframmentazione.</p> | 
| <p>JET_errDistributedTransactionAlreadyPreparedToCommit</p> | <p>La sessione specificata è nello stato preparato per il commit e non può iniziare nuovi aggiornamenti fino a quando non viene eseguito il commit o il rollback della transazione corrente.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>L'ID database specificato non corrisponde a un database noto nell'istanza di .</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La sessione specificata ha solo privilegi di sola lettura e non può avviare un'attività che può eseguire un aggiornamento, inclusa la deframmentazione.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</p> | 
| <p>JET_wrnDefragAlreadyRunning</p> | <p>L JET_bitDefragmentBatchStart è stata passata, ma un'attività di deframmentazione sta già eseguendo la deframmentazione nel database specificato.</p> | 
| <p>JET_wrnDefragNotRunning</p> | <p>L JET_bitDefragmentBatchStop è stata passata, ma non è attualmente in esecuzione alcuna attività di deframmentazione.</p> | 



In caso di esito positivo, viene eseguita l'azione richiesta di avvio di un'attività di deframmentazione per dati con opzioni specificate oppure viene eseguita l'azione di arresto di un'attività di deframmentazione esistente.

In caso di errore, l'azione richiesta di avvio o arresto di un processo di deframmentazione online non viene eseguita. Non si verificano altri effetti collaterali.

#### <a name="remarks"></a>Commenti

La deframmentazione online è controllata sia da un'impostazione di parametro che da questa API. Il valore predefinito del parametro di sistema JET_OnlineDefragAll, il che significa che la deframmentazione è abilitata per tutte le strutture di dati supportate. Tuttavia, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md), è possibile disabilitare la deframmentazione online o abilitarla in modo selettivo solo per gli alberi dello spazio del database, solo per i database, solo per i file di streaming o per qualsiasi combinazione di queste opzioni. Se l'impostazione di sistema per la deframmentazione in linea è su un'impostazione obsoleta, **JetDefragment2** considera l'impostazione come JET_OnlineDefragAll.

Può essere presente al massimo un'attività in esecuzione per ogni database. L'attività viene eseguita come thread nel processo che ospita ESE.

La sessione utilizzata per avviare l'attività di deframmentazione online può essere usata successivamente per le operazioni di database mentre l'attività di deframmentazione continua, perché l'attività di deframmentazione alloca una propria sessione. La sessione specificata viene usata solo per controllare le autorizzazioni associate alla sessione di avvio dell'attività e non viene effettivamente usata per le operazioni di deframmentazione stesse.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
