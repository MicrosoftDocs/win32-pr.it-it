---
description: 'Altre informazioni su: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878606"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columnid"></a>JET_COLUMNID

Il tipo di dati **JET_COLUMNID** identifica una colonna all'interno di una tabella.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Tipi di dati

JET_COLUMNID

Identifica una colonna all'interno di una tabella.

### <a name="remarks"></a>Commenti

Gli ID di colonna sono univoci all'interno di una singola tabella. Una volta che una colonna dispone di un ID di colonna specifico, avrà sempre l'ID della colonna. Il ripristino da backup non comporterà la modifica del valore di un ID di colonna. Tuttavia, se una o più colonne della tabella, precedenti a una colonna della tabella specifica, vengono eliminate, un database compatto può modificare il valore di un ID di colonna.

In alcuni casi, gli ID di colonna costituiscono l'unico mezzo per identificare le colonne. Quando viene creata una tabella temporanea, le relative colonne non hanno nomi, ma una matrice di ID di colonna viene restituita dalla funzione create.

Le colonne in tabelle diverse possono avere lo stesso ID di colonna.

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
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>

