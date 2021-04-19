---
description: 'Altre informazioni su: funzione JetDupCursor'
title: Funzione JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317346"
---
# <a name="jetdupcursor-function"></a>Funzione JetDupCursor


_**Si applica a:** Windows | Windows Server_

## <a name="jetdupcursor-function"></a>Funzione JetDupCursor

La funzione **JetDupCursor** duplica un cursore aperto e restituisce un handle al cursore duplicato. Se il cursore duplicato era un cursore di sola lettura, il cursore duplicato è anche un cursore di sola lettura. Qualsiasi stato correlato alla costruzione di una chiave di ricerca o all'aggiornamento di un record non viene copiato nel cursore duplicato. Inoltre, la posizione del cursore originale non viene duplicata nel cursore duplicato. Il cursore duplicato viene sempre aperto nell'indice cluster e il relativo percorso è sempre nella prima riga della tabella.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pTableID*

Puntatore a *TableID*.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Non esistono risorse di cursore disponibili.</p></td>
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


In seguito all'esito positivo, *pTableID* è impostato su un cursore duplicato.

In caso di errore, non viene apportata alcuna modifica. Lo stato di *TableID* è invariato.

#### <a name="remarks"></a>Commenti

Per il cursore duplicato non è stato copiato l'intero stato del cursore. La posizione del cursore duplicato, incluso l'indice corrente, è in genere diversa dal cursore specificato. Il cursore duplicato viene sempre restituito nell'indice cluster e nella prima riga della tabella. Se la tabella è vuota, il cursore duplicato non si trova in nessuna riga.

Le tabelle aperte con **JetDupCursor** devono essere in genere chiuse con [JetCloseTable](./jetclosetable-function.md). L'eccezione a questa regola si verifica quando **JetDupCursor** viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback](./jetrollback-function.md)). Quando si esegue il rollback di una transazione, il cursore viene chiuso automaticamente. In questo caso, è un errore chiudere la tabella con [JetCloseTable](./jetclosetable-function.md).

Il numero di tabelle che è possibile aprire contemporaneamente è interessato direttamente da [JET_paramMaxOpenTables](./resource-parameters.md). Per informazioni dettagliate, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md) .

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

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
