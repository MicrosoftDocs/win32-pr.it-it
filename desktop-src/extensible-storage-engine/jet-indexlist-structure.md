---
description: 'Altre informazioni su: JET_INDEXLIST struttura'
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
ms.openlocfilehash: c57fda6eaea161839cdaa758c41f13749d4c5eda
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480047"
---
# <a name="jet_indexlist-structure"></a>Struttura JET_INDEXLIST


_**Si applica a:** Windows | Windows Server_

## <a name="jet_indexlist-structure"></a>Struttura JET_INDEXLIST

La **JET_INDEXLIST** contiene le informazioni necessarie per attraversare una tabella temporanea creata dalle funzioni [JetGetIndexInfo](./jetgetindexinfo-function.md) [o JetGetTableIndexInfo.](./jetgettableindexinfo-function.md) Ogni riga della tabella temporanea descrive una colonna di un indice.

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

Dimensione della struttura in byte. La chiamata API aggiornerà questo campo, quindi il chiamante deve assicurarsi che questo valore corrisponda a sizeof( JET_INDEXLIST ).

**tableid**

Identificatore di tabella della tabella temporanea creata. È responsabilità del chiamante chiudere la tabella.

**cRecord**

Numero di record nella tabella temporanea creata.

**columnidindexname**

Identificatore di colonna del nome dell'indice.

Questa colonna è un [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

Identificatore di colonna degli *grbit usati* nell'indice. Vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) per un elenco di bit validi.

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

Identificatore di colonna del numero totale di colonne su cui si estende l'indice.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidiColumn**

Identificatore di colonna del numero di colonne nell'indice. Per altre informazioni, vedere la sezione Osservazioni di questo argomento.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>cIndexInfoCols<br />15</p> | <p>Specifica che sono consentite 15 colonne.</p> | 
| <p>cColumnInfoCols<br />14</p> | <p>Specifica che sono consentite 14 colonne.</p> | 
| <p>cObjectInfoCols<br />9</p> | <p>Specifica che sono consentite 9 colonne.</p> | 



**columnidcolumnid**

Identificatore di colonna della colonna indicizzata. Per altre informazioni, vedere la sezione Osservazioni di questo argomento. Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Identificatore di colonna della coltyp della colonna indicizzata. Per altre informazioni, vedere la sezione Osservazioni di questo argomento. Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Identificatore di colonna del codice paese della colonna indicizzata. Il codice paese è deprecato.

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Identificatore di colonna dell'identificatore di lingua (LCID) in cui è stato creato l'indice. Per altre informazioni, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Identificatore di colonna della tabella codici in cui è stato creato l'indice. Per altre informazioni, vedere [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Identificatore di colonna della sequenza di regole di confronto in cui è stato creato l'indice. La sequenza di regole di confronto è deprecata.

Questa colonna è un [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

Identificatore di colonna dei *grbit che* si applicano all'ordine della colonna nell'indice.

I dati per questa colonna possono essere ordinati come JET_bitKeyAscending o JET_bitKeyDescending. Questa colonna è un [JET_coltypLong](./jet-coltyp.md). Ad esempio, un indice definito come "-column1 \\ 0+column2 0" avrà JET_bitKeyDescending per "column1" e JET_bitKeyAscending \\ per "column2".

Le opzioni seguenti sono valide per questo membro.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>Segmento di indice in ordine crescente.</p> | 
| <p>JET_bitKeyDescending</p> | <p>Segmento di indice in ordine decrescente.</p> | 



**columnidcolumnname**

Identificatore di colonna del nome della colonna.

Questa colonna è un [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

Identificatore di colonna dei flag utilizzati per creare l'indice. Per altre informazioni, vedere la **sezione dwMapFlags** [di JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Commenti

Ogni riga della tabella temporanea corrisponde a una colonna in un indice specifico.

Ad esempio, l'indice "+A \\ 0+B \\ 0+C \\ 0+D \\ 0+E \\ 0" è maggiore di cinque colonne e occuperà cinque righe nella tabella temporanea. Ognuna di queste cinque righe avrà un valore pari a 5 nella colonna identificata dalla colonna columnid. Tuttavia, ogni riga avrà un valore diverso per columnid columnid, compreso tra 0 e 4.

Il numero di chiavi in un determinato indice corrisponde al numero di valori univoci per i quali un chiamante può cercare e ottenere una corrispondenza esatta. Il numero di voci è il numero di righe corrispondenti a un indice. Se un indice ha un vincolo di univocità, il numero di chiavi è uguale al numero di voci. Ad esempio, se una tabella contiene le informazioni seguenti e viene creato un indice sulla colonna denominata "key", sono presenti tre chiavi (100, 200 e 500), ma sono presenti quattro voci ("this", "is", "an" e "example").


| <p>Chiave</p> | <p>Voce</p> | 
|------------|--------------|
| <p>100</p> | <p>"this"</p> | 
| <p>100</p> | <p>"is"</p> | 
| <p>200</p> | <p>"an"</p> | 
| <p>500</p> | <p>"example"</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



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
