---
description: 'Altre informazioni su: funzione JetGetSecondaryIndexBookmark'
title: JetGetSecondaryIndexBookmark (funzione)
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
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313098"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark (funzione)

La funzione **JetGetSecondaryIndexBookmark** recupera un segnalibro speciale per la voce di indice secondaria in corrispondenza della posizione corrente di un cursore. Questo segnalibro può quindi essere utilizzato per riposizionare in modo efficiente il cursore sulla stessa voce di indice utilizzando [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md). Questa operazione è particolarmente utile quando si riposiziona in un indice secondario che contiene chiavi duplicate o che contiene più voci di indice per lo stesso record.

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

*TableID*

Cursore da utilizzare per questa chiamata.

*pvSecondaryKey*

Buffer di output che riceve la chiave secondaria.

*cbSecondaryKeyMax*

Dimensione massima, in byte, del buffer di output per la chiave secondaria.

*pcbSecondaryKeyActual*

Riceve le dimensioni effettive, in byte, della chiave secondaria.

Se questo parametro è NULL, le dimensioni effettive della chiave secondaria non verranno restituite.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive della chiave secondaria. Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.

*pvPrimaryBookmark*

Buffer di output che riceve il segnalibro della chiave primaria.

*cbPrimaryBookmarkMax*

Dimensione massima, in byte, del buffer di output per il segnalibro della chiave primaria.

*pcbPrimaryKeyActual*

Riceve le dimensioni effettive, in byte, del segnalibro della chiave primaria.

Se questo parametro è NULL, non verranno restituite le dimensioni effettive del segnalibro della chiave primaria.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive del segnalibro della chiave primaria. Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>L'operazione è stata completata correttamente, ma uno dei buffer di output era troppo piccolo per ricevere i dati richiesti.</p>
<p>Il buffer di output è stato riempito con la maggior parte del segnalibro. Anche le dimensioni effettive del segnalibro sono state restituite, se richiesto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Il cursore non si trova attualmente in un indice secondario.</p>
<p>Non è significativo recuperare un segnalibro di indice secondario quando il cursore non sta attualmente usando un indice secondario. <a href="gg269221(v=exchg.10).md">JetGetBookmark</a> deve essere utilizzato quando il cursore non si trova in un indice secondario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non è posizionato in corrispondenza di un record.</p>
<p>I motivi possono essere diversi. Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il segnalibro dell'indice secondario per la voce di indice in corrispondenza della posizione corrente di un cursore verrà restituito nei buffer di output. Non si verificherà alcuna modifica allo stato del database.

In caso di errore, lo stato dei buffer di output e le dimensioni effettive del segnalibro dell'indice secondario saranno indefiniti a meno che non venga restituito JET_errBufferTooSmall. Nel caso in cui venga restituito JET_errBufferTooSmall, i buffer di output conterranno la maggior parte del segnalibro dell'indice secondario che rientrerà nello spazio fornito e le dimensioni effettive del segnalibro dell'indice secondario saranno accurate. In ogni caso, non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

In genere i segnalibri devono essere trattati come blocchi opachi di dati. Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati. Tuttavia, le proprietà seguenti possono essere note su tutti i segnalibri ESENT:

  - Un segnalibro identifica in modo univoco un record in una tabella specificata.

  - Il segnalibro di un record non viene modificato per la durata di tale record.

  - Il segnalibro di un record corrisponde alla chiave di tale record nell'indice primario della tabella che contiene il record. Se non viene definito alcun indice primario su tale tabella, il motore di database creerà il proprio segnalibro per il record.

  - I segnalibri possono essere confrontati tra loro usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire il relativo ordinamento nell'indice primario sulla tabella dei record di origine. Se non viene definito alcun indice primario su tale tabella, l'ordine relativo dei segnalibri da tale tabella non è significativo.

  - Non è significativo confrontare i segnalibri dei record di tabelle diverse tra loro.

  - Un segnalibro è sempre minore o uguale a JET_cbBookmarkMost (256) byte di lunghezza prima di Windows Vista. In Windows Vista e versioni successive, i segnalibri possono essere più grandi. La dimensione massima di un segnalibro è uguale al valore corrente di JET_paramKeyMost + 1.

Generalmente, le chiavi devono essere considerate come blocchi opachi di dati. Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati. Tuttavia, le proprietà seguenti possono essere note su tutte le chiavi di ESENT:

  - Le chiavi possono essere confrontate tra loro utilizzando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire l'ordine relativo nell'indice di origine sulla tabella delle voci dell'indice di origine.

  - Non è significativo confrontare le chiavi di voci di indice da indici diversi tra loro.

  - Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte di lunghezza prima di Windows Vista. In Windows Vista e versioni successive, le chiavi possono essere più grandi. La dimensione massima di una chiave è uguale al valore corrente di JET_paramKeyMost.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
