---
description: 'Altre informazioni su: struttura JET_DBINFOUPGRADE'
title: Struttura JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306831"
---
# <a name="jet_dbinfoupgrade-structure"></a>Struttura JET_DBINFOUPGRADE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_dbinfoupgrade-structure"></a>Struttura JET_DBINFOUPGRADE

La struttura **JET_DBINFOUPGRADE** include informazioni sullo stato di aggiornamento del database. Questo valore viene recuperato solo se **JET_DBINFOUPGRADE** è stato passato a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Questa struttura non è necessaria per le versioni correnti del sistema operativo del motore di database.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a>Membri

**cbStruct**

Impostare sulla dimensione della struttura di **JET_DBINFOUPGRADE** , in byte.

**cbFilesizeLow**

**DWORD** basso che riflette le dimensioni correnti del file per il database.

**cbFilesizeHigh**

**Valore DWORD** elevato che rispecchia le dimensioni correnti del file per il database.

**cbFreeSpaceRequiredLow**

Il **valore DWORD** basso dello spazio disponibile su disco stimato necessario per un aggiornamento sul posto.

**cbFreeSpaceRequiredHigh**

**Valore DWORD** alto dello spazio disponibile su disco stimato necessario per un aggiornamento sul posto.

**csecToUpgrade**

Tempo stimato necessario per l'aggiornamento, in secondi.

**ulFlags**

Un campo di bit è costituito da zero o più dei flag seguenti: **fUpgradable**, **fAlreadyUpgraded**.

**fUpgradable**

Il database è aggiornabile.

**fAlreadyUpgraded**

Il database viene aggiornato al formato del database corrente.

### <a name="remarks"></a>Commenti

Una struttura **JET_DBINFOUPGRADE** viene popolata da una chiamata a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Se la funzione ha esito negativo, il contenuto della struttura non è definito.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
