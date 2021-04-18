---
description: Il metodo ShouldDrawSampleNow determina se il video deve essere disegnato senza impostare un collegamento di notifica del timer con il clock.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Metodo CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325346"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>CBaseVideoRenderer. ShouldDrawSampleNow, metodo

Il `ShouldDrawSampleNow` metodo determina se il video deve essere disegnato senza impostare un collegamento di notifica del timer con il clock.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) per l'esempio.

</dd> <dt>

*ptrStart* 
</dt> <dd>

Puntatore al momento in cui iniziare il rendering.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Puntatore al tempo necessario per arrestare il rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Restituisce \_ OK per indicare un valore di estrazione in una sola volta senza attendere, S \_ false per indicare il valore di *ptrStart* per ora, oppure un errore per indicare che non è possibile creare l'esempio, ovvero ignorarlo per risparmiare tempo.

## <a name="remarks"></a>Commenti

Questa funzione membro esegue l'override di [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




