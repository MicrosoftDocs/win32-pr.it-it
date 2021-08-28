---
description: Altre informazioni sulla funzione JetGetLock
title: Funzione JetGetLock
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51509f4027d4748f32b8c9dfb8756433b5f93935
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984834"
---
# <a name="jetgetlock-function"></a>Funzione JetGetLock


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetlock-function"></a>Funzione JetGetLock

La **funzione JetGetLock** consente di riservare in modo esplicito la possibilità di aggiornare una riga, di scrivere un blocco o di impedire in modo esplicito che una riga venga aggiornata da qualsiasi altra sessione, blocco di lettura. In genere, i blocchi di scrittura delle righe vengono acquisiti in modo implicito in seguito all'aggiornamento delle righe. I blocchi di lettura non sono in genere necessari a causa del controllo delle versioni dei record. In alcuni casi, tuttavia, una transazione può voler bloccare in modo esplicito una riga per imporre la serializzazione o garantire che un'operazione successiva abbia esito positivo, in quanto i blocchi necessari sono già stati evasi.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione che verrà usata per questa chiamata.

*tableid*

Cursore che verrà usato per questa chiamata.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più dei valori seguenti:


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitReadLock</p> | <p>Questo flag determina l'acquisizione di un blocco di lettura nel record corrente. I blocchi di lettura non sono compatibili con i blocchi di scrittura già mantenuti da altre sessioni, ma sono compatibili con i blocchi di lettura mantenuti da altre sessioni.</p> | 
| <p>JET_bitWriteLock</p> | <p>Questo flag determina l'acquisizione di un blocco di scrittura nel record corrente. I blocchi di scrittura non sono compatibili con i blocchi di scrittura o lettura mantenuti da altre sessioni, ma sono compatibili con i blocchi di lettura mantenuti dalla stessa sessione.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Il <em>grbit specificato</em> non è né JET_bitReadLock né JET_bitWriteLock. Deve essere uno di questi due flag.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Per acquisire un blocco, il cursore deve essere posizionato su un record. I blocchi sono sempre sui record.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNotInTransaction</p> | <p>I blocchi possono essere acquisiti solo dalle sessioni in una transazione.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Il cursore non può essere di sola lettura e acquisire un blocco di scrittura.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La sessione deve disporre delle autorizzazioni di scrittura per acquisire il blocco di scrittura.</p> | 
| <p>JET_errWriteConflict</p> | <p>Errore restituito quando viene richiesto un blocco in conflitto.</p> | 



In caso di esito positivo, la sessione ha acquisito il blocco richiesto.

In caso di errore, la sessione non ha acquisito il blocco richiesto.

#### <a name="remarks"></a>Commenti

I blocchi di scrittura non possono essere acquisiti con sessioni o cursori con autorizzazioni di sola lettura, anche se la sessione e il cursore non eseguono un'operazione di aggiornamento. Sia la sessione che il cursore devono avere privilegi di scrittura per acquisire un blocco di scrittura.

I blocchi di lettura e scrittura sono un mezzo di blocco pessimistico. Il blocco pessimistico prevede che più sessioni simultanee siano in conflitto e acquisiscono i blocchi in anticipo per garantire che le operazioni riescano.

La maggior parte delle operazioni sarà serializzabile in base ai blocchi presi in modo implicito. Tuttavia, alcune operazioni non verranno eseguite. Per illustrare questo problema, considerare le due transazioni,

T1: R(A), U(B)

T2: R(B), U(A)

Il controllo delle versioni a livello di record garantisce che ogni transazione eseguita contemporaneamente veda i valori originali per A e B. Non esiste un ordine di esecuzione seriale che possa produrre gli stessi risultati per A e B nel caso in cui i risultati dipendono dai dati letti. Per rendere serializzabile questa transazione, l'applicazione deve acquisire un blocco di lettura esplicito su A e B in ogni transazione quando viene letto il valore.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
