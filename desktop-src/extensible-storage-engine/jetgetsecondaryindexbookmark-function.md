---
description: Altre informazioni sulla funzione JetGetSecondaryIndexBookmark
title: Funzione JetGetSecondaryIndexBookmark
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a27d34b2622c5fe4ce2c72e3781394457e9cc20
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472523"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>Funzione JetGetSecondaryIndexBookmark


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetsecondaryindexbookmark-function"></a>Funzione JetGetSecondaryIndexBookmark

La **funzione JetGetSecondaryIndexBookmark** recupera un segnalibro speciale per la voce di indice secondaria nella posizione corrente di un cursore. Questo segnalibro può quindi essere usato per riposizionare in modo efficiente il cursore sulla stessa voce di indice usando [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md). Ciò è particolarmente utile quando si riposiziona in un indice secondario che contiene chiavi duplicate o che contiene più voci di indice per lo stesso record.

**Windows XP: JetGetSecondaryIndexBookmark** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pvSecondaryKey*

Buffer di output che riceve la chiave secondaria.

*cbSecondaryKeyMax*

Dimensione massima, in byte, del buffer di output per la chiave secondaria.

*pcbSecondaryKeyActual*

Riceve le dimensioni effettive in byte della chiave secondaria.

Se questo parametro è NULL, le dimensioni effettive della chiave secondaria non verranno restituite.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive della chiave secondaria. Questo significa che questo numero sarà maggiore delle dimensioni del buffer di output.

*pvPrimaryBookmark*

Buffer di output che riceve il segnalibro della chiave primaria.

*cbPrimaryBookmarkMax*

Dimensione massima, in byte, del buffer di output per il segnalibro della chiave primaria.

*pcbPrimaryKeyActual*

Riceve le dimensioni effettive, in byte, del segnalibro della chiave primaria.

Se questo parametro è NULL, le dimensioni effettive del segnalibro della chiave primaria non verranno restituite.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive del segnalibro di chiave primaria. Questo significa che questo numero sarà maggiore delle dimensioni del buffer di output.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L'operazione è stata completata correttamente, ma uno dei buffer di output era troppo piccolo per ricevere i dati richiesti.</p><p>Il buffer di output è stato riempito con la quantità di segnalibro adatta. Se richiesto, sono state restituite anche le dimensioni effettive del segnalibro.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Il cursore non si trova attualmente in un indice secondario.</p><p>Non è significativo recuperare un segnalibro di indice secondario quando il cursore non usa attualmente un indice secondario. <a href="gg269221(v=exchg.10).md">JetGetBookmark</a> deve essere usato quando il cursore non si trova in un indice secondario.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è posizionato su un record.</p><p>I motivi possono essere diversi. Ad esempio, ciò si verifica se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, il segnalibro dell'indice secondario per la voce di indice nella posizione corrente di un cursore verrà restituito nei buffer di output. Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, lo stato dei buffer di output e le dimensioni effettive del segnalibro dell'indice secondario non saranno definiti a meno JET_errBufferTooSmall restituito. Nel caso in cui JET_errBufferTooSmall restituito, i buffer di output conterranno la maggior parte del segnalibro dell'indice secondario che si adatterà allo spazio fornito e le dimensioni effettive del segnalibro dell'indice secondario saranno accurate. In ogni caso, non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

I segnalibri devono in genere essere considerati blocchi di dati opachi. Non è consigliabile tentare di sfruttare la struttura interna di questi dati. Tuttavia, le proprietà seguenti possono essere note su tutti i segnalibri ESENT:

  - Un segnalibro identifica in modo univoco un record in una determinata tabella.

  - Il segnalibro di un record non cambierà per la durata del record.

  - Il segnalibro di un record corrisponde alla chiave del record nell'indice primario sulla tabella contenente tale record. Se su tale tabella non è definito alcun indice primario, il motore di database creerà il proprio segnalibro per il record.

  - I segnalibri possono essere confrontati tra loro usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire l'ordinamento relativo nell'indice primario sulla tabella dei record di origine. Se non viene definito alcun indice primario su tale tabella, l'ordinamento relativo dei segnalibri da tale tabella non è significativo.

  - Non è importante confrontare tra loro segnalibri di record di tabelle diverse.

  - Un segnalibro è sempre minore o uguale a JET_cbBookmarkMost (256) byte di lunghezza prima di Windows Vista. In Windows Vista e versioni successive, i segnalibri possono essere più grandi. La dimensione massima di un segnalibro è uguale al valore corrente di JET_paramKeyMost + 1.

Le chiavi devono in genere essere considerate come blocchi di dati opachi. Non è consigliabile tentare di sfruttare la struttura interna di questi dati. Tuttavia, le proprietà seguenti possono essere note su tutte le chiavi ESENT:

  - Le chiavi possono essere confrontate tra loro usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire il relativo ordinamento nell'indice di origine sulla tabella delle voci dell'indice di origine.

  - Non è importante confrontare le chiavi delle voci di indice di indici diversi tra loro.

  - Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte di lunghezza prima di Windows Vista. In Windows Vista e versioni successive, le chiavi possono essere più grandi. Le dimensioni massime di una chiave sono uguali al valore corrente di JET_paramKeyMost.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
