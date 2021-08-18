---
description: Altre informazioni sulla funzione JetGotoBookmark
title: Funzione JetGotoBookmark
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 56e94339a49cc80e8b7b416e89efc5c85079981e0430f325e29f1dd711eef63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979000"
---
# <a name="jetgotobookmark-function"></a>Funzione JetGotoBookmark


_**Si applica a:** Windows | Windows Server_

## <a name="jetgotobookmark-function"></a>Funzione JetGotoBookmark

La **funzione JetGotoBookmark** posiziona un cursore su una voce di indice per il record associato al segnalibro specificato. Il segnalibro può essere usato con qualsiasi indice definito in una tabella. Il segnalibro per un record può essere recuperato usando [JetGetBookmark.](./jetgetbookmark-function.md)

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pvBookmark*

Buffer contenente il segnalibro da utilizzare per posizionare il cursore.

*cbBookmark*

Dimensione del segnalibro nel buffer.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>L'operazione non può essere completata perché tutte le attività nell'istanza associata alla sessione sono scadute in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>L'operazione non può essere completata perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p>
<p><strong>Windows XP:</strong>   Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Il segnalibro specificato non è valido. Ciò potrebbe verificarsi perché la dimensione del segnalibro è zero o il puntatore del buffer del segnalibro è <strong>NULL.</strong></p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore si trova in un indice secondario e non è stata trovata alcuna voce di indice per il record associato al segnalibro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata ancora inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Impossibile trovare il record associato al segnalibro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La stessa sessione non può essere usata per più thread contemporaneamente.</p>
<p><strong>Windows XP:</strong>   Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice per il record associato al segnalibro specificato. Se un record è stato preparato per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo di indici verrà annullato. Se è stata costruita una chiave di ricerca per il cursore, tale chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la posizione del cursore rimarrà invariata. Se un record è stato preparato per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo di indici verrà annullato. Se è stata costruita una chiave di ricerca per il cursore, tale chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Esistono due modi per usare un segnalibro per posizionare un cursore su un indice. Il primo è usare il segnalibro per posizionarsi direttamente sul record. Ciò si verifica quando l'indice corrente del cursore è l'indice primario. Questa tecnica funziona perché un segnalibro ESENT corrisponde alla chiave primaria del record associato.

Il secondo modo per usare un segnalibro è posizionarlo su una voce in un indice secondario che corrisponde al record associato a tale segnalibro. Durante questo processo, il motore cerca il record effettivo usando il segnalibro nell'indice primario. Usa quindi i dati del record e la definizione dell'indice secondario per calcolare una chiave nell'indice secondario che punta al record. Posiziona quindi il cursore sulla voce di indice per la chiave. Se il cursore si trova attualmente in un indice secondario su una o più colonne chiave multivalore, il cursore verrà posizionato sulla voce di indice corrispondente al primo multivalore di ognuna di queste colonne chiave.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
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
[JetGetBookmark](./jetgetbookmark-function.md)
