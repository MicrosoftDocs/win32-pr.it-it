---
description: Il metodo ScheduleSample pianifica un esempio per il rendering.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Metodo CBaseRenderer.ScheduleSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88e728b90078ab11a6215dad60a88b819b2c513071637e2aa5c6b6ed7226189b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157593"
---
# <a name="cbaserendererschedulesample-method"></a>Metodo CBaseRenderer.ScheduleSample

Il `ScheduleSample` metodo pianifica un esempio per il rendering.

## <a name="syntax"></a>Sintassi


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'esempio è stato pianificato oppure **FALSE** se l'esempio è stato eliminato.

## <a name="remarks"></a>Commenti

Questo metodo determina innanzitutto se il rendering dell'esempio deve essere eseguito immediatamente, sottoposto a rendering in futuro o eliminato. A tale scopo, chiama il [**metodo CBaseRenderer::GetSampleTimes.**](cbaserenderer-getsampletimes.md) Se il rendering dell'esempio deve essere eseguito immediatamente, il metodo segnala l'evento [**\_ RenderEvent di CBaseRenderer::m.**](cbaserenderer-m-renderevent.md) Se il rendering dell'esempio deve essere eseguito in futuro, il metodo chiama il metodo [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) per la pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




