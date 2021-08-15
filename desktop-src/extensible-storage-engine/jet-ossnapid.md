---
description: 'Altre informazioni su: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: 2dac261072ac9a5ce5a845ff046628cf348cd5815c34e16fccb575c2c0da3095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765077"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

Il **JET_OSSNAPID** di dati contiene un handle per uno snapshot del database.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Tipi di dati

JET_OSSNAPID

Handle per uno snapshot del database. Questo handle viene usato negli elementi dell'API JET coinvolti nel backup dello snapshot.

**È** possibile usare NULL per indicare un handle non valido.

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

