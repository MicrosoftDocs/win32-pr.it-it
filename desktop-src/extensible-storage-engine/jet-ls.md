---
description: 'Altre informazioni su: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 38ddb306ee6fdcbd1eb792b2c29ca367adc0f4b88cc25dfcbdde22c2638258d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765040"
---
# <a name="jet_ls"></a>JET_LS


_**Si applica a:** Windows | Windows Server_

## <a name="jet_ls"></a>JET_LS

Il **JET_LS** di dati contiene un handle di contesto per l'archiviazione locale(LS). Questo handle può essere associato a un cursore o a una tabella e può fare riferimento a risorse allocate dinamicamente.

**Windows XP: JET_LS** è stato introdotto in Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Tipi di dati

JET_LS

Il valore JET_LSNil indica un handle di contesto non valido.

### <a name="remarks"></a>Commenti

Un handle di contesto viene inizialmente associato al **tipo JET_LS** dati, usando [JetSetLS](./jetsetls-function.md). L'handle di contesto può essere recuperato dal **tipo JET_LS** dati, usando [JetGetLS](./jetgetls-function.md).

L'handle di contesto può essere dissociato in modo esplicito dal tipo di dati JET_LS [tramite JetGetLS](./jetgetls-function.md) con JET_bitLSReset.  In alternativa, l'handle di contesto può essere dissociato in modo implicito dal tipo di dati JET_LS quando l'oggetto sottostante viene rilasciato dal motore di database **come** risultato di un'azione diretta o indiretta da parte dell'applicazione. Nel caso implicito, viene eseguito un callback di runtime per l'applicazione in modo che possa pulire l'handle di contesto. Per altre informazioni sulla dissociazione implicita dal tipo JET_LS dati, vedere [JetSetLS](./jetsetls-function.md). 

I flag seguenti sono associati al tipo JET_LS dati.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Termine</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>L'handle di contesto viene dissociato dall'oggetto .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSCursor</p></td>
<td><p>Impostare o recuperare l'archiviazione locale associata a un cursore di tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Impostare o recuperare l'archiviazione locale associata a una tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_LSNil</p></td>
<td><p>L'handle di contesto non è valido.</p></td>
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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
