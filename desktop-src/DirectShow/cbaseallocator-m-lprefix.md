---
description: Prefisso di ogni buffer, in byte.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: Membro CBaseAllocator::m_lPrefix (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a22f2ac1a54c4820f109b55002428c87df321328ef6b6b6d6096343df8cde85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955290"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Membro CBaseAllocator::m \_ lPrefix

Prefisso di ogni buffer, in byte. Se il valore è diverso da zero, ogni puntatore al buffer restituito dal metodo [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) è preceduto da un blocco di byte di dimensioni *m \_ lPrefix*. Questo blocco di memoria è denominato *prefisso*. La [**variabile membro CBaseAllocator::m \_ lSize**](cbaseallocator-m-lsize.md) non include il valore del prefisso.

## <a name="syntax"></a>Sintassi


```C++
long m_lPrefix;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




