---
description: Il metodo SendNotifyWindow invia una notifica al filtro upstream dell'handle della finestra video.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Metodo CBaseRenderer. SendNotifyWindow (Renbase. h)
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
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326427"
---
# <a name="cbaserenderersendnotifywindow-method"></a>CBaseRenderer. SendNotifyWindow, metodo

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

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output del filtro upstream.

</dd> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra video o **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il pin di output del filtro upstream supporta l'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , questo metodo invia il codice evento [**della \_ \_ finestra di notifica EC**](ec-notify-window.md) insieme all'handle della finestra.

I renderer video possono eseguire l'override dei metodi [**CBaseRenderer:: CompleteConnect**](cbaserenderer-completeconnect.md) per chiamare questo metodo. Fornisce un meccanismo per informare il filtro upstream dell'handle della finestra. In tal caso, eseguire l'override anche del metodo [**CBaseRenderer:: BreakConnect**](cbaserenderer-breakconnect.md) e chiamare `SendNotifyWindow` con un handle **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




