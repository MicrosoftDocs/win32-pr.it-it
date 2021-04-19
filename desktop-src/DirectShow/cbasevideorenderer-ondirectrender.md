---
description: Il metodo OnDirectRender raccoglie informazioni sulla temporizzazione che controlla la sincronizzazione e il controllo della qualità.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Metodo CBaseVideoRenderer. OnDirectRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326562"
---
# <a name="cbasevideorendererondirectrender-method"></a>CBaseVideoRenderer. OnDirectRender, metodo

Il metodo **OnDirectRender** raccoglie informazioni sulla temporizzazione che controlla la sincronizzazione e il controllo della qualità.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Chiamare questo metodo anziché [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) e [**OnRenderEnd**](cbasevideorenderer-onrenderend.md). Questo metodo viene utilizzato dal renderer video DirectDraw.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




