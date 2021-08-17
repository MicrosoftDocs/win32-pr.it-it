---
description: 'Altre informazioni su: Funzione JetGetInstanceMiscInfo'
title: Funzione JetGetInstanceMiscInfo
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ada8dfcd69a4e1933bcb60756d1b812f3b358cd37a3cda914819d2a9f6f4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472351"
---
# <a name="jetgetinstancemiscinfo-function"></a>Funzione JetGetInstanceMiscInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetinstancemiscinfo-function"></a>Funzione JetGetInstanceMiscInfo

La **funzione JetGetInstanceMiscInfo** recupera informazioni sull'istanza, mentre l'istanza è online.

**Windows Vista: JetGetInstanceMiscInfo** è stato introdotto in Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Identifica l'istanza di database che verrà usata per la chiamata API.

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo del buffer dipende da *InfoLevel.* Il chiamante è responsabile dell'allineamento appropriato del buffer.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult.*

*InfoLevel*

Determina il tipo di informazioni che verranno recuperate per l'istanza specificata *dall'istanza di*. Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel.*

Le opzioni seguenti sono disponibili per l'uso con questo parametro.

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
<td><p>JET_InstanceMiscInfoLogSignature</p></td>
<td><p><em>pvResult viene</em> interpretato come una <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> della sequenza del log delle transazioni associata a questa istanza.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Buffer troppo piccolo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>È stato specificato <a href="gg294048(v=exchg.10).md">un JET_INSTANCE</a> non valido o <em>un InfoLevel</em> non valido.</p></td>
</tr>
</tbody>
</table>


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
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
