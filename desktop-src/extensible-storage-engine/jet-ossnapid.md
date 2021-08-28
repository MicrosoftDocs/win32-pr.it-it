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
ms.openlocfilehash: d6185f17c16cbdb2a45e172a14af346c3519aa12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468368"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

Il **JET_OSSNAPID** di dati contiene un handle per uno snapshot del database.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Tipi di dati

JET_OSSNAPID

Handle per uno snapshot del database. Questo handle viene usato negli elementi dell'API JET coinvolti nel backup dello snapshot.

**È** possibile usare NULL per indicare un handle non valido.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


