---
description: Il metodo SESINK imposta l'oggetto IQualityControl che riceverà i messaggi di qualità.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Metodo CBaseVideoRenderer. SESINK (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325347"
---
# <a name="cbasevideorenderersetsink-method"></a>Metodo CBaseVideoRenderer. SESINK

Il `SetSink` metodo imposta l'oggetto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) che riceverà i messaggi di qualità.

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

Puntatore all'oggetto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) a cui devono essere inviate le notifiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IQualityControl::**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) SetValue nel renderer video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




