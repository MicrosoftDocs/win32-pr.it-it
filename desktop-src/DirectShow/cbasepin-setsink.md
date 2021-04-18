---
description: 'Il metodo SESINK imposta un gestore di qualità esterno. Questo metodo implementa il metodo IQualityControl:: SetValue.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Metodo CBasePin. SESINK (Amfilter. h)
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
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327347"
---
# <a name="cbasepinsetsink-method"></a>Metodo CBasePin. SESINK

Il `SetSink` metodo imposta un gestore di qualità esterno. Questo metodo implementa il metodo [**IQualityControl::**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) SetValue.

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

Puntatore all'interfaccia [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) del gestore qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Chiamare questo metodo per reindirizzare i messaggi di controllo di qualità a un gestore di qualità esterno. Per altre informazioni, vedere [gestione del controllo di qualità](quality-control-management.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




