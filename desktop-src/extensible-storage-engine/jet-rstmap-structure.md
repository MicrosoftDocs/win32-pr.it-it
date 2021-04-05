---
description: 'Altre informazioni su: struttura JET_RSTMAP'
title: Struttura JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750554"
---
# <a name="jet_rstmap-structure"></a>Struttura JET_RSTMAP


_**Si applica a:** Windows | Windows Server_

## <a name="jet_rstmap-structure"></a>Struttura JET_RSTMAP

La struttura di **JET_RSTMAP** consente di rimappare i percorsi dei file di database archiviati nei log delle transazioni durante il ripristino, se utilizzati dalle funzioni [JetInit](./jetinit-function.md) e [JetExternalRestore](./jetexternalrestore-function.md) . Ciò consente lo spostamento dei database in modalità offline o quando vengono ripristinati dal backup.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Membri

**szDatabaseName**

Percorso assoluto corrente di un database associato ai log delle transazioni riprodotti durante il ripristino.

**szNewDatabaseName**

Nuovo percorso assoluto per il database.

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
<td><p>Implementato come <strong>JET_RSTMAP_W</strong> (Unicode) e <strong>JET_RSTMAP_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
