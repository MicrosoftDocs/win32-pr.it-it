---
description: 'Altre informazioni su: Funzione JetDelete'
title: Funzione JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 039ddcb0610b6a958e9c45be7e3a898631d2a0fc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984954"
---
# <a name="jetdelete-function"></a>Funzione JetDelete


_**Si applica a:** Windows | Windows Server_

## <a name="jetdelete-function"></a>Funzione JetDelete

La **funzione JetDelete** elimina il record corrente in una tabella di database.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database che verrà usato per la chiamata API.

*tableid*

Cursore su una tabella di database. La riga corrente verrà eliminata.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errCallbackFailed</p> | <p>La funzione di callback non è riuscita in qualche modo. Ad esempio, le violazioni di accesso nelle funzioni di callback vengono intercettte e convertite in JET_errCallbackFailed. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errIllegalOperation</p> | <p>Il cursore specificato da <em>tableid</em> non supporta l'eliminazione. Vedere la sezione relativa alle osservazioni.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore specificato <em>da tableid</em> non si trova in un record.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Il motore di database non dispone di autorizzazioni sufficienti per eliminare il record. Questo problema può verificarsi se il file di database è stato aperto con accesso in sola lettura.</p> | 
| <p>JET_errRollbackError</p> | <p>Esiste un buffer di aggiornamento (vedere <a href="gg269339(v=exchg.10).md">JetPrepareUpdate),</a>ma non è possibile eseguire il rollback di tutte le modifiche apportate alle colonne di tipo JET_coltypLongText e/o colonne di tipo JET_coltypLongBinary.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Non è valido usare la stessa sessione da più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transazione è di sola lettura e non supporta le eliminazioni.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>L'operazione non è riuscita perché la memoria disponibile non è sufficiente per mantenere le informazioni transazionali sull'aggiornamento.</p> | 
| <p>JET_errWriteConflict</p> | <p>Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento. L'aggiornamento tentato da questa sessione avrà esito negativo.</p> | 



In caso di esito positivo, la valuta viene lasciata poco prima del record successivo. Se il record eliminato è l'ultimo nella tabella, la valuta viene lasciata alla fine della tabella, ovvero dopo il nuovo ultimo record. Se il record eliminato è l'unico record nella tabella, la valuta viene impostata sull'inizio.

Gli indici appropriati vengono aggiornati automaticamente.

Se viene preparato un aggiornamento [(tramite JetPrepareUpdate),](./jetprepareupdate-function.md)verrà annullato. Il buffer di aggiornamento verrà reimpostato.

In caso di errore, la valuta rimane invariata. Se viene preparato un aggiornamento (vedere [JetPrepareUpdate),](./jetprepareupdate-function.md)è possibile reimpostare il buffer di aggiornamento.

#### <a name="remarks"></a>Commenti

Non tutte le tabelle supportano l'eliminazione di righe. Una tabella temporanea in genere non supporta l'eliminazione di righe. L'eliminazione di record può essere abilitata nelle tabelle temporanee per molti motivi, alcuni dei quali sono:

  - JET_bitTTUpdatable è stato specificato durante la creazione.

  - Le tabelle temporanee di grandi dimensioni possono supportare l'eliminazione se sono state create con JET_bitTTScrollable o JET_bitTTIndexed. La soglia alla quale una tabella temporanea diventa "grande" è attualmente di 64 kilobyte, ma potrebbe essere modificata nelle versioni future.

Windows XP e versioni successive. Le funzioni di callback possono essere richiamate **da JetDelete,** JET_cbtypBeforeDelete e JET_cbtypAfterDelete.

È importante comprendere l'impatto dell'esecuzione di un numero elevato di operazioni di aggiornamento all'interno di una singola transazione. Ogni aggiornamento del database deve essere monitorato dal motore di database nell'archivio delle versioni. L'archivio versioni contiene un record attivo di tutte le diverse versioni di ogni record o voce di indice nel database che può essere visualizzato da tutte le transazioni attive. Queste versioni vengono usate per supportare il controllo della concorrenza con più versioni in uso dal motore di database per supportare le transazioni che usano l'isolamento dello snapshot. Dopo che il motore di database ha esaurito le risorse usate per archiviare queste versioni, non può più accettare altre modifiche fino a quando alcune transazioni non sono state conclusa per consentire il recupero di queste risorse. Quando il motore è in questo stato, tutti gli aggiornamenti avranno esito negativo JET_errVersionStoreOutOfMemory. Le risorse disponibili per il motore di database per archiviare queste versioni possono essere controllate tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md) con JET_paramMaxVerPages *e* *JET_paramGlobalMinVerPages*.

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
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
