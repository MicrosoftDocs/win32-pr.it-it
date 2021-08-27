---
description: 'Altre informazioni su: JET_CONVERT Structure'
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
ms.openlocfilehash: 9ca27bcc8024d8d3f0f634f6f8e6b23082b8d075
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480507"
---
# <a name="jet_convert-structure"></a>JET_CONVERT struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>JET_CONVERT struttura

La **JET_CONVERT** contiene il nome di una DLL della versione precedente di ESE usata per la lettura di un database creato con tale versione precedente. Vengono inoltre forniti altri flag per controllare la natura della conversione.

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


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_CONVERT_W</strong> (Unicode) <strong>e JET_CONVERT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JetCompact](./jetcompact-function.md)
