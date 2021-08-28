---
description: 'Altre informazioni su: JET_SETINFO Structure'
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
ms.openlocfilehash: 4198598a95134291e9b9aa88eb9dcdf4ada79045
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983814"
---
# <a name="jet_setinfo-structure"></a>JET_SETINFO struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_setinfo-structure"></a>JET_SETINFO struttura

La **JET_SETINFO** contiene parametri di input facoltativi per [JetSetColumn.](./jetsetcolumn-function.md) In **caso contrario,** è possibile passare un puntatore NULL in cui verrebbe passato un puntatore a questa struttura. Il significato del passaggio di **null** è lo stesso del passaggio **di JET_SETINFO** con **cbStruct** impostato su sizeof(JET_SETINFO), **ibLongValue** impostato su 0 (zero) e **itagSequence** impostato su 1.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, **dell'oggetto JET_SETINFO**. Questo valore conferma la presenza dei campi seguenti.

**ibLongValue**

Offset del primo byte da impostare in una colonna di tipo JET_coltypLongBinary [o](./jet-coltyp.md) [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Descrive il numero di sequenza del valore in una colonna multivalore da impostare. La matrice di valori è in base uno. Il primo valore è la sequenza 1, non 0 (zero). Se la colonna del record ha un solo valore, è necessario passare 1 come **itagSequence** se tale valore viene sostituito. Il valore 0 (zero) indica l'aggiunta di una nuova istanza del valore di colonna alla fine della sequenza di valori di colonna.

Con una colonna che può contenere più valori, è possibile usare solo un numero di sequenza maggiore di 1 in [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 in [JetSetColumn](./jetsetcolumn-function.md). Nell'implementazione corrente del motore, qualsiasi colonna creata con JET_bitColumnTagged può contenere più valori. Le colonne create con JET_bitColumnMultiValued differiscono dalle colonne con tag multivalore solo nel modo in cui vengono indicizzate. Vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) per altre informazioni.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetSetColumn](./jetsetcolumn-function.md)
