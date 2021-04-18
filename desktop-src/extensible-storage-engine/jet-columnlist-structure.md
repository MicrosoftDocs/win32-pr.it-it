---
description: 'Altre informazioni su: struttura JET_COLUMNLIST'
title: Struttura JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308511"
---
# <a name="jet_columnlist-structure"></a>Struttura JET_COLUMNLIST


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columnlist-structure"></a>Struttura JET_COLUMNLIST

La struttura **JET_COLUMNLIST** contiene le informazioni necessarie per attraversare la tabella temporanea creata dalle funzioni [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) . Ogni riga nella tabella temporanea descrive una colonna della tabella specificata nella chiamata API. Questa struttura viene utilizzata solo con [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni in byte della struttura. La chiamata API aggiornerà questo campo, in modo che il chiamante assicuri che questo valore corrisponda a sizeof (JET_COLUMNLIST).

**TableID**

Identificatore di tabella della tabella temporanea creata. È responsabilità del chiamante chiudere la tabella.

**cRecord**

Numero di record nella tabella temporanea creata dalla chiamata API.

**columnidPresentationOrder**

Identificatore di colonna dell'ordine di presentazione.

L'ordine di presentazione viene utilizzato per ordinare le righe della tabella temporanea. L'ordine di presentazione è un [JET_coltypLong](./jet-coltyp.md)fisso. Se il livello di informazioni specificato non è un livello di compattazione, viene anche contrassegnato come JET_bitColumnTTKey.

**columnidcolumnname**

Identificatore di colonna del nome della colonna.

Se il livello di informazioni specificato non è Compact, viene anche contrassegnato come JET_bitColumnTTKey.

**columnidcolumnid**

Identificatore di colonna dell'identificatore di colonna.

L'identificatore di colonna è un [JET_coltypLong](./jet-coltyp.md)fisso.

**columnidcoltyp**

Identificatore di colonna del tipo di colonna.

Il tipo di colonna è un [JET_coltypLong](./jet-coltyp.md)fisso.

**columnidCountry**

Identificatore di colonna del codice paese.

Il codice paese è un [JET_coltypShort](./jet-coltyp.md)fisso.

**columnidLangid**

Identificatore di colonna dell'identificatore di lingua.

L'identificatore di lingua è un [JET_coltypShort](./jet-coltyp.md)fisso.

**columnidCp**

Identificatore di colonna della tabella codici.

La tabella codici è un [JET_coltypShort](./jet-coltyp.md)fisso.

**columnidCollate**

Identificatore di colonna della sequenza delle regole di confronto.

La sequenza delle regole di confronto è un [JET_coltypShort](./jet-coltyp.md)fisso.

**columnidcbMax**

Identificatore di colonna del campo **cbMax** .

**CbMax** è un [JET_coltypLong](./jet-coltyp.md)fisso.

**columnidgrbit**

Identificatore di colonna del *grbits* della colonna. Il campo *grbit* è un [JET_coltypLong](./jet-coltyp.md)fisso. Per ulteriori informazioni su questi bit, vedere [JET_COLUMNDEF](./jet-columndef-structure.md).

Di seguito sono riportati i valori possibili per **columnidgrbit**:

JET_bitColumnTagged

JET_bitColumnFixed

JET_bitColumnUpdatable

JET_bitColumnNotNULL

JET_bitColumnAutoincrement

JET_bitColumnVersion

JET_bitColumnMultiValued

JET_bitColumnEscrowUpdate

JET_bitColumnFinalize

JET_bitColumnDeleteOnZero

JET_bitColumnUserDefinedDefault

**columnidDefault**

Identificatore di colonna del valore predefinito della colonna.

Il valore predefinito è un [JET_coltypLongBinary](./jet-coltyp.md).

**columnidBaseTableName**

Identificatore di colonna del nome della tabella da cui è stata derivata la tabella.

Il nome della tabella è un [JET_coltypText](./jet-coltyp.md).

**columnidBaseColumnName**

Identificatore di colonna del nome della colonna da cui è stata derivata la colonna.

Il nome della colonna è un [JET_coltypText](./jet-coltyp.md).

**columnidDefinitionName**

Identificatore di colonna del nome della definizione di colonna.

Il nome della definizione di colonna è un [JET_coltypText](./jet-coltyp.md).

### <a name="remarks"></a>Commenti

Per impostazione predefinita, l'ordine delle righe nella tabella temporanea viene ordinato in base al nome della colonna. Può anche essere ordinato in base all'identificatore di colonna. Per ulteriori informazioni sull'ordinamento in base all'identificatore di colonna, vedere [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

La chiamata a [JetGetColumnInfo](./jetgetcolumninfo-function.md) o [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) può specificare una forma compatta di risultati. Se sono state ereditate colonne da una tabella modello, i risultati di Compact non li archivia.

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

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
