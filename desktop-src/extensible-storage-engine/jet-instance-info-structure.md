---
description: 'Altre informazioni su: struttura JET_INSTANCE_INFO'
title: Struttura JET_INSTANCE_INFO
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
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885025"
---
# <a name="jet_instance_info-structure"></a>Struttura JET_INSTANCE_INFO


_**Si applica a:** Windows | Windows Server_

## <a name="jet_instance_info-structure"></a>Struttura JET_INSTANCE_INFO

La struttura **JET_INSTANCE_INFO** riceve informazioni sulle istanze di database in esecuzione quando vengono utilizzate con le funzioni [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) e [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .

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

[JET_INSTANCE](./jet-instance.md) dell'istanza di specificata.

**szInstanceName**

Il nome dell'istanza di database. Questo valore può essere **null** se l'istanza non ha un nome.

**cDatabases**

Numero di database collegati all'istanza del database. **cDatabases** include inoltre la dimensione delle matrici di stringhe restituite in **szDatabaseFileName**, **szDatabaseDisplayName** e **szDatabaseSLVFileName**.

**szDatabaseFileName**

Matrice di stringhe, ognuna delle quali contiene il nome file di un database associato all'istanza del database. La matrice contiene elementi **cDatabases** .

**szDatabaseDisplayName**

Matrice di stringhe, ognuna delle quali contiene il nome visualizzato di un database. Attualmente la stringa può essere NULL. La matrice contiene elementi **cDatabases** .

**szDatabaseSLVFileName**

Matrice di stringhe, ognuna delle quali contiene il nome file del file SLV collegato all'istanza del database. La matrice contiene elementi **cDatabases** . I file SLV non sono supportati, pertanto questo campo deve essere ignorato.

### <a name="remarks"></a>Commenti

A ogni istanza di database possono essere collegati diversi database.

Per una determinata struttura di **JET_INSTANCE_INFO** , la matrice di stringhe restituita per i database si trova nello stesso ordine. Ad esempio, "szDatabaseDisplayName \[ i \] " e "szDatabaseFileName \[ i \] " si riferiscono entrambi allo stesso database.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_INSTANCE_INFO_W</strong> (Unicode) e <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
