---
description: 'Altre informazioni su: JET_CALLBACK funzione di callback'
title: Funzione di callback JET_CALLBACK
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308517"
---
# <a name="jet_callback-callback-function"></a>Funzione di callback JET_CALLBACK


_**Si applica a:** Windows | Windows Server_

## <a name="jet_callback-callback-function"></a>Funzione di callback JET_CALLBACK

La funzione **JET_CALLBACK** è una funzione di callback multifunzione utilizzata dal motore di database per informare l'applicazione di un evento che interessa la deframmentazione in linea e le notifiche dello stato del cursore.

Vedere [JET_CBTYP](./jet-cbtyp.md) per impostazioni specifiche da usare per i parametri di questa funzione, in quanto queste impostazioni variano in base all'opzione di **JET_CBTYP** selezionata per l'uso nel parametro *CBTYP* .

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione per cui viene eseguito il callback.

*dbid*

Database per il quale viene eseguito il callback.

*TableID*

Cursore per il quale viene eseguito il callback.

*cbtyp*

Punto nell'operazione in cui viene eseguito il callback. Vedere [JET_CBTYP](./jet-cbtyp.md) per un elenco di valori e il significato dei parametri seguenti in ogni caso.

*pvArg1*

Parametro utilizzato per comunicare con l'applicazione utilizzando il callback. Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .

*pvArg2*

Parametro utilizzato per comunicare con l'applicazione utilizzando il callback. Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .

*pvContext*

Parametro utilizzato per comunicare con l'applicazione utilizzando il callback. Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .

*ulUnused*

Parametro utilizzato per comunicare con l'applicazione utilizzando il callback. Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .

#### <a name="return-value"></a>Valore restituito

La funzione restituisce uno dei [codici di errore del motore di archiviazione estendibile](./extensible-storage-engine-error-codes.md). Per informazioni su come restituire questi codici come HRESULT, vedere [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md). In seguito all'esito positivo, l'operazione che ha emesso il callback può procedere normalmente. In alcuni casi, il callback può restituire un avviso che influenza l'operazione. Per informazioni sull'uso di questi avvisi da parte dell'operazione, vedere [JET_CBTYP](./jet-cbtyp.md) .

In caso di errore, l'operazione che ha emesso il callback può procedere normalmente o potrebbe non riuscire. Per informazioni sull'uso del codice di errore da parte dell'operazione, vedere [JET_CBTYP](./jet-cbtyp.md) .

#### <a name="remarks"></a>Commenti

Se il callback passa un cursore all'applicazione, è importante tenere presente che questo cursore è intenzionalmente limitato a un set di funzionalità più piccolo per evitare la ricorsione e altre Brute. Sono consentite le operazioni seguenti:

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCurrentIndex](./jetgetcurrentindex-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordPosition](./jetgetrecordposition-function.md)

  - [JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)

  - [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetRegisterCallback](./jetregistercallback-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUnregisterCallback](./jetunregistercallback-function.md)

Quando si progetta il callback, tenere presente che anche con queste restrizioni, è comunque possibile che il callback abbia esito negativo.

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
