---
description: Ricerca di funzionalità.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: Membro CSourceSeeking::m_dwSeekingCaps (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98044f8a05c22022f66e6014be591d99ec57451e33e8f2d7d464e6793bec19e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054031"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Membro CSourceSeeking::m \_ dwSeekingCaps

Ricerca di funzionalità.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Osservazioni

Per impostazione predefinita, il valore è impostato sulla combinazione bit per bit dei flag seguenti:

-   AM \_ SEEKING \_ CanSeekForwards
-   AM \_ SEEKING \_ CanSeekBackwards
-   AM \_ SEEKING \_ CanSeekAbsolute
-   AM \_ SEEKING \_ CanGetStopPos
-   AM \_ SEEKING \_ CanGetDuration

Se il filtro supporta un set diverso di funzionalità, eseguire l'override di questo valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




