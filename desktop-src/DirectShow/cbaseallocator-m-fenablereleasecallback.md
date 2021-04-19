---
description: "Flag che indica se il callback di rilascio è abilitato. Questo flag viene impostato nel metodo del costruttore. Se il valore è FALSE, la chiamata al metodo CBaseAllocator:: senotify comporta l'attivazione di un'asserzione (nelle build di debug)."
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Membro CBaseAllocator:: m_fEnableReleaseCallback (Amfilter. h)'
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
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333379"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>Membro fEnableReleaseCallback di CBaseAllocator:: m \_

Flag che indica se il callback di rilascio è abilitato. Questo flag viene impostato nel metodo del costruttore. Se il valore è **false**, la chiamata al metodo [**CBaseAllocator:: senotify**](cbaseallocator-setnotify.md) comporta l'attivazione di un'asserzione (nelle build di debug).

## <a name="syntax"></a>Sintassi


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




