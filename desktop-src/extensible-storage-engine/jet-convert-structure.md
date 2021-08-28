---
description: 'Altre informazioni su: JET_CONVERT struttura'
title: JET_CONVERT struttura
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
ms.openlocfilehash: ce3fbcc7de9c7904689de3df923a87d575b1b92b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986784"
---
# <a name="jet_convert-structure"></a>JET_CONVERT struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>JET_CONVERT struttura

La **JET_CONVERT** contiene il nome di una DLL della versione precedente di ESE utilizzata per la lettura di database creati con tale versione precedente. Vengono inoltre forniti altri flag per controllare la natura della conversione.

**Windows Server 2003:** La funzionalità di [JetCompact che](./jetcompact-function.md) ha eseguito una conversione è stata rimossa dal prodotto in Windows Server 2003. È supportato solo in Windows 2000 e Windows XP.

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

Nome, incluse le informazioni sul percorso, della versione precedente della DLL ESE.

**fFlags**

Riservato per l'utilizzo nel sistema.

**fSchemaChangesOnly**

Riservato per l'utilizzo nel sistema.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_CONVERT_W</strong> (Unicode) <strong>e JET_CONVERT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JetCompact](./jetcompact-function.md)
