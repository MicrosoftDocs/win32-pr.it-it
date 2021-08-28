---
description: 'Altre informazioni su: JET_OBJECTINFO struttura'
title: Struttura JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
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
ms.openlocfilehash: d61c42897da6d55dc96f2e59847fcf727424d60e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986124"
---
# <a name="jet_objectinfo-structure"></a>Struttura JET_OBJECTINFO


_**Si applica a:** Windows | Windows Server_

## <a name="jet_objectinfo-structure"></a>Struttura JET_OBJECTINFO

La **JET_OBJECTINFO** contiene informazioni su un oggetto. Le tabelle sono gli unici tipi di oggetto attualmente supportati.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, della **JET_OBJECTINFO** struttura .

**objtyp**

Contiene il [JET_OBJTYP](./jet-objtyp.md) della struttura . Attualmente verranno restituite solo le tabelle, ovvero JET_objtypTable.

**dtCreate**

Obsoleta. Non usare.

**dtUpdate**

Obsoleta. Non usare.

**grbit**

Gruppo di bit che contengono le opzioni disponibili per questa chiamata, che includono zero o più degli elementi seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTableInfoBookmark</p> | <p>La tabella può contenere segnalibri.</p> | 
| <p>JET_bitTableInfoRollback</p> | <p>È possibile eseguire il rollback della tabella.</p> | 
| <p>JET_bitTableInfoUpdatable</p> | <p>La tabella può essere aggiornata.</p> | 



**flags**

Campo di bit che contiene zero o più dei flag seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitObjectSystem</p> | <p>La tabella è una tabella di sistema ed è solo per uso interno.</p> | 
| <p>JET_bitObjectTableDerived</p> | <p>DDL ereditato dalla tabella di una tabella modello.</p> | 
| <p>JET_bitObjectTableFixedDDL</p> | <p>Non è possibile modificare il linguaggio DDL per la tabella.</p> | 
| <p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p> | <p>Usato in combinazione con JET_bitObjectTableTemplate per non consentire colonne fisse o variabili nelle tabelle derivate (in modo che le colonne fisse o variabili possano essere aggiunte al modello in futuro).</p><p><strong>Windows XP:</strong> Questo valore è stato introdotto in Windows XP.</p> | 
| <p>JET_bitObjectTableTemplate</p> | <p>La tabella è una tabella modello.</p> | 



**cRecord**

Numero di record nella tabella.

Questo valore viene recuperato solo se **JET_OBJECTINFO** stato passato [a JetGetObjectInfo.](./jetgetobjectinfo-function.md)

**cPage**

Numero di pagine utilizzate dalla tabella.

Questo valore viene recuperato solo se **JET_OBJECTINFO** stato passato [a JetGetObjectInfo.](./jetgetobjectinfo-function.md)

### <a name="remarks"></a>Commenti

Una **JET_OBJECTINFO** viene popolata da una chiamata a [JetGetObjectInfo](./jetgetobjectinfo-function.md) o [JetGetTableInfo.](./jetgettableinfo-function.md) Se la chiamata API non riesce, il contenuto della struttura non è definito.

Se applicabile, le statistiche della tabella includono il numero di record e il numero di pagine presenti nell'indice cluster, ovvero l'indice contenente i dati del record. Le statistiche dell'indice sono accessibili separatamente in base al nome, [usando JetGetIndexInfo](./jetgetindexinfo-function.md) [o JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
