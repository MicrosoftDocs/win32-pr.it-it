---
description: Altre informazioni sulla funzione JetGetBookmark
title: Funzione JetGetBookmark
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7806770d528d83f18d6f3eb061dc3043e15a0e53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984844"
---
# <a name="jetgetbookmark-function"></a>Funzione JetGetBookmark


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetbookmark-function"></a>Funzione JetGetBookmark

La **funzione JetGetBookmark** recupera il segnalibro per il record associato alla voce di indice nella posizione corrente di un cursore. Questo segnalibro può quindi essere usato per riposizionare il cursore sullo stesso record [usando JetGoToBookmark](./jetgotobookmark-function.md).

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pvBookmark*

Buffer di output che riceve il segnalibro.

*cbMax*

Dimensione massima, in byte, del buffer di output.

*pcbActual*

Dimensioni effettive, in byte, del segnalibro.

Se questo parametro è **NULL,** le dimensioni effettive del segnalibro non verranno restituite.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive del segnalibro. Questo significa che questo numero sarà maggiore della dimensione del buffer di output.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L'operazione è stata completata correttamente, ma il buffer di output è troppo piccolo per ricevere l'intero segnalibro. Il buffer di output è stato riempito con la maggior parte del segnalibro che sarebbe possibile inserire. Se richiesto, sono state restituite anche le dimensioni effettive del segnalibro.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>L'operazione non può essere completata perché tutte le attività nell'istanza associata alla sessione sono scadute in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>L'operazione non può essere completata perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong> Questi valori restituiti sono stati introdotti in Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è posizionato su un record. I motivi possono essere diversi. Ad esempio, ciò si verifica se il cursore viene posizionato dopo l'ultimo record nell'indice corrente.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong> Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, il segnalibro per il record associato alla voce di indice nella posizione corrente di un cursore verrà restituito nel buffer di output. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, lo stato del buffer di output e le dimensioni effettive del segnalibro non saranno definiti, a meno JET_errBufferTooSmall non sia stato restituito . Nel caso in cui JET_errBufferTooSmall restituito, il buffer di output conterrà la maggior parte del segnalibro che si adatterà allo spazio fornito e le dimensioni effettive del segnalibro saranno accurate. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

I segnalibri devono in genere essere considerati come blocchi di dati opachi. Non è consigliabile tentare di sfruttare la struttura interna di questi dati. Tuttavia, le condizioni seguenti sono vere per tutti i segnalibri ESENT:

  - Un segnalibro identifica in modo univoco un record in una determinata tabella.

  - Il segnalibro di un record non cambierà per la durata di tale record.

  - Il segnalibro di un record corrisponde alla chiave del record nell'indice primario sulla tabella contenente tale record. Se non viene definito alcun indice primario su tale tabella, il motore di database creerà il proprio segnalibro per il record.

  - I segnalibri possono essere confrontati tra loro usando la funzione [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire il relativo ordinamento nell'indice primario sulla tabella dei record di origine. Se sulla tabella non è definito alcun indice primario, non è significativo usare l'ordinamento relativo dei segnalibri della tabella.

  - È inutile confrontare i segnalibri di record di tabelle diverse.

  - Un segnalibro è sempre minore o uguale JET_cbBookmarkMost (256) byte, prima di Windows Vista.
    
**Windows Vista:** In Windows Vista e versioni successive, i segnalibri possono essere più grandi di JET_cbBookmarkMost (256) byte. La dimensione massima di un segnalibro è uguale al valore corrente di JET_paramKeyMost + 1.

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
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
