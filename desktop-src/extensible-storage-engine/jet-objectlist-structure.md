---
description: 'Altre informazioni su: JET_OBJECTLIST struttura'
title: Struttura JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21a3ea030421406a5bc571bb5cc1887f77b4710d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983124"
---
# <a name="jet_objectlist-structure"></a>Struttura JET_OBJECTLIST


_**Si applica a:** Windows | Windows Server_

## <a name="jet_objectlist-structure"></a>Struttura JET_OBJECTLIST

La **JET_OBJECTLIST** attraversa una tabella temporanea creata con [JetGetObjectInfo.](./jetgetobjectinfo-function.md) Ogni riga della tabella temporanea descrive un oggetto nel database.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni della struttura, in byte. La chiamata API aggiornerà questo campo, quindi il chiamante deve assicurarsi che questo valore corrisponda a sizeof( JET_INDEXLIST ).

**tableid**

Identificatore di tabella della tabella temporanea creata. Il chiamante deve contenere codice che chiuderà la tabella.

**cRecord**

Numero di record nella tabella temporanea creata.

**columnidcontainername**

Identificatore di colonna del nome del tipo di contenitore.

Gli unici contenitori attualmente supportati sono le tabelle. Questa colonna è un [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

Identificatore di colonna del nome dell'oggetto.

Questa colonna è un [JET_coltypText](./jet-coltyp.md).

**columnidobjtyp**

Identificatore di colonna del tipo dell'oggetto. Gli unici contenitori attualmente supportati sono le tabelle, quindi questo campo verrà JET_objtypTable.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columniddtCreate**

Obsoleta. Non usare.

**columniddtUpdate**

Obsoleta. Non usare.

**columnidgrbit**

Identificatore di colonna dei **grbit applicabili** all'oggetto. Per un elenco di **grbit applicabili,** vedere [JET_TABLECREATE](./jet-tablecreate-structure.md).

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

Identificatore di colonna dei flag applicabili all'oggetto. Per un elenco dei flag applicabili, vedere [JET_OBJECTINFO](./jet-objectinfo-structure.md).

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcRecord**

Identificatore di colonna del numero di record presenti nella tabella denominata in **columnidobjectname**.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificatore di colonna del numero di pagine utilizzate dall'oggetto.

Questa colonna è un [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Commenti

Ogni riga della tabella temporanea corrisponde a un oggetto nel database.

Quando la tabella temporanea viene creata con il parametro *InfoLevel* nella funzione [JetGetObjectInfo](./jetgetobjectinfo-function.md) impostato su JET_ObjInfoListNoStats, le colonne identificate da **columnidcRecord** e **columnidcPage** non conterranno informazioni significative.

Attualmente, nella tabella temporanea saranno presenti solo le informazioni sulle tabelle.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)
