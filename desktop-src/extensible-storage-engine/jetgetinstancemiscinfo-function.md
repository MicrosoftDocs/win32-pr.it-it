---
description: 'Altre informazioni su: funzione JetGetInstanceMiscInfo'
title: JetGetInstanceMiscInfo (funzione)
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
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057924"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo (funzione)

La funzione **JetGetInstanceMiscInfo** recupera informazioni sull'istanza di, mentre l'istanza è online.

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

*istanza*

Identifica l'istanza del database che verrà usata per la chiamata API.

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo di buffer dipende da *InfoLevel*. Il chiamante è responsabile dell'allineamento appropriato del buffer.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult*.

*InfoLevel*

Determina il tipo di informazioni che verranno recuperate per l'istanza di specificata dall' *istanza*. Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*.

Con questo parametro è possibile usare le opzioni seguenti.

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
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> della sequenza del log delle transazioni associata a questa istanza.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Il buffer è troppo piccolo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>È stato specificato un <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> non valido o un <em>InfoLevel</em> non valido.</p></td>
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
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
