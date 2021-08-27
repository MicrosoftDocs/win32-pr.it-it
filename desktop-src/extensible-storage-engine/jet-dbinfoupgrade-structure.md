---
description: 'Altre informazioni su: JET_DBINFOUPGRADE struttura'
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
ms.openlocfilehash: 57c9265f45412bd31e087a52ab2b923c9c55c430
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467658"
---
# <a name="jet_dbinfoupgrade-structure"></a>Struttura JET_DBINFOUPGRADE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_dbinfoupgrade-structure"></a>Struttura JET_DBINFOUPGRADE

La **JET_DBINFOUPGRADE** contiene informazioni sullo stato di aggiornamento del database. Questo valore viene recuperato solo se **JET_DBINFOUPGRADE** stato passato a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo.](./jetgetdatabasefileinfo-function.md) Questa struttura non è necessaria per le versioni correnti del sistema operativo del motore di database.

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

Impostare sulla dimensione della **struttura JET_DBINFOUPGRADE,** in byte.

**cbFilesizeLow**

Valore **DWORD basso** che riflette le dimensioni correnti del file per il database.

**cbFilesizeHigh**

Valore **DWORD elevato che** riflette le dimensioni correnti del file per il database.

**cbFreeSpaceRequiredLow**

Valore **DWORD basso dello** spazio disponibile su disco stimato necessario per un aggiornamento sul posto.

**cbFreeSpaceRequiredHigh**

Valore **DWORD elevato dello** spazio disponibile su disco stimato necessario per un aggiornamento sul posto.

**csecToUpgrade**

Tempo stimato necessario per l'aggiornamento, espresso in secondi.

**ulFlags**

Campo di bit costituito da zero o più dei flag seguenti: **fUpgradable**, **fAlreadyUpgraded**.

**fUpgradable**

Il database è aggiornabile.

**fAlreadyUpgraded**

Il database viene aggiornato al formato di database corrente.

### <a name="remarks"></a>Commenti

Una **JET_DBINFOUPGRADE** viene popolata da una chiamata a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo.](./jetgetdatabasefileinfo-function.md) Se la funzione non riesce, il contenuto della struttura non è definito.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
