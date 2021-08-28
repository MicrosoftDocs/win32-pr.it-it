---
description: Altre informazioni sulla funzione JetCommitTransaction2
title: Funzione JetCommitTransaction2
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6080380fd8326504e7b1182b439571e3904f0d53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986064"
---
# <a name="jetcommittransaction2-function"></a>Funzione JetCommitTransaction2


_**Si applica a:** Windows | Windows Server_

La **funzione JetCommitTransaction2** esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente ed esegue la migrazione al punto di salvataggio precedente. Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio allo stato del database e la sessione chiuderà la transazione.

La **funzione JetCommitTransaction2** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che specificano zero o più valori elencati nella tabella seguente.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>Il commit della transazione viene eseguito normalmente, ma questa API non attende lo scaricamento della transazione nel file di log delle transazioni prima di tornare al chiamante. In questo modo si riduce drasticamente la durata di un'operazione di commit a costo della durabilità. Qualsiasi transazione non scaricata nel log prima di un arresto anomalo verrà automaticamente interrotta durante il ripristino dell'arresto anomalo durante la chiamata successiva alla <a href="gg294068(v=exchg.10).md">funzione JetInit.</a></p><p>Se JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, questa opzione viene ignorata.</p><p>Se questa chiamata a <strong>JetCommitTransaction2</strong> non corrisponde alla prima chiamata alla <a href="gg294083(v=exchg.10).md">funzione JetBeginTransaction</a> per questa sessione, questa opzione viene ignorata. Ciò è dovuto al fatto che l'azione finale che si verifica nel punto di salvataggio più esterno è il fattore determinante per stabilire se viene effettivamente eseguito il commit su disco dell'intera transazione.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Tutte le transazioni di cui è stato eseguito il commit in precedenza da qualsiasi sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante.</p><p>Questa opzione può essere usata anche se la sessione non è attualmente in una transazione.</p><p>Questa opzione non può essere usata in combinazione con altre opzioni.</p><p>Questa opzione è disponibile nelle versioni del sistema operativo Windows Server a partire da Windows Server 2003.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Se in precedenza la sessione ha eseguito il commit di transazioni e non sono ancora state scaricate nel file di log delle transazioni, devono essere scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante. Ciò è utile se in precedenza l'applicazione ha eseguito il commit di diverse transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.</p><p>Questa opzione può essere usata anche se la sessione non è attualmente in una transazione.</p><p>Questa opzione non può essere usata in combinazione con altre opzioni.</p> | 



*cmsecDurableCommit*

Durata per il commit di una transazione lazy.

*pCommitID*

ID commit associato a questo record di commit.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE (Extensible Archiviazione Engine), vedere [Errori](./extensible-storage-engine-errors.md) del motore di Archiviazione estendibile e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata alla <a href="gg269240(v=exchg.10).md">funzione JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo dalle versioni del Windows operativo a partire da Windows XP.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una delle opzioni richieste non è valida o non è implementata. Questo errore verrà restituito dalla <strong>funzione JetCommitTransaction2</strong> quando si verifica quanto segue:</p><ul><li><p>È stato <em>specificato un grbit</em> non valido.</p></li><li><p>JET_bitWaitLastLevel0Commit è stato specificato in combinazione con un altro <em>grbit</em>.</p></li><li><p>JET_bitWaitAllLevel0Commit è stato specificato in combinazione con un altro <em>grbit</em>.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNotInTransaction</p> | <p>L'operazione non è riuscita perché la sessione specificata non è in una transazione.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo dalle versioni del Windows operativo a partire da Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, verrà eseguito il commit di tutte le modifiche apportate al database durante il punto di salvataggio corrente per la sessione specificata e tale punto di salvataggio verrà terminato. Se l'ultimo punto di salvataggio per la sessione è stato terminato, la transazione verrà facoltativamente scaricata nel file di log delle transazioni e la sessione verrà chiusa.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database. L'applicazione deve chiamare la [funzione JetRollback](./jetrollback-function.md) per interrompere la transazione.

#### <a name="remarks"></a>Commenti

Deve essere presente una chiamata a **JetCommitTransaction2** o [JetRollback](./jetrollback-function.md) in modo che corrisponda a ogni chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) per una determinata sessione.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
