---
description: Il metodo NewSegment notifica al filtro che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Metodo CTransformFilter.NewSegment (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2cb83c376b012ae3474f87b0f8d26c7fb5560812c1d8ddcbb3ea62293797bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953550"
---
# <a name="ctransformfilternewsegment-method"></a>Metodo CTransformFilter.NewSegment

Il `NewSegment` metodo notifica al filtro che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStart* 
</dt> <dd>

Ora di inizio del segmento, rispetto all'origine originale.

</dd> <dt>

*tStop* 
</dt> <dd>

Ora di arresto del segmento rispetto all'origine originale.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocità di elaborazione del segmento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) del pin di input chiama questo metodo. Questo metodo recapita la `NewSegment` chiamata al pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




