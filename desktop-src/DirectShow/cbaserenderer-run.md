---
description: Il metodo run esegue il filtro.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Metodo CBaseRenderer. Run (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333329"
---
# <a name="cbaserendererrun-method"></a>Metodo CBaseRenderer. Run

Il `Run` metodo esegue il filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseFilter:: Run**](cbasefilter-run.md) . Esegue le azioni seguenti:

-   Chiama il metodo **CBaseFilter:: Run** .
-   Viene eseguito il commit dell'allocatore. Vedere [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).
-   Se lo stato precedente è stato interrotto, il filtro rilascia tutti i campioni che contiene. (L'esempio non è più valido).
-   Chiama il metodo [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) e restituisce il risultato. Se un esempio è in sospeso, il metodo **StartStreaming** lo pianifica per il rendering.

Se il filtro non è connesso, invia immediatamente un evento [**EC \_ complete**](ec-complete.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




