---
description: Il metodo ShouldDrawSampleNow determina se il video deve essere disegnato senza impostare un collegamento di consigli del timer con l'orologio.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Metodo CBaseVideoRenderer.ShouldDrawSampleNow (Renbase.h)
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
ms.openlocfilehash: e3c0297ccf670de12380c5f02af2c67d6050bac29dd1fa7e7e89a6e6c7c20592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074686"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>Metodo CBaseVideoRenderer.ShouldDrawSampleNow

Il `ShouldDrawSampleNow` metodo determina se il video deve essere disegnato senza impostare un collegamento di consulenza del timer con l'orologio.

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

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) per l'esempio.

</dd> <dt>

*ptrStart* 
</dt> <dd>

Puntatore all'ora di inizio del rendering.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Puntatore all'ora in cui arrestare il rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Restituisce S OK per indicare il disegno in una sola volta senza attendere, S FALSE per indicare il disegno in fase \_ \_ di *ptrStart* o un errore per indicare che non disegnare il campione; in altri caso, ignorarlo per risparmiare tempo.

## <a name="remarks"></a>Commenti

Questa funzione membro esegue l'override di [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




