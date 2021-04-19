---
description: 'Il metodo NewSegment notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come un segmento. Implementa il metodo IPin:: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Metodo CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328511"
---
# <a name="cbasepinnewsegment-method"></a>CBasePin. NewSegment, metodo

Il `NewSegment` metodo notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento. Implementa il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT NewSegment(
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

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta le variabili membro [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md)e [**CBasePin:: m \_ drate**](cbasepin-m-drate.md) . Nella classe derivata eseguire l'override di questo metodo per passare la notifica downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




