---
description: 'Altre informazioni su: funzione JetGetBookmark'
title: JetGetBookmark (funzione)
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
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131962"
---
# <a name="jetgetbookmark-function"></a>JetGetBookmark (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetbookmark-function"></a>JetGetBookmark (funzione)

La funzione **JetGetBookmark** Recupera il segnalibro per il record associato alla voce di indice in corrispondenza della posizione corrente di un cursore. Questo segnalibro può quindi essere utilizzato per riposizionare il cursore sullo stesso record utilizzando [JetGoToBookmark](./jetgotobookmark-function.md).

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

*TableID*

Cursore da utilizzare per questa chiamata.

*pvBookmark*

Buffer di output che riceve il segnalibro.

*cbMax*

Dimensione massima, in byte, del buffer di output.

*pcbActual*

Dimensioni effettive, in byte, del segnalibro.

Se questo parametro è **null** , le dimensioni effettive del segnalibro non verranno restituite.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive del segnalibro. Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.

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
<td><p>L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intero segnalibro. Il buffer di output è stato riempito con la maggior parte del segnalibro. Anche le dimensioni effettive del segnalibro sono state restituite, se richiesto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:  </strong> Questi valori restituiti sono introdotti in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non è posizionato in corrispondenza di un record. I motivi possono essere diversi. Questa situazione si verifica, ad esempio, se il cursore è posizionato dopo l'ultimo record nell'indice corrente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, nel buffer di output verrà restituito il segnalibro per il record associato alla voce di indice in corrispondenza della posizione corrente di un cursore. Non si verificherà alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, lo stato del buffer di output e le dimensioni effettive del segnalibro saranno indefiniti a meno che non venga restituito JET_errBufferTooSmall. Nel caso in cui venga restituito JET_errBufferTooSmall, il buffer di output conterrà la maggior parte del segnalibro che rientrerà nello spazio fornito e le dimensioni effettive del segnalibro saranno accurate. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

In genere i segnalibri devono essere trattati come blocchi opachi di dati. Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati. Tuttavia, le condizioni seguenti sono vere per tutti i segnalibri ESENT:

  - Un segnalibro identifica in modo univoco un record in una tabella specificata.

  - Il segnalibro di un record non viene modificato per la durata di tale record.

  - Il segnalibro di un record corrisponde alla chiave di tale record nell'indice primario della tabella che contiene il record. Se nella tabella non è definito alcun indice primario, il motore di database creerà il proprio segnalibro per il record.

  - I segnalibri possono essere confrontati tra loro tramite la funzione [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire il relativo ordinamento nell'indice primario sulla tabella dei record di origine. Se non viene definito alcun indice primario su tale tabella, non è significativo utilizzare l'ordinamento relativo dei segnalibri della tabella.

  - Non è significativo confrontare i segnalibri dei record di tabelle diverse tra loro.

  - Un segnalibro è sempre minore o uguale a JET_cbBookmarkMost (256) byte di lunghezza, prima di Windows Vista.
    
**Windows Vista:** In Windows Vista e versioni successive, i segnalibri possono essere più grandi di JET_cbBookmarkMost (256) byte. La dimensione massima di un segnalibro è uguale al valore corrente di JET_paramKeyMost + 1.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
