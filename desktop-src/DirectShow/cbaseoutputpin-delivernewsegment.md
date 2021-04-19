---
description: Il metodo DeliverNewSegment recapita una notifica del nuovo segmento al pin di input connesso.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Metodo CBaseOutputPin. DeliverNewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332064"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a>CBaseOutputPin. DeliverNewSegment, metodo

Il `DeliverNewSegment` Metodo recapita una notifica del nuovo segmento al pin di input connesso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStart* 
</dt> <dd>

Posizione iniziale del supporto del segmento, in unità di 100 nanosecondi.

</dd> <dt>

*tStop* 
</dt> <dd>

Posizione media finale del segmento, in unità da 100 nanosecondi.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocità di elaborazione del segmento, espresso come percentuale della frequenza originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>              |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il PIN non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




