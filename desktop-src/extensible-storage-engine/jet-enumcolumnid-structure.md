---
description: 'Altre informazioni su: JET_ENUMCOLUMNID Structure'
title: JET_ENUMCOLUMNID struttura
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
ms.openlocfilehash: 21f28e160f1c31dac909e02bf64acba0ae230305
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479644"
---
# <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID struttura

La **JET_ENUMCOLUMNID** enumera un set specifico di colonne e, facoltativamente, un set specifico di più valori per tali colonne quando viene usata la funzione [JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice **di** JET_ENUMCOLUMNID strutture.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Membri

**columnid**

ID di colonna da enumerare.

Se l'ID colonna è 0 (zero), l'enumerazione di questa colonna viene ignorata e viene generato uno slot corrispondente nella matrice di output delle strutture [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) con stato di colonna JET_wrnColumnSkipped.

**ctagSequence**

Identifica facoltativamente una matrice di valori di colonna (in base all'indice in base uno) da enumerare per l'ID di colonna specificato.

Se **ctagSequence** è 0 (zero), **rgtagSequence** viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.

Se un elemento **di rgtagSequence** è 0 (zero), l'enumerazione di tale valore di colonna (in base all'indice in base uno) verrà ignorata. Uno slot corrispondente nella matrice di output della **struttura JET_ENUMCOLUMNID** verrà generato con un valore di stato della colonna JET_wrnColumnSkipped.

**rgtagSequence**

Matrice di indici in base uno nella matrice di valori di colonna per una determinata colonna. Un singolo elemento è **un elemento itagSequence** definito [in](./jet-retrievecolumn-structure.md)JET_RETRIEVECOLUMN . Un **valore itagSequence** pari a 0 (zero) indica "skip". Un **valore itagSequence** pari a 1 indica che restituisce il valore della prima colonna della colonna, 2 indica la seconda e così via.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
