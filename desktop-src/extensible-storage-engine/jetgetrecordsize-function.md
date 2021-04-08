---
description: 'Altre informazioni su: funzione JetGetRecordSize'
title: JetGetRecordSize (funzione)
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 255ca71f3b57c0d1f1bc8440a9a6d4697c09c670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968048"
---
# <a name="jetgetrecordsize-function"></a>JetGetRecordSize (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetrecordsize-function"></a>JetGetRecordSize (funzione)

La funzione **JetGetRecordSize** recupera le informazioni sulle dimensioni dei record dal percorso desiderato.

**Windows Vista: JetGetRecordSize** è stato introdotto in Windows Vista.

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Identifica il contesto della sessione di database che verrà usato per la chiamata API.

*TableID*

Identifica la tabella o il cursore che verrà usato per la chiamata API. Il cursore deve essere posizionato su un record o avere preparato un aggiornamento.

*precsize*

Puntatore a un buffer di output per la struttura [JET_RECSIZE](./jet-recsize-structure.md) .

*grbit*

Si tratta di uno o più dei valori seguenti.

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
<td><p>JET_bitRecordSizeInCopyBuffer</p></td>
<td><p>Questo consente di recuperare le dimensioni del record che si trova nel buffer di copia preparato per l'aggiornamento. In caso contrario, il <em>TableID</em> o il cursore deve essere posizionato su un record e tale record verrà usato.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordSizeRunningTotal</p></td>
<td><p>Quando si specifica questo bit, il <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> non viene azzerato prima di compilare il contenuto, agendo efficacemente come un accumulo di statistiche per più record visitati o aggiornati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRecordSizeLocal</p></td>
<td><p>In questo modo, l'API ignorerà i valori Long non intrinseci. Ad esempio, verrà usato solo il record locale nella pagina.</p></td>
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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Una delle opzioni richieste non è valida o non è stata implementata. Questo errore verrà restituito dalla funzione <strong>JetGetRecordSize</strong> quando viene specificato un <em>grbit</em> non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  JET_errInstanceUnavailable verranno restituiti solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è consentito usare la stessa sessione da più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  JET_errInstanceUnavailable verranno restituiti solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Questo problema può verificarsi se il cursore è stato posizionato in modo errato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Se il cursore non è posizionato in una transazione, questo può verificarsi se un altro thread Elimina il record da questa sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Può essere restituito se è stato passato un<em>Precsize</em> <strong>null</strong>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

La dimensione della chiave accumulata nel campo **cbOverhead** di [JET_RECSIZE](./jet-recsize-structure.md), è interessata dall'JET_bitRecordSizeInCopyBuffer. Se viene specificato questo bit, le dimensioni della chiave accumulate nel campo **cbOverhead** sono le dimensioni della chiave completa. Se questo bit non viene usato, le dimensioni della chiave accumulate non includeranno alcuna dimensione salvata a causa della compressione del prefisso di chiave.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008.</p></td>
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
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
