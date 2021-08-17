---
description: 'Altre informazioni su: Funzione JetGetLS'
title: Funzione JetGetLS
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
ms.openlocfilehash: 3a359bb2899a2dea604e236a7118c914e795bffba7ca675229e28ad3a7f25dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979061"
---
# <a name="jetgetls-function"></a>Funzione JetGetLS


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetls-function"></a>Funzione JetGetLS

La **funzione JetGetLS** consente all'applicazione di recuperare l'handle di contesto noto come Archiviazione locale associato a un cursore o alla tabella associata a tale cursore. Questo handle di contesto deve essere stato impostato in precedenza [tramite JetSetLS.](./jetsetls-function.md) **È anche possibile usare JetGetLS** per recuperare contemporaneamente l'handle di contesto corrente per un cursore o una tabella e reimpostare tale handle di contesto.

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

*tableid*

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
<td><p>Indica che l'handle di contesto associato al cursore specificato deve essere recuperato.</p>
<p>Se non JET_bitLSCursor né JET_bitLSTable specificato, JET_bitLSCursor si presuppone.</p>
<p>Questa opzione non può essere usata con JET_bitLSTable. L'operazione avrà esito negativo JET_errInvalidgrbit se viene tentata.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Indica che deve essere recuperato l'handle di contesto associato alla tabella che contiene il cursore specificato. Non è valido usare questa opzione con JET_bitLSCursor. L'operazione avrà esito negativo JET_errInvalidgrbit se viene tentata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Indica che l'handle di contesto per l'oggetto scelto deve essere reimpostato JET_LSNil. Il valore corrente dell'handle di contesto viene restituito nel buffer di output.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Errori del motore Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).

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
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una delle opzioni richieste non era valida, usata in modo non valido o non implementata.</p>
<p>Questo problema può verificarsi <strong>per JetGetLS</strong> quando JET_bitLSCursor e JET_bitLSTable sono impostate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>Impossibile restituire l'handle di contesto perché nessun handle di contesto è attualmente associato all'oggetto richiesto.</p>
<p><strong>Nota:  </strong> Questo errore non viene restituito se JET_bitLSReset specificato ma non è stato associato alcun handle di contesto all'oggetto richiesto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, l'handle di contesto è stato recuperato correttamente dall'oggetto richiesto. Se JET_bitLSReset stato specificato, anche l'handle di contesto è stato rimosso correttamente dall'oggetto . Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, non è stata apportata alcuna modifica allo stato dell'oggetto richiesto. Non verrà apportata alcuna modifica allo stato del database.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
