---
description: 'Altre informazioni su: struttura JET_INDEXLIST'
title: Struttura JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346996"
---
# <a name="jet_indexlist-structure"></a>Struttura JET_INDEXLIST


_**Si applica a:** Windows | Windows Server_

## <a name="jet_indexlist-structure"></a>Struttura JET_INDEXLIST

La struttura **JET_INDEXLIST** contiene le informazioni necessarie per attraversare una tabella temporanea creata dalle funzioni [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) . Ogni riga della tabella temporanea descrive una colonna di un indice.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni in byte della struttura. La chiamata API aggiornerà questo campo, in modo che il chiamante assicuri che questo valore corrisponda a sizeof (JET_INDEXLIST).

**TableID**

Identificatore di tabella della tabella temporanea creata. È responsabilità del chiamante chiudere la tabella.

**cRecord**

Numero di record nella tabella temporanea creata.

**columnidindexname**

Identificatore di colonna del nome dell'indice.

Questa colonna è un [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

Identificatore di colonna di *grbits* utilizzato nell'indice. Per un elenco di bit validi, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcKey**

Identificatore di colonna del numero di chiavi nell'indice.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcEntry**

Identificatore di colonna del numero di voci nell'indice.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificatore di colonna del numero di pagine utilizzate dall'indice. Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcColumn**

Identificatore di colonna del numero totale di colonne di cui l'indice si estende.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidiColumn**

Identificatore di colonna del numero di colonne nell'indice. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>cIndexInfoCols<br />
15</p></td>
<td><p>Specifica che sono consentite 15 colonne.</p></td>
</tr>
<tr class="even">
<td><p>cColumnInfoCols<br />
14</p></td>
<td><p>Specifica che sono consentite 14 colonne.</p></td>
</tr>
<tr class="odd">
<td><p>cObjectInfoCols<br />
9</p></td>
<td><p>Specifica che sono consentite 9 colonne.</p></td>
</tr>
</tbody>
</table>


**columnidcolumnid**

Identificatore di colonna della colonna indicizzata. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento. Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Identificatore di colonna di coltyp della colonna indicizzata. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento. Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Identificatore di colonna del codice paese della colonna indicizzata. Il codice paese è deprecato.

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Identificatore di colonna dell'identificatore di lingua (LCID) in cui è stato creato l'indice. Per ulteriori informazioni, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Identificatore di colonna della tabella codici in cui è stato creato l'indice. Per ulteriori informazioni, vedere [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Identificatore di colonna della sequenza delle regole di confronto in cui è stato creato l'indice. La sequenza delle regole di confronto è deprecata.

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

Identificatore di colonna di *grbits* che si applicano all'ordine della colonna nell'indice.

I dati di questa colonna possono essere ordinati come JET_bitKeyAscending o JET_bitKeyDescending. Questa colonna è un [JET_coltypLong](./jet-coltyp.md). Ad esempio, un indice definito come "-Column1 \\ 0 + Column2 \\ 0" avrà JET_bitKeyDescending per "Column1" e JET_bitKeyAscending per "Column2".

Per questo membro sono valide le opzioni seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitKeyAscending</p></td>
<td><p>Segmento di indice in ordine crescente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitKeyDescending</p></td>
<td><p>Segmento di indice in ordine decrescente.</p></td>
</tr>
</tbody>
</table>


**columnidcolumnname**

Identificatore di colonna del nome della colonna.

Questa colonna è un [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

Identificatore di colonna dei flag utilizzati per creare l'indice. Per ulteriori informazioni, vedere la sezione **dwMapFlags** di [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Commenti

Ogni riga della tabella temporanea corrisponde a una colonna in un particolare indice.

Ad esempio, l'indice "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0" è più di cinque colonne e occuperà cinque righe nella tabella temporanea. Ognuna di queste cinque righe avrà un valore pari a 5 nella colonna identificata dalla colonna ColumnID. Tuttavia, ogni riga avrà un valore diverso per la colonna ColumnID, che va da 0 a 4.

Il numero di chiavi in un particolare indice corrisponde al numero di valori univoci per cui un chiamante può cercare e ottenere una corrispondenza esatta. Il numero di voci indica il numero di righe corrispondenti a un indice. Se un indice ha un vincolo di univocità, il numero di chiavi è uguale al numero di voci. Se, ad esempio, una tabella contiene le informazioni seguenti e viene creato un indice sulla colonna denominata "Key", sono disponibili tre chiavi (100, 200 e 500), ma vi sono quattro voci ("This", "is", "an" e "example").

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Chiave</p></th>
<th><p>Voce</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>100</p></td>
<td><p>&quot;this&quot;</p></td>
</tr>
<tr class="even">
<td><p>100</p></td>
<td><p>&quot;is&quot;</p></td>
</tr>
<tr class="odd">
<td><p>200</p></td>
<td><p>&quot;un&quot;</p></td>
</tr>
<tr class="even">
<td><p>500</p></td>
<td><p>&quot;example&quot;</p></td>
</tr>
</tbody>
</table>


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
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
