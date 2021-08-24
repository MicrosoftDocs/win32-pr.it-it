---
description: Altre informazioni sulla funzione JetUpdate
title: Funzione JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e02550fb40987906e21d588263daed9dc68aa5d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478247"
---
# <a name="jetupdate-function"></a>Funzione JetUpdate


_**Si applica a:** Windows | Windows Server_

## <a name="jetupdate-function"></a>Funzione JetUpdate

La **funzione JetUpdate** esegue un'operazione di aggiornamento che include l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente. L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete](./jetdelete-function.md).

**JetUpdate** è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando [JetPrepareUpdate](./jetprepareupdate-function.md) e quindi chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o più volte per impostare lo stato del record. Infine, **jetUpdate viene** chiamato per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo da **JetUpdate** o [JetUpdate2](./jetupdate2-function.md)e non durante [JetSetColumn](./jetsetcolumn-function.md) [o JetSetColumns](./jetsetcolumns-function.md).

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pvBookmark*

Puntatore a un segnalibro restituito per una riga inserita.

*cbBookmark*

Dimensioni del buffer a cui punta *pvBookmark*.

*pcbActual*

Dimensioni restituite del segnalibro per la riga inserita restituita in *pvBookmark.*

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Il buffer specificato per il segnalibro di record non è sufficientemente grande da archiviare il segnalibro del record.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Uguale a JET_errNullInvalid.</p> | 
| <p>JET_errDiskFull</p> | <p>L'operazione di aggiornamento richiede l'aumento del numero di file di database o l'allocazione dei file di log, ma l'unità disco in cui si trova il file di database o la serie di log è piena. In alternativa, il file di database si trova in un volume formattato FAT32 e il file di database è già di 4 GByte, il limite per ogni file per FAT32.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Il parametro <em>prep specificato</em> nella <a href="gg269339(v=exchg.10).md">funzione JetPrepareUpdate</a> non è un flag valido.</p> | 
| <p>JET_errKeyDuplicate</p> | <p>Una chiave di indice per questo record è un duplicato di un'altra chiave di indice per un altro record già presente nella tabella e l'indice non consente duplicati.</p> | 
| <p>JET_errKeyTruncated</p> | <p>Il record inserito o aggiornato ha uno o più indici per i quali la chiave generata avrebbe superato le dimensioni massime consentite. Di conseguenza, l'operazione non è riuscita a impedire il troncamento della chiave.</p> | 
| <p>JET_errMultiValuedIndexViolation</p> | <p>Il record inserito o aggiornato ha una colonna a più valori indicizzata con due o più valori identici all'interno della dimensione massima della chiave di lunghezza impostata per l'indice. Di conseguenza, il record ha due voci identiche nell'indice che non sono valide.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNullInvalid</p> | <p>Una o più colonne del record da inserire o nello stato aggiornato di un record da sostituire sono <strong>NULL</strong> che viola il vincolo definito per tali colonne.</p> | 
| <p>JET_errNullKeyDisallowed</p> | <p>Uno o più indici sono definiti per non consentire una chiave <strong>NULL</strong> e lo stato inserito o aggiornato di un record sostituito viola questo vincolo definito.</p> | 
| <p>JET_errRecordPrimaryChanged</p> | <p>Un'operazione di sostituzione dei record ha aggiornato la chiave primaria. Gli aggiornamenti alle colonne chiave primaria devono essere evasi eliminando il record esistente e inserendo un nuovo record con i dati desiderati.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Non è valido tentare un aggiornamento all'interno dell'ambito di una transazione di sola lettura. Una transazione di sola lettura è una transazione avviata tramite una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate è</a> stato chiamato con JET_prepCancel ma il cursore non era nello stato preparato.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>L'operazione non è riuscita perché la memoria disponibile non è sufficiente per mantenere le informazioni transazionali sull'aggiornamento.</p> | 
| <p>JET_errWriteConflict</p> | <p>Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento. L'aggiornamento tentato da questa sessione avrà esito negativo.</p> | 



In caso di esito positivo, l'operazione di aggiornamento aperta sul cursore viene completata. Se per la tabella è definita una colonna con incremento automatico, questo valore viene impostato per i record inseriti. Se per la tabella è definita una colonna di versione, il relativo valore viene inizializzato per i record appena inseriti o incrementato ogni volta che un record viene sostituito. Tutti gli indici, inclusi gli indici cluster e non cluster, vengono aggiornati.

In caso di errore, non vengono apportate modifiche di alcun tipo al database. Prima di inserire e prima di sostituire le funzioni di callback potrebbero essere state chiamate, ma dopo i callback insert e after replace non saranno stati chiamati, perché quest'ultimo non può causare l'esito negativo di un aggiornamento. Il buffer di copia del cursore viene lasciato nello stato preparato, in modo che esista la possibilità di correggere in modo incrementale i problemi che hanno causato errori e ripetere l'operazione di aggiornamento.

#### <a name="remarks"></a>Commenti

Le funzioni di callback possono essere registrate per essere chiamate prima o dopo l'inserimento e prima o dopo l'aggiornamento.

Le limitazioni relative alle dimensioni dei record vengono applicate [da JetSetColumn](./jetsetcolumn-function.md)e non in generale da **JetUpdate**.

È importante comprendere l'impatto dell'esecuzione di un numero elevato di operazioni di aggiornamento all'interno di una singola transazione. Ogni aggiornamento del database deve essere monitorato dal motore di database nell'archivio delle versioni. L'archivio versioni contiene un record attivo di tutte le diverse versioni di ogni record o voce di indice nel database che può essere vista da tutte le transazioni attive. Queste versioni vengono usate per supportare il controllo della concorrenza con più versioni in uso dal motore di database per supportare le transazioni che usano l'isolamento dello snapshot. Dopo che il motore di database ha esaurito le risorse usate per archiviare queste versioni, non può più accettare altre modifiche fino a quando alcune transazioni non sono state conclusa per consentire il recupero di queste risorse. Quando il motore è in questo stato, tutti gli aggiornamenti avranno esito negativo JET_errVersionStoreOutOfMemory. Le risorse disponibili per il motore di database per archiviare queste versioni possono essere controllate tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md) con JET_paramMaxVerPages [e](./resource-parameters.md) [JET_paramGlobalMinVerPages](./resource-parameters.md).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
