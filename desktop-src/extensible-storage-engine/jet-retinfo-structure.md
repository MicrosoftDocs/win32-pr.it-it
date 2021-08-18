---
description: 'Altre informazioni su: JET_RETINFO struttura'
title: JET_RETINFO struttura
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: a04ee087f036bf0d6a9e0bb4c9c558dbfe3ae5a8fc8e875973ef2930e7ba911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038729"
---
# <a name="jet_retinfo-structure"></a>JET_RETINFO struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_retinfo-structure"></a>JET_RETINFO struttura

La **JET_RETINFO** contiene parametri di input e output facoltativi [per JetRetrieveColumn](./jetretrievecolumn-function.md). In caso contrario, è possibile passare un puntatore Null in cui verrebbe passato un puntatore a questa struttura. Il passaggio di un puntatore Null equivale **a** passare JET_RETINFO con **cbStruct** impostato su sizeof(JET_RETINFO), **ibLongValue** impostato su 0 (zero) e **itagSequence** impostato su 1.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>Membri

**cbStruct**

Deve essere impostato sulla dimensione della struttura **JET_RETINFO,** in byte, e serve per confermare la presenza dei campi seguenti.

**ibLongValue**

Offset del primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md). Si noti che la quantità di dati recuperati da questo offset è inferiore alla dimensione del buffer di output e alle dimensioni dei dati nel valore effettivo dopo questo offset.

**itagSequence**

Descrive il numero di sequenza del valore in una colonna multivalore. Si noti che la matrice di valori è basata su uno. Il primo valore è la sequenza 1, non 0. Se la colonna del record ha un solo valore, è necessario passare 1 come **itagSequence**

Con una colonna che può contenere più valori, è possibile usare solo un numero di sequenza maggiore di 1 in [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 in [JetSetColumn](./jetsetcolumn-function.md). Nell'implementazione corrente del motore, qualsiasi colonna creata con JET_bitColumnTagged può contenere più valori. Le colonne create con JET_bitColumnMultiValued differiscono dalle colonne con tag multivalore solo nel modo in cui vengono indicizzate. Per [altre JET_INDEXCREATE,](./jet-indexcreate-structure.md) vedere JET_INDEXCREATE.

**columnidNextTagged**

Restituisce il columnid della colonna con tag, multivalore o sparse recuperata quando tutte le colonne con tag vengono recuperate passando 0 come columnid [a JetRetrieveColumn](./jetretrievecolumn-function.md).

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
