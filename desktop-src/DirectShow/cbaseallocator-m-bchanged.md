---
description: Flag che indica se i requisiti del buffer sono stati modificati.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: Membro CBaseAllocator::m_bChanged (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7edb5ed770628d7dfd982017e720ef0136bace74dd7e311121925f6c8657d2fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131501"
---
# <a name="cbaseallocatorm_bchanged-member"></a>Membro CBaseAllocator::m \_ bChanged

Flag che indica se i requisiti del buffer sono stati modificati. Il [**metodo CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) imposta il valore su **TRUE.** In una classe derivata, il metodo virtuale [**puro CBaseAllocator::Alloc**](cbaseallocator-alloc.md) deve impostare nuovamente il valore su **FALSE.** Dopo aver allocato i buffer, non è necessario riallocarli mentre *m \_ bChanged* è **FALSE.**

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




