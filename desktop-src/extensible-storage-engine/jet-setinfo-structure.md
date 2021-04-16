---
description: 'Altre informazioni su: struttura JET_SETINFO'
title: Struttura JET_SETINFO
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531117"
---
# <a name="jet_setinfo-structure"></a>Struttura JET_SETINFO


_**Si applica a:** Windows | Windows Server_

## <a name="jet_setinfo-structure"></a>Struttura JET_SETINFO

La struttura **JET_SETINFO** contiene parametri di input facoltativi per [JetSetColumn](./jetsetcolumn-function.md). Un puntatore **null** può essere passato dove un puntatore a questa struttura verrebbe altrimenti passato. Il significato del passaggio di un **valore null** equivale al passaggio **di JET_SETINFO** con **cbStruct** impostato su sizeof (JET_SETINFO), **ibLongValue** impostato su 0 (zero) e **itagSequence** impostato su 1.

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

Offset al primo byte da impostare in una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Descrive il numero di sequenza del valore in una colonna multivalore da impostare. La matrice di valori è in base uno. Il primo valore è Sequence 1, non 0 (zero). Se la colonna record ha un solo valore, è necessario passare 1 come **itagSequence** se tale valore viene sostituito. Il valore 0 (zero) indica di aggiungere una nuova istanza di valore di colonna alla fine della sequenza dei valori di colonna.

Con una colonna che può contenere più valori, è possibile usare un numero di sequenza maggiore di 1 in [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 in [JetSetColumn](./jetsetcolumn-function.md). Nell'implementazione corrente del motore, qualsiasi colonna creata con JET_bitColumnTagged può contenere più valori. Le colonne create con JET_bitColumnMultiValued differiscono dalle colonne con tag multivalore solo nel modo in cui vengono indicizzate. Per ulteriori informazioni, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

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

[JetSetColumn](./jetsetcolumn-function.md)
