---
description: Il metodo NewSegment notifica al filtro che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come un segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Metodo CTransformFilter. NewSegment (Transfrm. h)
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
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331133"
---
# <a name="ctransformfilternewsegment-method"></a>CTransformFilter. NewSegment, metodo

Il `NewSegment` metodo notifica al filtro che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento.

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

Ora di inizio del segmento rispetto all'origine originale.

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

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CTransformInputPin:: NewSegment**](ctransforminputpin-newsegment.md) del PIN di input chiama questo metodo. Questo metodo recapita la `NewSegment` chiamata al pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




