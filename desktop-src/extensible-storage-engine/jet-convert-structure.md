---
description: 'Altre informazioni su: struttura JET_CONVERT'
title: Struttura JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879829"
---
# <a name="jet_convert-structure"></a>Struttura JET_CONVERT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>Struttura JET_CONVERT

La struttura **JET_CONVERT** contiene il nome di una dll della versione ESE precedente utilizzata per la lettura di un database creato con la versione precedente. Inoltre, vengono forniti altri flag per controllare la natura della conversione.

**Windows Server 2003:** La funzionalità di [JetCompact](./jetcompact-function.md) che ha eseguito una conversione è stata rimossa dal prodotto in Windows Server 2003. È supportato solo in Windows 2000 e Windows XP.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Membri

**SzOldDll**

Nome, incluse le informazioni sul percorso, alla versione precedente della DLL ESE.

**fFlags**

Riservato per l'utilizzo nel sistema.

**fSchemaChangesOnly**

Riservato per l'utilizzo nel sistema.

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
<td><p>Implementato come <strong>JET_CONVERT_W</strong> (Unicode) e <strong>JET_CONVERT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetCompact](./jetcompact-function.md)
