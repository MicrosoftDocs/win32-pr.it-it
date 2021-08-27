---
description: Flag che indica se il callback di versione è abilitato. Questo flag viene impostato nel metodo del costruttore. Se il valore è FALSE, la chiamata al metodo CBaseAllocator::SetNotify causa l'esecuzione di un'asserzione (nelle build di debug).
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: Membro CBaseAllocator::m_fEnableReleaseCallback (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2fc1dfebb051ddffffce341547562901153b47bd5da002ebd847965593a73d93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131461"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>Membro CBaseAllocator::m \_ fEnableReleaseCallback

Flag che indica se il callback di versione è abilitato. Questo flag viene impostato nel metodo del costruttore. Se il valore è **FALSE,** la chiamata al metodo [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) causa l'esecuzione di un'asserzione (nelle build di debug).

## <a name="syntax"></a>Sintassi


```C++
BOOL m_fEnableReleaseCallback;
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

 

 




