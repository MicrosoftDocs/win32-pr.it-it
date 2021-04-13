---
description: 'Altre informazioni su: struttura JET_ENUMCOLUMNID'
title: Struttura JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526083"
---
# <a name="jet_enumcolumnid-structure"></a>Struttura JET_ENUMCOLUMNID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_enumcolumnid-structure"></a>Struttura JET_ENUMCOLUMNID

La struttura **JET_ENUMCOLUMNID** enumera un set specifico di colonne e, facoltativamente, un set specifico di più valori per tali colonne quando viene utilizzata la funzione [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice di strutture di **JET_ENUMCOLUMNID** .

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Membri

**ColumnID**

ID di colonna da enumerare.

Se l'ID di colonna è 0 (zero), l'enumerazione di questa colonna verrà ignorata e verrà generato uno slot corrispondente nella matrice di output di [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) strutture con lo stato della colonna JET_wrnColumnSkipped.

**ctagSequence**

Identifica facoltativamente una matrice di valori di colonna (in base a un indice in base 1) da enumerare per l'ID di colonna specificato.

Se **ctagSequence** è 0 (zero), **rgtagSequence** viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.

Se un elemento di **rgtagSequence** è 0 (zero), l'enumerazione del valore della colonna (in base a un indice in base 1) verrà ignorata. Uno slot corrispondente nella matrice di output della struttura **JET_ENUMCOLUMNID** verrà generato con un valore di stato della colonna pari a JET_wrnColumnSkipped.

**rgtagSequence**

Matrice di indici in base uno nella matrice di valori di colonna per una colonna specificata. Un singolo elemento è un **itagSequence** definito in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Un **itagSequence** di 0 (zero) indica "Skip". Un **itagSequence** di 1 indica che restituisce il primo valore della colonna, 2 indica il secondo e così via.

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


### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
