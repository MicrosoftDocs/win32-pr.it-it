---
description: 'Altre informazioni su: struttura JET_RETINFO'
title: Struttura JET_RETINFO
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879610"
---
# <a name="jet_retinfo-structure"></a>Struttura JET_RETINFO


_**Si applica a:** Windows | Windows Server_

## <a name="jet_retinfo-structure"></a>Struttura JET_RETINFO

La struttura **JET_RETINFO** contiene parametri di input e output facoltativi per [JetRetrieveColumn](./jetretrievecolumn-function.md). Un puntatore null può essere passato dove un puntatore a questa struttura verrebbe altrimenti passato. Il passaggio di un puntatore null equivale a passare **JET_RETINFO** con **cbStruct** impostato su sizeof (JET_RETINFO), **ibLongValue** impostato su 0 (zero) e **itagSequence** impostato su 1.

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

Deve essere impostato sulla dimensione della struttura di **JET_RETINFO** , in byte, e serve per confermare la presenza dei campi seguenti.

**ibLongValue**

Offset al primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md). Si noti che la quantità di dati recuperati da questo offset è inferiore alle dimensioni del buffer di output e alla dimensione dei dati nel valore effettivo dopo questo offset.

**itagSequence**

Descrive il numero di sequenza del valore in una colonna multivalore. Si noti che la matrice di valori è in base uno. Il primo valore è Sequence 1, not 0. Se la colonna record ha un solo valore, è necessario passare 1 come **itagSequence**

Con una colonna che può contenere più valori, è possibile usare un numero di sequenza maggiore di 1 in [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 in [JetSetColumn](./jetsetcolumn-function.md). Nell'implementazione corrente del motore, qualsiasi colonna creata con JET_bitColumnTagged può contenere più valori. Le colonne create con JET_bitColumnMultiValued differiscono dalle colonne con tag multivalore solo nel modo in cui vengono indicizzate. Per ulteriori informazioni, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

**columnidNextTagged**

Restituisce l'ColumnID della colonna con tag, multivalore o di tipo sparse recuperata quando tutte le colonne con tag vengono recuperate passando 0 come ColumnID a [JetRetrieveColumn](./jetretrievecolumn-function.md).

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
