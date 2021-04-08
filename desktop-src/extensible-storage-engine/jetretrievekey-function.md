---
description: 'Altre informazioni su: funzione JetRetrieveKey'
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
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058215"
---
# <a name="jetretrievekey-function"></a>Funzione JetRetrieveKey


_**Si applica a:** Windows | Windows Server_

## <a name="jetretrievekey-function"></a>Funzione JetRetrieveKey

La funzione **JetRetrieveKey** recupera la chiave per la voce di indice in corrispondenza della posizione corrente di un cursore. Tali chiavi vengono costruite mediante chiamate a [JetMakeKey](./jetmakekey-function.md). La chiave recuperata può quindi essere utilizzata per restituire in modo efficiente tale cursore alla stessa voce di indice mediante una chiamata a [JetSeek](./jetseek-function.md).

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

*TableID*

Cursore da utilizzare per questa chiamata.

*pvData*

Buffer di output che riceverà la chiave.

*cbMax*

Dimensione massima in byte del buffer di output.

*pcbActual*

Riceve le dimensioni effettive, in byte, della chiave.

Se questo parametro è NULL, non verrà restituita la dimensione effettiva della chiave.

Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive della chiave. Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Quando viene specificato, il motore restituisce la chiave di ricerca per il cursore. La chiave di ricerca viene compilata utilizzando una o più chiamate precedenti a <a href="gg269329(v=exchg.10).md">JetMakeKey</a> per la ricerca di tale chiave utilizzando <a href="gg294103(v=exchg.10).md">JetSeek</a> o l'impostazione di un intervallo di indici utilizzando <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Nessun tasto di ricerca corrente per il cursore. Questa operazione viene eseguita per <strong>JetRetrieveKey</strong> se viene specificato JET_bitRetrieveCopy e non è stata creata una chiave di ricerca per questo cursore utilizzando una chiamata precedente a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>. La chiave di ricerca verrà eliminata da una chiamata precedente a qualsiasi API di spostamento sul cursore diverso da <a href="gg294117(v=exchg.10).md">JetMove</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non è posizionato in corrispondenza di un record. I motivi possono essere diversi. Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intera chiave. Il buffer di output è stato riempito con la maggior parte della chiave. Sono state restituite anche le dimensioni effettive della chiave, se richieste.</p>
<p><strong>Nota</strong>   Se JET_bitRetrieveCopy è specificato, questo errore non verrà restituito. Per ulteriori informazioni, vedere la sezione Osservazioni.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, la chiave per la voce di indice in corrispondenza della posizione corrente di un cursore verrà restituita nel buffer di output. Se JET_wrnBufferTruncated viene restituito, il buffer di output conterrà la maggior parte della chiave che rientrerà nello spazio specificato e le dimensioni effettive della chiave saranno accurate. Non si verificherà alcuna modifica allo stato del database.

In caso di errore, lo stato del buffer di output e le dimensioni effettive della chiave non saranno definiti. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Generalmente, le chiavi devono essere considerate come blocchi opachi di dati. Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati. Tuttavia, le proprietà seguenti possono essere note su tutte le chiavi di ESENT:

  - Le chiavi possono essere confrontate tra loro tramite la funzione [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) per stabilire il relativo ordinamento nell'indice di origine sulla tabella delle voci dell'indice di origine.

  - Non è significativo confrontare le chiavi di voci di indice da indici diversi tra loro.

  - Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte di lunghezza prima di Windows Vista. In Windows Vista e versioni successive, le chiavi possono essere più grandi. La dimensione massima di una chiave è uguale al valore corrente di JET_paramKeyMost.

Oltre alle proprietà precedenti delle chiavi di ESENT in generale, è importante notare che una chiave di ricerca è diversa dalla chiave per una voce di indice. In particolare, una chiave di ricerca può essere più lunga di una chiave ordinaria. Questa lunghezza aggiuntiva si verifica quando si usa un'opzione con caratteri jolly durante la costruzione della chiave di ricerca. Per ulteriori informazioni, vedere [JetMakeKey](./jetmakekey-function.md) .

In questa API è presente un bug importante presente in tutte le versioni. Se la chiave di ricerca viene richiesta utilizzando l'utilizzo di JET_bitRetrieveCopy e il buffer di output è troppo piccolo per ricevere l'intera chiave, JET_wrnBufferTruncated non verrà restituito. Viene invece restituito JET_errSuccess. È importante verificare che le dimensioni effettive della chiave restituite tramite *pcbActual* siano inferiori o uguali alla dimensione del buffer di output. Se la dimensione effettiva è maggiore della dimensione del buffer di output, il chiamante di **JetRetrieveKey** deve reagire come se fosse stato restituito JET_wrnBufferTruncated.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
