---
description: 'Altre informazioni su: JET_SIGNATURE Structure'
title: JET_SIGNATURE struttura
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: da4684872358d9d6751812b2adb2b2bea819a2e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476477"
---
# <a name="jet_signature-structure"></a>JET_SIGNATURE struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_signature-structure"></a>JET_SIGNATURE struttura

La **JET_SIGNATURE** contiene informazioni che identificano in modo univoco un database.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Membri

**ulRandom**

Numero assegnato in modo casuale.

**logtimeCrea**

Il [JET_LOGTIME](./jet-logtime-structure.md) al momento [dell'esecuzione di JetCreateDatabase.](./jetcreatedatabase-function.md)

**szComputerName**

Valore stringa facoltativo del nome NetBIOS per il computer. Questo valore non può essere impostato.

### <a name="remarks"></a>Commenti

Può essere trovato come elemento di JET_DBINFOMISC [.](./jet-dbinfomisc-structure.md)

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
