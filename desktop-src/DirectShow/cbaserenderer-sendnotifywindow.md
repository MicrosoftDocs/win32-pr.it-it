---
description: Il metodo SendNotifyWindow invia una notifica al filtro upstream dell'handle della finestra video.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Metodo CBaseRenderer.SendNotifyWindow (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4956ad2b20040b0d22903d2ffaa2c7b460af9250fe057d106db545173d53a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157498"
---
# <a name="cbaserenderersendnotifywindow-method"></a>Metodo CBaseRenderer.SendNotifyWindow

Il `SendNotifyWindow` metodo invia una notifica al filtro upstream dell'handle della finestra video.

## <a name="syntax"></a>Sintassi


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di output del filtro upstream.

</dd> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra video o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il pin di output del filtro upstream supporta [**l'interfaccia IMediaEventSink,**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) questo metodo invia il codice evento [**EC NOTIFY \_ \_ WINDOW**](ec-notify-window.md) insieme all'handle della finestra.

I renderer video possono eseguire l'override [**dei metodi CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) per chiamare questo metodo. Fornisce un meccanismo per informare il filtro upstream dell'handle di finestra. In questo caso, eseguire l'override anche del metodo [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) e chiamare `SendNotifyWindow` con un handle **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




