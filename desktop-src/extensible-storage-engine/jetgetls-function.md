---
description: 'Altre informazioni su: funzione JetGetLS'
title: JetGetLS (funzione)
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318092"
---
# <a name="jetgetls-function"></a>JetGetLS (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetls-function"></a>JetGetLS (funzione)

La funzione **JetGetLS** consente all'applicazione di recuperare l'handle di contesto noto come archiviazione locale associato a un cursore o alla tabella associata a tale cursore. Questo handle di contesto deve essere stato impostato in precedenza utilizzando [JetSetLS](./jetsetls-function.md). **JetGetLS** può essere utilizzato anche per recuperare contemporaneamente l'handle del contesto corrente per un cursore o una tabella e reimpostare tale handle di contesto.

**Windows XP: JetGetLS** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pls*

Buffer di output che riceve l'handle di contesto attualmente associato al cursore o alla tabella.

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
<td><p>JET_bitLSCursor</p></td>
<td><p>Indica che è necessario recuperare l'handle di contesto associato al cursore specificato.</p>
<p>Se non viene specificato né JET_bitLSCursor né JET_bitLSTable, JET_bitLSCursor si presume.</p>
<p>Questa opzione non può essere utilizzata con JET_bitLSTable. L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Indica che è necessario recuperare l'handle di contesto associato alla tabella che contiene il cursore specificato. Non è consentito usare questa opzione con JET_bitLSCursor. L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Indica che l'handle del contesto per l'oggetto scelto deve essere reimpostato su JET_LSNil. Il valore corrente dell'handle di contesto viene restituito nel buffer di output.</p></td>
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
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una delle opzioni richieste non è valida, è stata usata in modo non valido o non è stata implementata.</p>
<p>Questo problema può verificarsi per <strong>JetGetLS</strong> quando vengono impostati sia JET_bitLSCursor che JET_bitLSTable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>Non è stato possibile restituire l'handle del contesto perché all'oggetto richiesto non è attualmente associato alcun handle di contesto.</p>
<p><strong>Nota  </strong> Questo errore non viene restituito se JET_bitLSReset è specificato ma non è stato associato alcun handle di contesto all'oggetto richiesto.</p></td>
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
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, l'handle di contesto è stato recuperato dall'oggetto richiesto. Se JET_bitLSReset è stato specificato, anche tale handle di contesto è stato rimosso correttamente dall'oggetto. Non si verificherà alcuna modifica allo stato del database.

In caso di errore, non sono state apportate modifiche allo stato dell'oggetto richiesto. Non si verificherà alcuna modifica allo stato del database.

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
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
