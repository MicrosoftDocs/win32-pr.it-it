---
description: 'Altre informazioni: Funzione JetRetrieveKey'
title: Funzione JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65925ce2425dcf717b7db94f5b83ca48a68c8f31
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466221"
---
# <a name="jetretrievekey-function"></a>Funzione JetRetrieveKey


_**Si applica a:** Windows | Windows Server_

## <a name="jetretrievekey-function"></a>Funzione JetRetrieveKey

La **funzione JetRetrieveKey** recupera la chiave per la voce di indice nella posizione corrente di un cursore. Tali chiavi vengono costruite tramite chiamate [a JetMakeKey](./jetmakekey-function.md). La chiave recuperata può quindi essere usata per restituire in modo efficiente il cursore alla stessa voce di indice tramite una chiamata a [JetSeek](./jetseek-function.md).

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pvData*

Buffer di output che riceverà la chiave.

*cbMax*

Dimensione massima in byte del buffer di output.

*pcbActual*

Riceve le dimensioni effettive in byte della chiave.

Se questo parametro è NULL, le dimensioni effettive della chiave non verranno restituite.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive della chiave. Questo significa che questo numero sarà maggiore delle dimensioni del buffer di output.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Se specificato, il motore restituirà la chiave di ricerca per il cursore. La chiave di ricerca viene creata usando una o più chiamate precedenti a <a href="gg269329(v=exchg.10).md">JetMakeKey</a> allo scopo di cercare tale chiave usando <a href="gg294103(v=exchg.10).md">JetSeek</a> o impostando un intervallo di indici tramite <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Non esiste alcuna chiave di ricerca corrente per il cursore. Questa operazione si verifica <strong>per JetRetrieveKey</strong> se JET_bitRetrieveCopy specificato e non è stata costruita una chiave di ricerca per questo cursore usando una chiamata precedente a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>. La chiave di ricerca verrà eliminata da una chiamata precedente a qualsiasi API di navigazione sul cursore diverso <a href="gg294117(v=exchg.10).md">da JetMove</a>.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è posizionato su un record. I motivi possono essere diversi. Ad esempio, ciò si verifica se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intera chiave. Il buffer di output è stato riempito con la maggior parte della chiave adatta. Se richiesto, sono state restituite anche le dimensioni effettive della chiave.</p><p><strong>Nota:</strong>   Questo errore non verrà restituito se JET_bitRetrieveCopy specificato. Per altre informazioni, vedere la sezione Osservazioni.</p> | 



In caso di esito positivo, la chiave per la voce di indice nella posizione corrente di un cursore verrà restituita nel buffer di output. Se JET_wrnBufferTruncated restituito, il buffer di output conterrà la maggior parte della chiave che si adatterà allo spazio fornito e le dimensioni effettive della chiave saranno accurate. Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, lo stato del buffer di output e le dimensioni effettive della chiave non saranno definiti. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Le chiavi devono in genere essere considerate come blocchi di dati opachi. Non è consigliabile tentare di sfruttare la struttura interna di questi dati. Tuttavia, le proprietà seguenti possono essere note su tutte le chiavi ESENT:

  - Le chiavi possono essere confrontate tra loro usando la funzione [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) per stabilire il relativo ordinamento nell'indice di origine sulla tabella delle voci dell'indice di origine.

  - Non è importante confrontare le chiavi delle voci di indice di indici diversi tra loro.

  - Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte di lunghezza prima di Windows Vista. In Windows Vista e versioni successive, le chiavi possono essere più grandi. La dimensione massima di una chiave è uguale al valore corrente di JET_paramKeyMost.

Oltre alle proprietà precedenti delle chiavi ESENT in generale, è importante notare che una chiave di ricerca è diversa dalla chiave per una voce di indice. In particolare, una chiave di ricerca può essere più lunga di una chiave normale. Questa lunghezza aggiuntiva si verifica quando si usa un'opzione con caratteri jolly durante la costruzione della chiave di ricerca. Per [altre informazioni, vedere JetMakeKey.](./jetmakekey-function.md)

In questa API è presente un bug importante in tutte le versioni. Se la chiave di ricerca viene richiesta usando JET_bitRetrieveCopy e il buffer di output è troppo piccolo per ricevere l'intera chiave, JET_wrnBufferTruncated non verrà restituito. JET_errSuccess verrà restituito . È importante verificare che le dimensioni effettive della chiave restituita tramite *pcbActual* siano minori o uguali alle dimensioni del buffer di output. Se le dimensioni effettive sono maggiori delle dimensioni del buffer di output, il chiamante di **JetRetrieveKey** deve reagire come se JET_wrnBufferTruncated restituito.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
