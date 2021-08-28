---
description: 'Altre informazioni su: JET_INSTANCE_INFO struttura'
title: JET_INSTANCE_INFO struttura
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
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
ms.openlocfilehash: 6dbeab994d012f031de7620487c754b69d00db3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472697"
---
# <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO struttura

La **JET_INSTANCE_INFO** riceve informazioni sull'esecuzione di istanze di database quando viene usata con le funzioni [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) e [JetOSSnapshotFreeze.](./jetossnapshotfreeze-function.md)

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a>Membri

**hInstanceId**

Valore [JET_INSTANCE](./jet-instance.md) dell'istanza specificata.

**szInstanceName**

Il nome dell'istanza di database. Questo valore può essere **NULL** se l'istanza non ha un nome.

**cDatabases**

Numero di database collegati all'istanza del database. **cDatabases** contiene anche le dimensioni delle matrici di stringhe restituite in **szDatabaseFileName**, **szDatabaseDisplayName** e **szDatabaseSLVFileName**.

**szDatabaseFileName**

Matrice di stringhe, ognuna delle quali contiene il nome file di un database collegato all'istanza del database. La matrice contiene **elementi cDatabases.**

**szDatabaseDisplayName**

Matrice di stringhe, ognuna delle quali contiene il nome visualizzato di un database. Attualmente la stringa può essere NULL. La matrice contiene **elementi cDatabases.**

**szDatabaseSLVFileName**

Matrice di stringhe, ognuna delle quali contiene il nome del file SLV collegato all'istanza del database. La matrice contiene **elementi cDatabases.** I file SLV non sono supportati, quindi questo campo deve essere ignorato.

### <a name="remarks"></a>Commenti

A ogni istanza del database possono essere collegati diversi database.

Per una **struttura JET_INSTANCE_INFO,** la matrice di stringhe restituita per i database è nello stesso ordine. Ad esempio, "szDatabaseDisplayName \[ i \] " e "szDatabaseFileName \[ i " fanno entrambi riferimento allo stesso \] database.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_INSTANCE_INFO_W</strong> (Unicode) <strong>e JET_INSTANCE_INFO _A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
