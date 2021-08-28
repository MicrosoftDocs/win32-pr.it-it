---
description: 'Altre informazioni su: JET_COLUMNLIST struttura'
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
ms.openlocfilehash: 6b7f874c95352ce29954adf46b1682dec89c7a9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471797"
---
# <a name="jet_columnlist-structure"></a>Struttura JET_COLUMNLIST


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columnlist-structure"></a>Struttura JET_COLUMNLIST

La **JET_COLUMNLIST** contiene le informazioni necessarie per attraversare la tabella temporanea creata dalle funzioni [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md) Ogni riga della tabella temporanea descrive una colonna nella tabella specificata nella chiamata API. Questa struttura viene usata solo con [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)

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

Dimensione della struttura in byte. La chiamata API aggiornerà questo campo, quindi il chiamante deve assicurarsi che questo valore corrisponda a sizeof( JET_COLUMNLIST ).

**tableid**

Identificatore di tabella della tabella temporanea creata. È responsabilità del chiamante chiudere la tabella.

**cRecord**

Numero di record nella tabella temporanea creata dalla chiamata API.

**columnidPresentationOrder**

Identificatore di colonna dell'ordine di presentazione.

L'ordine di presentazione viene usato per ordinare le righe della tabella temporanea. L'ordine di presentazione è fisso [JET_coltypLong](./jet-coltyp.md). Se il livello di informazioni specificato non è compatto, viene contrassegnato anche come JET_bitColumnTTKey.

**columnidcolumnname**

Identificatore di colonna del nome della colonna.

Se il livello di informazioni specificato non è compatto, viene contrassegnato anche come JET_bitColumnTTKey.

**columnidcolumnid**

Identificatore di colonna dell'identificatore di colonna.

L'identificatore di colonna è un [valore JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Identificatore di colonna del tipo di colonna.

Il tipo di colonna è un tipo [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Identificatore di colonna del codice paese.

Il codice paese è un valore [fisso JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Identificatore di colonna dell'identificatore di lingua.

L'identificatore di lingua è un [valore fisso JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Identificatore di colonna della tabella codici.

La tabella codici è una tabella [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Identificatore di colonna della sequenza di regole di confronto.

La sequenza di regole di confronto è un [valore JET_coltypShort](./jet-coltyp.md).

**columnidcbMax**

Identificatore di colonna del **campo cbMax.**

**CbMax è** un valore fisso [JET_coltypLong](./jet-coltyp.md).

**columnidgrbit**

Identificatore di colonna *dei grbit* della colonna. Il *campo grbit* è un valore [fisso JET_coltypLong](./jet-coltyp.md). Per altre informazioni su questi bit, vedere [JET_COLUMNDEF](./jet-columndef-structure.md).

Di seguito sono riportati i valori possibili **per columnidgrbit:**

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

Per impostazione predefinita, l'ordine delle righe nella tabella temporanea viene ordinato in base al nome della colonna. Può anche essere ordinato in base all'identificatore di colonna. Per altre informazioni sull'ordinamento in base all'identificatore di colonna, vedere [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)

La chiamata a [JetGetColumnInfo](./jetgetcolumninfo-function.md) o [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) potrebbe specificare una forma compatta di risultati. Se una o più colonne sono state ereditate da una tabella modello, i risultati compatti non le archivieranno.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



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
