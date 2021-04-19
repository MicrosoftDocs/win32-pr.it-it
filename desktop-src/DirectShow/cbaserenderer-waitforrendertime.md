---
description: Il metodo WaitForRenderTime attende l'ora di presentazione dell'esempio corrente.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Metodo CBaseRenderer. WaitForRenderTime (Renbase. h)
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
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324193"
---
# <a name="cbaserendererwaitforrendertime-method"></a>CBaseRenderer. WaitForRenderTime, metodo

Il `WaitForRenderTime` metodo attende l'ora di presentazione dell'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                           | Descrizione                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                                                       |
| <dl> <dt>**stato di VFW \_ E \_ \_ modificato**</dt> </dl> | Lo stato del filtro è stato modificato prima dell'arrivo dell'ora di presentazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo attende fino a quando si verifica una delle condizioni seguenti:

-   Il tempo di presentazione dell'esempio arriva, a quel punto è possibile eseguire il rendering dell'esempio.
-   Il filtro interrompe o inizia a scaricare i dati.

Se l'ora di presentazione arriva, viene segnalato l'evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) . Se lo stato viene modificato, viene segnalato l'evento [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) . Questo metodo attende entrambi gli eventi. La classe derivata può eseguire l'override di questo metodo per attendere eventi aggiuntivi, se necessario.

Questo metodo chiama il metodo [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) all'inizio dell'attesa e il metodo [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) al termine dell'attesa. Nessuno dei due metodi esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




