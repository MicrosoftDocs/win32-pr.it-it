---
description: Durata del flusso. Per impostazione predefinita, il valore è impostato sul valore della variabile membro CSourceSeeking::m \_ rtStop.
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: Membro CSourceSeeking::m_rtDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6aa62a3cdf906a4e9666b7786c08e49fca250ef042d187902132410cc2f0abaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053971"
---
# <a name="csourceseekingm_rtduration-member"></a>Membro CSourceSeeking::m \_ rtDuration

Durata del flusso. Per impostazione predefinita, il valore è impostato sul valore della variabile membro [**CSourceSeeking::m \_ rtStop.**](csourceseeking-m-rtstop.md)

## <a name="syntax"></a>Sintassi


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Osservazioni

Mantenere la **sezione \_ critica m pLock** prima di accedere a questa variabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




