---
description: Altre informazioni sulla funzione JetUpdate2
title: Funzione JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f85633a16077c3957bebb1e236f5bbca6180778a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479567"
---
# <a name="jetupdate2-function"></a>Funzione JetUpdate2


_**Si applica a:** Windows | Windows Server_

## <a name="jetupdate2-function"></a>Funzione JetUpdate2

La **funzione JetUpdate2** esegue un'operazione di aggiornamento, inclusa l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente. Questa funzione contiene un elenco di *opzioni grbit* che possono essere impostate durante l'esecuzione di un aggiornamento. L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete](./jetdelete-function.md).

**Windows Server 2003: JetUpdate2** è stato introdotto in Windows Server 2003.

**JetUpdate2 è** il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando [JetPrepareUpdate](./jetprepareupdate-function.md) e quindi chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o più volte per impostare lo stato del record. Infine, **viene chiamato JetUpdate2** per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo da [JetUpdate](./jetupdate-function.md) o **JetUpdate2** e non durante [JetSetColumn](./jetsetcolumn-function.md) [o JetSetColumns](./jetsetcolumns-function.md).

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
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

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitUpdateCheckESE97Compatibility</p> | <p>Questo flag fa sì che l'aggiornamento restituirà un errore se l'aggiornamento non sarebbe stato possibile nella versione Windows 2000 di ESE, che ha applicato un numero massimo inferiore di istanze di colonna multivalore in ogni record rispetto alle versioni successive di ESE. Questo è importante solo per le applicazioni che vogliono replicare i dati tra le applicazioni ospitate in Windows 2000 e le applicazioni ospitate in Windows Server 2003 o versioni successive di ESE. Non deve essere necessario per la maggior parte delle applicazioni.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Il buffer specificato per il segnalibro di record non è sufficientemente grande da archiviare il segnalibro del record.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
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
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate è</a> stato chiamato con JET_prepCancel ma il cursore non si trova nello stato preparato.</p> | 
| <p>JET_errWriteConflict</p> | <p>Un'operazione di sostituzione dei record per cui un blocco di scrittura non è già stato allocato può riscontrare un conflitto di scrittura al momento dell'aggiornamento.</p> | 



In caso di esito positivo, l'operazione di aggiornamento aperta sul cursore viene completata. Se per la tabella è definita una colonna con incremento automatico, questo valore viene impostato per i record inseriti. Se per la tabella è definita una colonna di versione, il relativo valore viene inizializzato per i record appena inseriti o incrementato ogni volta che un record viene sostituito. Tutti gli indici, inclusi gli indici cluster e non cluster, vengono aggiornati.

In caso di errore, non vengono apportate modifiche di alcun tipo al database. Prima di inserire e prima di sostituire le funzioni di callback potrebbero essere state chiamate, ma dopo i callback insert e after replace non saranno stati chiamati, perché quest'ultimo non può causare l'esito negativo di un aggiornamento. Il buffer di copia del cursore viene lasciato nello stato preparato, in modo che esista la possibilità di correggere in modo incrementale i problemi che hanno causato errori e ripetere l'operazione di aggiornamento.

#### <a name="remarks"></a>Commenti

Le limitazioni relative alle dimensioni dei record vengono applicate [da JetSetColumn](./jetsetcolumn-function.md)e non in generale da [JetUpdate](./jetupdate-function.md). L'unica eccezione è quando viene JET_bitUpdateCheckESE97Compatibility flag di compatibilità. In questo caso, l'intero record viene controllato perché una singola [operazione JetSetColumn](./jetsetcolumn-function.md) che ha superato il limite può essere compensata da una chiamata successiva a [JetSetColumn](./jetsetcolumn-function.md).

Per altre informazioni, vedere la sezione Osservazioni in [JetUpdate.](./jetupdate-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[Oggetti JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[Oggetti JetSetColumns](./jetsetcolumns-function.md)
