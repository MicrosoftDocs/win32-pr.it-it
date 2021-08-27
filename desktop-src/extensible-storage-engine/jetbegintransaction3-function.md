---
description: Altre informazioni sulla funzione JetBeginTransaction3
title: Funzione JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7c963da40f72fb7ea54c5614836a1de81a0b3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479237"
---
# <a name="jetbegintransaction3-function"></a>Funzione JetBeginTransaction3


_**Si applica a:** Windows | Windows Server_

La **funzione JetBeginTransaction3** determina l'immissione di una transazione in una sessione e la creazione di un nuovo punto di salvataggio. Questa funzione può essere chiamata più volte in una singola sessione per creare punti di salvataggio aggiuntivi. Questi punti di salvataggio possono essere usati per mantenere o annullare le modifiche al database in modo selettivo.

La **funzione JetBeginTransaction3** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*trxid*

Identificatore facoltativo fornito dall'utente per identificare la transazione.

*grbit*

Gruppo di bit che specifica zero o più valori dell'opzione di chiamata elencati nella tabella seguente.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>La transazione non modificherà il database. Se si tenta di eseguire un aggiornamento, l'operazione avrà esito negativo con JET_errTransReadOnly di risposta. Questa opzione viene ignorata a meno che non venga richiesta quando la sessione specificata non è già in una transazione. Questa opzione è disponibile nelle versioni del Windows operativo a partire da Windows XP.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE [(Extensible](./extensible-storage-engine-errors.md) Archiviazione Engine), vedere Extensible Archiviazione Engine Errors and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata alla <a href="gg269240(v=exchg.10).md">funzione JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo codice restituito viene restituito dalle versioni di Windows a partire da Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore viene restituito dalle versioni di Windows a partire da Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Non è possibile avviare una nuova transazione perché la sessione è già alla profondità massima del punto di salvataggio consentita dal motore di database.</p> | 



In caso di esito positivo, la sessione specificata si trova all'interno di una transazione. Se in precedenza la sessione era all'interno di una transazione, verrà creato un nuovo punto di salvataggio.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Per altre informazioni sul funzionamento delle transazioni, vedere [JetBeginTransaction.](./jetbegintransaction-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

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
