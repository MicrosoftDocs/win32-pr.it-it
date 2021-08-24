---
description: Il metodo NewSegment notifica al pin che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento. Questo metodo implementa il metodo IPin::NewSegment.
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Metodo CTransformInputPin.NewSegment (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c522755fe898717f0c06af9698be07ab2ebca491666982d6ff62756ef48ae08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907421"
---
# <a name="ctransforminputpinnewsegment-method"></a>Metodo CTransformInputPin.NewSegment

Il `NewSegment` metodo notifica al pin che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento. Questo metodo implementa il [**metodo IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

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

Ora di inizio del segmento.

</dd> <dt>

*tStop* 
</dt> <dd>

Ora di arresto del segmento.

</dd> <dt>

*dRate* 
</dt> <dd>

Frequenza del segmento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::NewSegment.**](cbasepin-newsegment.md) Chiama il metodo [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) del filtro per recapitare la chiamata a valle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




