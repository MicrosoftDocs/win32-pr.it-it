---
description: Il metodo SetSink imposta un gestore qualità esterno. Questo metodo implementa il metodo IQualityControl::SetSink.
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Metodo CBasePin.SetSink (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e94dc561e378ab526eee04f82e0f54a90889ee4396996d96d01f6c8da8c34d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108631"
---
# <a name="cbasepinsetsink-method"></a>Metodo CBasePin.SetSink

Il `SetSink` metodo imposta un gestore qualità esterno. Questo metodo implementa il [**metodo IQualityControl::SetSink.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piqc* 
</dt> <dd>

Puntatore [**all'interfaccia IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) del gestore qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Chiamare questo metodo per reindirizzare i messaggi di controllo qualità a un responsabile qualità esterno. Per altre informazioni, vedere [Quality-Control Management](quality-control-management.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




