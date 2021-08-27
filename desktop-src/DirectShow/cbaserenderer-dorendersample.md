---
description: Il metodo DoRenderSample esegue il rendering di un esempio.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Metodo CBaseRenderer.DoRenderSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef91e7ad27d008f5dfdb83e5642ecba8ec68bc424824dca9c8aa068ec055f24f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076431"
---
# <a name="cbaserendererdorendersample-method"></a>Metodo CBaseRenderer.DoRenderSample

Il `DoRenderSample` metodo esegue il rendering di un esempio.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo. Il comportamento dipende interamente dal tipo di filtro implementato. Un renderer video, ad esempio, disegna l'immagine video contenuta nell'esempio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




