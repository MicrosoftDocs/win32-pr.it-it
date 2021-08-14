---
description: Questo argomento si applica Windows XP Service Pack 2 o versione successiva. La struttura KSTOPOLOGY CONNECTION descrive una connessione di nodo \_ all'interno di un filtro di streaming del kernel (KS). Un nodo può essere connesso a un altro nodo all'interno del filtro o a un segnaposto nel filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION struttura (Ks.h)
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
ms.openlocfilehash: 80a7b6f046edd1cd7f602487a11d6a79c375276814f9374f4142d148699bb8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397245"
---
# <a name="kstopology_connection-structure"></a>Struttura KSTOPOLOGY \_ CONNECTION

Questo argomento si applica Windows XP Service Pack 2 o versione successiva.

La **struttura KSTOPOLOGY \_ CONNECTION** descrive una connessione di nodo all'interno di un filtro di streaming del kernel (KS). Un nodo può essere connesso a un altro nodo all'interno del filtro o a un segnaposto nel filtro.

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

**Fromnode**
</dt> <dd>

Indice del nodo upstream nella connessione. Se la connessione upstream è un pin, anziché un nodo, il valore è KSFILTER \_ NODE.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Se il valore del **campo FromNode** è KSFILTER NODE, questo campo \_ specifica l'indice del pin upstream. In caso contrario, questo campo viene ignorato.

</dd> <dt>

**ToNode**
</dt> <dd>

Indice del nodo downstream nella connessione. Se la connessione downstream è un pin, anziché un nodo, il valore è KSFILTER \_ NODE.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Se il valore del **campo ToNode** è KSFILTER NODE, questo campo \_ specifica l'indice del pin downstream. In caso contrario, questo campo viene ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Strutture](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo::get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




