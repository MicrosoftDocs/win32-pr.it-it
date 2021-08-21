---
description: Il metodo ResetStreamingTimes reimposta tutte le volte che controllano lo streaming.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Metodo CBaseVideoRenderer.ResetStreamingTimes (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bebf6f827cac883660b383b76f3a6ead7987e9fb468d0fd6f14205f59ad4d530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074775"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>Metodo CBaseVideoRenderer.ResetStreamingTimes

Il `ResetStreamingTimes` metodo reimposta tutte le volte che controllano lo streaming.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

I tempi vengono impostati in modo che i fotogrammi non verranno eliminati inizialmente e in modo che il primo frame verrà disegnato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




