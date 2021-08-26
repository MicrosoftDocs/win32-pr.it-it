---
description: 'Altre informazioni su: JET_CONDITIONALCOLUMN struttura'
title: JET_CONDITIONALCOLUMN struttura
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: dacaff181b40af870bd01bf9d287683c3d3d63a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469478"
---
# <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN struttura

La **JET_CONDITIONALCOLUMN** definisce la modalità di esecuzione dell'indicizzazione condizionale per un determinato indice. Un indice condizionale contiene una voce di indice solo per le righe che soddisfano la condizione specificata. Tuttavia, la colonna condizionale non fa parte della chiave dell'indice, ma controlla solo la presenza della voce di indice.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Membri

**cbStruct**

Questo campo deve essere inizializzato su sizeof( JET_CONDITIONALCOLUMN ), in byte.

**szColumnName**

Nome della colonna che contiene i dati in cui il motore di database indicizza in modo condizionale la riga.

**grbit** Gruppo di bit che fornisce le opzioni per l'indice condizionale. Il passaggio di zero valori or **OR** logicamente non è valido **per** JET_CONDITIONALCOLUMN . Il campo di bit deve essere esattamente uno dei seguenti:


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitIndexColumnMustBeNull</p> | <p>La colonna specificata dal <em>parametro szColumnName</em> deve essere NULL perché una voce di indice venga visualizzata in questo indice per una determinata riga.</p> | 
| <p>JET_bitIndexColumnMustBeNonNull</p> | <p>La colonna specificata dal <em>parametro szColumnName</em> deve essere non NULL per una voce di indice perché una determinata riga venga visualizzata in questo indice.</p> | 



### <a name="remarks"></a>Commenti

Un indice condizionale contiene una voce di indice solo per le righe che soddisfano la condizione specificata. Ad esempio, una colonna può essere denominata "Marked" e quando una riga è contrassegnata, la colonna viene impostata su un valore non NULL. Un JET_bitIndexColumnMustBeNonNull'indice condizionale in questa colonna mostrerà tutte le righe contrassegnate e un indice condizionale JET_bitIndexColumnMustBeNull mostra le righe non contrassegnate. Questo è anche un modo pratico per eseguire l'eliminazione di un flag e l'indice di Garbage Collection.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) <strong>e JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
