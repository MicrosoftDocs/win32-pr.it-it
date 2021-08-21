---
description: Il metodo NewSegment notifica al pin che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento. Implementa il metodo IPin::NewSegment.
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Metodo CBasePin.NewSegment (Amfilter.h)
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
ms.openlocfilehash: ed3ffc9cc0656509b29a6c32baeaf7311437a79e8402fbae0727cf9f93a30abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384551"
---
# <a name="cbasepinnewsegment-method"></a>Metodo CBasePin.NewSegment

Il `NewSegment` metodo notifica al pin che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento. Implementa il [**metodo IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

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

Posizione media iniziale del segmento, in unità da 100 nanosecondi.

</dd> <dt>

*tStop* 
</dt> <dd>

Posizione media finale del segmento, in unità da 100 nanosecondi.

</dd> <dt>

*dRate* 
</dt> <dd>

Frequenza con cui deve essere elaborato questo segmento, come percentuale della velocità originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta le variabili membro [**CBasePin::m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin::m \_ tStop**](cbasepin-m-tstop.md)e [**CBasePin::m \_ dRate.**](cbasepin-m-drate.md) Nella classe derivata eseguire l'override di questo metodo per passare la notifica a valle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




