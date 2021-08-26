---
description: Altre informazioni sulla funzione JetBeginTransaction2
title: Funzione JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c228f7ac0c1b796cc3c6c489e9e83766ada5d716
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466358"
---
# <a name="jetbegintransaction2-function"></a>Funzione JetBeginTransaction2


_**Si applica a:** Windows | Windows Server_

## <a name="jetbegintransaction2-function"></a>Funzione JetBeginTransaction2

La **funzione JetBeginTransaction2** determina l'immissione di una transazione in una sessione e la creazione di un nuovo punto di salvataggio. Questa funzione può essere chiamata più volte in una singola sessione per creare punti di salvataggio aggiuntivi. Questi punti di salvataggio possono essere usati per mantenere o rimuovere in modo selettivo le modifiche al database.

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>La transazione non modificherà il database. Se si tenta di eseguire un aggiornamento, l'operazione avrà esito negativo JET_errTransReadOnly. Questa opzione viene ignorata a meno che non venga richiesta quando la sessione specificata non è già in una transazione. Questa opzione è disponibile solo a Windows XP.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Non è possibile avviare una nuova transazione perché la sessione è già alla profondità massima del punto di salvataggio consentita dal motore di database.</p> | 



In caso di esito positivo, la sessione specificata si trova all'interno di una transazione. Se la sessione era in precedenza all'interno di una transazione, verrà creato un nuovo punto di salvataggio.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Per altre informazioni sul funzionamento delle transazioni, vedere [JetBeginTransaction](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
