---
description: 'Altre informazioni su: Funzione JetDefragment'
title: Funzione JetDefragment
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
ms.openlocfilehash: 2f9fdce5268e6981fa018f58ed14b31c2c078cce
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985947"
---
# <a name="jetdefragment-function"></a>Funzione JetDefragment


_**Si applica a:** Windows | Windows Server_

## <a name="jetdefragment-function"></a>Funzione JetDefragment

La **funzione JetDefragment avvia** e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database. Questa operazione viene eseguita per limitare l'aumento delle dimensioni del database usando l'allocazione dei dischi esistente in modo più efficiente all'interno del database. Può anche ridurre le working set assicurando che i dati sono più imballati. Infine, può migliorare le prestazioni dell'applicazione velocizzando le operazioni comuni tramite una migliore organizzazione dei dati.

La deframmentazione del database è un'operazione online e non interrompe la normale attività del database, ad esempio operazioni di query o aggiornamenti dei dati. **JetDefragment** inoltre non esegue una copia di tutti i dati esistenti. Al contrario, deframmenta un database sul posto. Infine, **JetDefragment recupera** lo spazio interno del database per il nuovo utilizzo, ma non rilascia spazio in eccesso al sistema operativo file system.

Il formato risultante dei dati può essere molto più efficiente, ma in genere non è ottimale. La deframmentazione è limitata al rilascio di pagine di database per il nuovo utilizzo che contengono dati già eliminati logicamente. La deframmentazione rende inoltre disponibili le pagine di database per il nuovo utilizzo in alcuni casi combinando i dati di due pagine quando possono rientrare in una singola pagina.

Questa operazione è diversa [da JetCompact, che](./jetcompact-function.md) rende una copia di un database di sola lettura in un formato estremamente ottimale.

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

*Dbid*

Database che verrà deframmentato.

*szTableName*

Parametro non utilizzato. La deframmentazione viene eseguita per l'intero database descritto dall'ID database specificato.

*pcPasses*

Quando si avvia un'attività di deframmentazione online, questo parametro di input imposta il numero massimo di passaggi di deframmentazione. Quando si arresta un'attività di deframmentazione online, questo buffer di output viene impostato sul numero di passaggi eseguiti.

Quando questo parametro è impostato su NULL, il numero di passaggi di deframmentazione online è illimitato.

*pcSeconds*

Quando si avvia un'attività di deframmentazione online, questo parametro di input imposta il tempo massimo per la deframmentazione. Quando si arresta un'attività di deframmentazione online, questo buffer di output viene impostato sul periodo di tempo utilizzato per la deframmentazione.

Quando questo parametro è impostato su NULL o se *pcSeconds* punta a un valore negativo, il tempo massimo per la deframmentazione è illimitato.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitDefragmentAvailSpaceTreesOnly</p> | <p>Deframmenta la parte di spazio disponibile dell'allocazione dello spazio del database ESE. Lo spazio del database è suddiviso in due tipi: spazio di proprietà e spazio disponibile. Lo spazio di proprietà viene allocato a una tabella o a un indice mentre lo spazio disponibile è pronto per l'uso rispettivamente all'interno della tabella o dell'indice. Lo spazio disponibile è molto più dinamico nel comportamento e richiede la deframmentazione in linea più dello spazio di proprietà o dei dati della tabella o dell'indice.</p> | 
| <p>JET_bitDefragmentBatchStart</p> | <p>Avvia una nuova attività di deframmentazione.</p> | 
| <p>JET_bitDefragmentBatchStop</p> | <p>Arresta un'attività di deframmentazione.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Il database scelto per la deframmentazione è di sola lettura e non può essere aggiornato in alcun modo, inclusa la deframmentazione.</p> | 
| <p>JET_errDistributedTransactionAlreadyPreparedToCommit</p> | <p>La sessione specificata è nello stato pronto per il commit e non può iniziare nuovi aggiornamenti fino a quando non viene eseguito il commit o il rollback della transazione corrente.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>L'ID di database specificato non corrisponde a un database noto nell'istanza.</p> | 
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

La deframmentazione online è controllata sia da un'impostazione di parametro che da questa API. Il valore predefinito del parametro di sistema JET_OnlineDefragAll, il che significa che la deframmentazione è abilitata per tutte le strutture di dati supportate. Tuttavia, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md), è possibile disabilitare la deframmentazione online o abilitarla in modo selettivo solo per gli alberi dello spazio del database, solo per i database, solo per i file di streaming o per qualsiasi combinazione di queste opzioni. Se l'impostazione di sistema per la deframmentazione online è impostata su un'impostazione obsoleta, **JetDefragment** considera l'impostazione come JET_OnlineDefragAll.

Può essere presente al massimo un'attività in esecuzione per ogni database. L'attività viene eseguita come thread nel processo che ospita ESE.

La sessione utilizzata per avviare l'attività di deframmentazione online può essere usata successivamente per le operazioni di database mentre l'attività di deframmentazione continua, perché l'attività di deframmentazione alloca una propria sessione. La sessione specificata viene usata solo per controllare le autorizzazioni associate alla sessione di avvio dell'attività e non viene effettivamente usata per le operazioni di deframmentazione stesse.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDefragmentW</strong> (Unicode) e <strong>JetDefragmentA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment2](./jetdefragment2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
