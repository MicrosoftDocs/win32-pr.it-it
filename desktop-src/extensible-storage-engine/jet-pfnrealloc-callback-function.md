---
description: 'Altre informazioni su: funzione JET_PFNREALLOC callback'
title: JET_PFNREALLOC di callback
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 24e4bc43928d6b7ea25294a0163b3b35b1fa04391196e86c54554a785ed2429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616888"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC di callback


_**Si applica a:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC di callback

La JET_PFNREALLOC è un callback compatibile di [rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usato da [JetEnumerateColumns](./jetenumeratecolumns-function.md) per allocare memoria per i buffer di output.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parametri

*pvContext*

Puntatore di contesto assegnato [a JetEnumerateColumns.](./jetenumeratecolumns-function.md) Questo puntatore di contesto può essere usato per trasmettere lo stato dal [chiamante di JetEnumerateColumns](./jetenumeratecolumns-function.md) all'implementazione di questo callback.

*Pv*

Se diverso da NULL, specifica un puntatore a un blocco di memoria allocato in precedenza da questo callback. Se NULL, verrà allocato un nuovo blocco di memoria delle dimensioni richieste.

*Cb*

Nuova dimensione in byte del blocco di memoria. Se questo parametro è 0 (zero) e viene specificato un blocco di memoria, tale blocco di memoria verrà liberato.

### <a name="return-value"></a>Valore restituito

Il sistema può generare codici di esito positivo o negativo in seguito a una chiamata a questa funzione. Per informazioni su come restituire questi codici come HRESULT, vedere Errori del motore Archiviazione [estendibile](./extensible-storage-engine-errors.md).

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
<td><p>Operazione completata</p></td>
<td><p>Se è stato specificato un blocco di memoria allocato in precedenza ed è stata specificata una nuova dimensione pari a zero, tale blocco viene liberato e viene restituito NULL. Se è stato specificato un blocco di memoria allocato in precedenza ed è stata specificata una nuova dimensione diverso da zero, viene restituito il blocco di memoria riallocato. Se non è stato specificato alcun blocco di memoria, viene restituito un blocco di memoria appena allocato delle dimensioni specificate.</p></td>
</tr>
<tr class="even">
<td><p>Operazioni non riuscite</p></td>
<td><p>Verrà restituito NULL. Se è stato fornito un blocco di memoria allocato in precedenza, tale blocco rimarrà allocato.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
