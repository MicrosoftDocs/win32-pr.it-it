---
description: Altre informazioni sulla funzione JetCommitTransaction
title: Funzione JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9592c9b596a7794cc130b7ed599b7c8562ff8b2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477627"
---
# <a name="jetcommittransaction-function"></a>Funzione JetCommitTransaction


_**Si applica a:** Windows | Windows Server_

## <a name="jetcommittransaction-function"></a>Funzione JetCommitTransaction

La **funzione JetCommitTransaction** esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente e le esegue la migrazione al punto di salvataggio precedente. Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio allo stato del database e la sessione chiuderà la transazione.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>Il commit della transazione viene eseguito normalmente, ma questa API non attende che la transazione venga scaricata nel file di log delle transazioni prima di tornare al chiamante. In questo modo si riduce drasticamente la durata di un'operazione di commit a s costo della durabilità. Qualsiasi transazione che non viene scaricata nel log prima di un arresto anomalo del sistema verrà interrotta automaticamente durante il recupero dall'arresto anomalo del sistema durante la chiamata successiva <a href="gg294068(v=exchg.10).md">a JetInit.</a></p><p>Se JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, questa opzione viene ignorata.</p><p>Se questa chiamata a <strong>JetCommitTransaction</strong> non corrisponde alla prima chiamata a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> per questa sessione, questa opzione viene ignorata. Ciò è dovuto al fatto che l'azione finale che si verifica nel punto di salvataggio più esterno è il fattore determinante per determinare se viene effettivamente eseguito il commit su disco dell'intera transazione.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Tutte le transazioni di cui in precedenza è stato eseguito il commit da qualsiasi sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante.</p><p>Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</p><p>Questa opzione non può essere usata in combinazione con altre opzioni.</p><p>Questa opzione è disponibile solo a Windows Server 2003.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Se in precedenza la sessione ha eseguito il commit di transazioni e non sono ancora state scaricate nel file di log delle transazioni, devono essere scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante. Ciò è utile se in precedenza l'applicazione ha eseguito il commit di più transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.</p><p>Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</p><p>Questa opzione non può essere usata in combinazione con altre opzioni.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una delle opzioni richieste non è valida o non è implementata. Questo errore verrà restituito da <strong>JetCommitTransaction</strong> quando:</p><ul><li><p>È stato <em>specificato un grbit</em> non valido.</p></li><li><p>JET_bitWaitLastLevel0Commit è stato specificato in combinazione con un <em>altro grbit</em>.</p></li><li><p>JET_bitWaitAllLevel0Commit è stato specificato in combinazione con un <em>altro grbit</em>.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNotInTransaction</p> | <p>L'operazione non è riuscita perché la sessione specificata non è in una transazione.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, verrà eseguito il commit di tutte le modifiche apportate al database durante il punto di salvataggio corrente per la sessione specificata e tale punto di salvataggio verrà terminato. Se l'ultimo punto di salvataggio per la sessione è stato terminato, la transazione verrà facoltativamente scaricata nel file di log delle transazioni e la sessione chiuderà la transazione.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database. L'applicazione deve chiamare [JetRollback per](./jetrollback-function.md) interrompere la transazione.

#### <a name="remarks"></a>Commenti

Deve essere presente una chiamata a **JetCommitTransaction** o [JetRollback](./jetrollback-function.md) in modo che corrisponda a ogni chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) per una determinata sessione.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
