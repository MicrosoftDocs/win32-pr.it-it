---
description: 'Altre informazioni su: JET_SETINFO struttura'
title: JET_SETINFO struttura
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 379fd60a001312152dbe181c27a3e8158ceca79b4cfa9075a530b6c73f4337cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253442"
---
# <a name="jet_setinfo-structure"></a>JET_SETINFO struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_setinfo-structure"></a>JET_SETINFO struttura

La **JET_SETINFO** contiene parametri di input facoltativi per [JetSetColumn.](./jetsetcolumn-function.md) È **possibile passare** un puntatore NULL dove verrebbe passato un puntatore a questa struttura. Il significato del passaggio di un valore **NULL** equivale al passaggio di **JET_SETINFO** con **cbStruct** impostato su sizeof(JET_SETINFO), **ibLongValue** impostato su 0 (zero) e **itagSequence** impostato su 1.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, del **JET_SETINFO**. Questo valore conferma la presenza dei campi seguenti.

**ibLongValue**

Offset del primo byte da impostare in una colonna di tipo JET_coltypLongBinary [o](./jet-coltyp.md) [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Descrive il numero di sequenza del valore in una colonna multivalore da impostare. La matrice di valori è in base uno. Il primo valore è la sequenza 1, non 0 (zero). Se la colonna del record ha un solo valore, è necessario passare 1 come **itagSequence** se tale valore viene sostituito. Il valore 0 (zero) indica l'aggiunta di una nuova istanza del valore di colonna alla fine della sequenza di valori di colonna.

Con una colonna che può contenere più valori, è possibile usare solo un numero di sequenza maggiore di 1 in [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 in [JetSetColumn](./jetsetcolumn-function.md). Nell'implementazione corrente del motore, qualsiasi colonna creata con JET_bitColumnTagged può contenere più valori. Le colonne create con JET_bitColumnMultiValued differiscono dalle colonne con tag multivalore solo nel modo in cui vengono indicizzate. Vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) per altre informazioni.

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

[JetSetColumn](./jetsetcolumn-function.md)
