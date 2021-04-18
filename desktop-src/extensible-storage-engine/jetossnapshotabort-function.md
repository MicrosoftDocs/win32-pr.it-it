---
description: 'Altre informazioni su: funzione JetOSSnapshotAbort'
title: JetOSSnapshotAbort (funzione)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315618"
---
# <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort (funzione)

La funzione **JetOSSnapshotAbort** notifica al motore che può riprendere le normali operazioni di i/o dopo un periodo di blocco terminato con uno snapshot non riuscito.

**Windows server 2003:**  **JetOSSnapshotAbort** è stato introdotto in Windows Server 2003.

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*grbit*

Opzioni per questa chiamata. Questo parametro è riservato per utilizzi futuri e l'unico valore valido supportato è 0 (zero).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>La sessione dello snapshot non è valida o il parametro grbit non è valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Identificatore per la sessione snapshot non valido.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, la sessione snapshot verrà terminata e verrà ripreso il normale comportamento del motore. Una nuova sessione snapshot può essere avviata in un secondo momento.

Se questa funzione ha esito negativo, la sessione snapshot non verrà interrotta.

#### <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata invece di [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) per informare il motore che lo snapshot è stato interrotto per i motivi che non sono correlati al motore. Queste informazioni possono essere usate in un secondo momento per consentire l'emissione di messaggi del registro eventi sulla sessione snapshot o per determinare altre azioni appropriate.

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
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
