---
description: 'Altre informazioni su: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: 82be9a4aa00f1880493d81dbcd53d1d8d76cc46a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983804"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

Il **JET_OSSNAPID** dati contiene un handle per uno snapshot del database.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Tipi di dati

JET_OSSNAPID

Handle per uno snapshot del database. Questo handle viene utilizzato negli elementi dell'API JET coinvolti nel backup di snapshot.

**È** possibile usare NULL per indicare un handle non valido.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


