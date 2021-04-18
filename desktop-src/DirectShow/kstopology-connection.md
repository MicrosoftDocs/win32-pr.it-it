---
description: Questo argomento si applica a Windows XP Service Pack 2 o versioni successive. La \_ struttura di connessione KSTOPOLOGY descrive una connessione nodo all'interno di un filtro di streaming kernel (KS). Un nodo può essere connesso a un altro nodo all'interno del filtro o a un pin sul filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: Struttura KSTOPOLOGY_CONNECTION (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330389"
---
# <a name="kstopology_connection-structure"></a>\_Struttura di connessione KSTOPOLOGY

Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.

La struttura di **\_ connessione KSTOPOLOGY** descrive una connessione nodo all'interno di un filtro di streaming kernel (KS). Un nodo può essere connesso a un altro nodo all'interno del filtro o a un pin sul filtro.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a>Members

<dl> <dt>

**FromNode**
</dt> <dd>

Indice del nodo upstream nella connessione. Se la connessione upstream è un PIN, anziché un nodo, il valore è KSFILTER \_ node.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Se il valore del campo **FromNode** è KSFILTER \_ node, questo campo specifica l'indice del pin upstream. In caso contrario, questo campo viene ignorato.

</dd> <dt>

**ToNode**
</dt> <dd>

Indice del nodo downstream nella connessione. Se la connessione downstream è un PIN, anziché un nodo, il valore è KSFILTER \_ node.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Se il valore del campo **ToNode** è KSFILTER \_ , questo campo specifica l'indice del pin downstream. In caso contrario, questo campo viene ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DirectShow](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo:: Get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




