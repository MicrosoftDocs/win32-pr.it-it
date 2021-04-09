---
description: 'Altre informazioni su: funzione JetGotoSecondaryIndexBookmark'
title: JetGotoSecondaryIndexBookmark (funzione)
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967651"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark (funzione)

La funzione **JetGotoSecondaryIndexBookmark** posiziona un cursore in una voce di indice associata al segnalibro dell'indice secondario specificato. Il segnalibro dell'indice secondario deve essere usato con lo stesso indice nella stessa tabella da cui è stato originariamente recuperato. Il segnalibro dell'indice secondario per una voce di indice può essere recuperato usando **JetGotoSecondaryIndexBookmark**.

**Windows XP:**  **JetGotoSecondaryIndexBookmark** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pvSecondaryKey*

Buffer contenente la chiave secondaria da utilizzare per posizionare il cursore.

*cbSecondaryKey*

Dimensione della chiave secondaria nel buffer.

*pvPrimaryBookmark*

Buffer che contiene il segnalibro della chiave primaria da utilizzare per posizionare il cursore.

*cbPrimaryBookmark*

Dimensioni del segnalibro della chiave primaria nel buffer.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

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
<td><p>JET_bitBookmarkPermitVirtualCurrency</p></td>
<td><p>Nel caso in cui non sia più possibile trovare la voce di indice, il cursore viene lasciato posizionato in corrispondenza del punto in cui è stata trovata in precedenza la voce di indice. L'operazione avrà comunque esito negativo con JET_errRecordDeleted; Tuttavia, sarà possibile passare alla voce di indice successiva o precedente relativa alla voce di indice mancante.</p></td>
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
<td><p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Il segnalibro dell'indice secondario specificato non è valido. Questo errore potrebbe essersi verificato perché la chiave secondaria è zero oppure il puntatore del buffer della chiave secondaria è <strong>null</strong>. Questo errore si verifica perché</p>
<ul>
<li><p>L'indice secondario corrente non ha un vincolo di univocità e le dimensioni del segnalibro fornito sono pari a zero.</p></li>
<li><p>Il puntatore del buffer del segnalibro è <strong>null</strong>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Il cursore non si trova attualmente in un indice secondario. Non è significativo passare a un segnalibro di indice secondario quando il cursore non usa attualmente un indice secondario. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> deve essere utilizzato quando il cursore non si trova in un indice secondario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Impossibile trovare la voce di indice associata al segnalibro dell'indice secondario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice associata al segnalibro dell'indice secondario specificato. Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato. Se è stata creata una chiave di ricerca per il cursore da usare, la chiave di ricerca verrà eliminata. Non si verificherà alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la posizione del cursore rimane invariata a meno che non venga restituito JET_errRecordDeleted e JET_bitBookmarkPermitVirtualCurrency venga specificato. In tal caso, il cursore verrà posizionato in corrispondenza del quale sarebbe stata la voce di indice associata al segnalibro dell'indice secondario specificato. Il cursore può essere spostato in relazione a tale posizione, ma non è ancora presente in una voce di indice valida.

Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato. Se è stata creata una chiave di ricerca per il cursore da usare, la chiave di ricerca verrà eliminata. In ogni caso, non si verificherà alcuna modifica allo stato del database.

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
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
