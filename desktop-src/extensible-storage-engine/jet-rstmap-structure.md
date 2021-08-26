---
description: 'Altre informazioni su: JET_RSTMAP struttura'
title: JET_RSTMAP struttura
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
ms.openlocfilehash: 8e9952c040540e78c76d81babbb4c7b326fe92f8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465858"
---
# <a name="jet_rstmap-structure"></a>JET_RSTMAP struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_rstmap-structure"></a>JET_RSTMAP struttura

La **JET_RSTMAP** consente il remapping dei percorsi dei file di database archiviati nei log delle transazioni durante il recupero, se usato dalle funzioni [JetInit](./jetinit-function.md) e [JetExternalRestore.](./jetexternalrestore-function.md) In questo modo i database possono essere spostati offline o quando vengono ripristinati dal backup.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Membri

**szDatabaseName**

Percorso assoluto corrente di un database associato ai log delle transazioni riprodotti durante il recupero.

**szNewDatabaseName**

Nuovo percorso assoluto per il database.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_RSTMAP_W</strong> (Unicode) <strong>e JET_RSTMAP_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
