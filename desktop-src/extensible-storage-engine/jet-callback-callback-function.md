---
description: 'Altre informazioni su: JET_CALLBACK callback'
title: JET_CALLBACK funzione di callback
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
ms.openlocfilehash: 8a49c63a948cd25abe97dfc58e10a97720eae248
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986164"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK funzione di callback


_**Si applica a:** Windows | Windows Server_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK funzione di callback

La **JET_CALLBACK** è una funzione di callback multivalore usata dal motore di database per informare l'applicazione di un evento che interessa la deframmentazione online e le notifiche sullo stato del cursore.

Vedere [JET_CBTYP](./jet-cbtyp.md) impostazioni specifiche da usare per i parametri di questa funzione, in quanto queste impostazioni differiranno **a** seconda dell'opzione JET_CBTYP selezionata per l'uso nel *parametro cbtyp.*

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

*Dbid*

Database per il quale viene eseguito il callback.

*tableid*

Cursore per cui viene eseguito il callback.

*cbtyp*

Punto dell'operazione in cui viene eseguito il callback. Vedere [JET_CBTYP](./jet-cbtyp.md) per un elenco di valori e il significato dei parametri seguenti in ogni caso.

*pvArg1*

Parametro utilizzato per comunicare con l'applicazione usando il callback . Vedere [JET_CBTYP](./jet-cbtyp.md) per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database.

*pvArg2*

Parametro utilizzato per comunicare con l'applicazione usando il callback . Vedere [JET_CBTYP](./jet-cbtyp.md) per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database.

*pvContext*

Parametro utilizzato per comunicare con l'applicazione usando il callback . Vedere [JET_CBTYP](./jet-cbtyp.md) per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database.

*ulUnused*

Parametro utilizzato per comunicare con l'applicazione usando il callback . Vedere [JET_CBTYP](./jet-cbtyp.md) per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database.

#### <a name="return-value"></a>Valore restituito

La funzione restituisce uno dei codici di errore [extensible Archiviazione Engine](./extensible-storage-engine-error-codes.md). Per informazioni su come restituire questi codici come HRESULT, vedere Errori del motore Archiviazione [estendibile](./extensible-storage-engine-errors.md). In caso di esito positivo, l'operazione che ha eseguito il callback può procedere normalmente. In alcuni casi, il callback può restituire un avviso che influisce su tale operazione. Vedere [JET_CBTYP](./jet-cbtyp.md) per informazioni sull'uso di questi avvisi da parte dell'operazione.

In caso di errore, l'operazione che ha eseguito il callback può continuare normalmente o potrebbe non riuscire. Vedere [JET_CBTYP](./jet-cbtyp.md) per informazioni sull'uso del codice di errore da parte dell'operazione.

#### <a name="remarks"></a>Commenti

Se il callback passa un cursore all'applicazione, è importante sapere che questo cursore è intenzionalmente limitato a un set più piccolo di funzionalità per evitare ricorsione e altre bruttezza. Sono consentite le operazioni seguenti:

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

Quando si progetta il callback, prendere in considerazione che, anche con queste restrizioni, è comunque possibile che il callback non riesca.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
