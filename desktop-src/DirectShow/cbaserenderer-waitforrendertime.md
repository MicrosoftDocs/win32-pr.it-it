---
description: Il metodo WaitForRenderTime attende l'ora di presentazione dell'esempio corrente.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Metodo CBaseRenderer.WaitForRenderTime (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e590a09c2c6d4cc34728f5ec29db0d8f650d3a1e9cb663e5993acd2cebe4793f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157356"
---
# <a name="cbaserendererwaitforrendertime-method"></a>Metodo CBaseRenderer.WaitForRenderTime

Il `WaitForRenderTime` metodo attende l'ora di presentazione dell'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                           | Descrizione                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                                                       |
| <dl> <dt>**STATO DI VFW \_ E \_ \_ MODIFICATO**</dt> </dl> | Lo stato del filtro è cambiato prima dell'arrivo dell'ora di presentazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo attende fino a quando non si verifica una delle condizioni seguenti:

-   Arriva l'ora di presentazione dell'esempio, a questo punto è possibile eseguire il rendering dell'esempio.
-   Il filtro arresta o inizia a scaricare i dati.

Se arriva l'ora di presentazione, viene segnalato [**l'evento \_ RenderEvent CBaseRenderer::m.**](cbaserenderer-m-renderevent.md) Se lo stato cambia, viene segnalato [**l'evento CBaseRenderer::m \_ ThreadSignal.**](cbaserenderer-m-threadsignal.md) Questo metodo attende entrambi gli eventi. La classe derivata può eseguire l'override di questo metodo per attendere eventi aggiuntivi, se necessario.

Questo metodo chiama il [**metodo CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) all'inizio dell'attesa e il metodo [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) al termine dell'attesa. Nessuno dei due metodi esegue qualsiasi operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




