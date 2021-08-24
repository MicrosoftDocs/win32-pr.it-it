---
description: Il metodo Pause sospende il filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Metodo CBaseRenderer.Pause (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9769a1243fdbd69037e275fc083a9b1b0766f7f404190b2e68920f238e2bf140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586081"
---
# <a name="cbaserendererpause-method"></a>Metodo CBaseRenderer.Pause

Il `Pause` metodo sospende il filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | La transizione è stata completata.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La transizione non è completa.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseFilter::P ause.**](cbasefilter-pause.md) Esegue i passaggi seguenti:

-   Chiama il **metodo CBaseFilter::P ause.**
-   Esegue il commit dell'allocatore. Vedere [**IMemAllocator::Commit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)
-   Se lo stato precedente è stato arrestato, il filtro rilascia qualsiasi esempio che contiene. L'esempio non è più valido.
-   Chiama il [**metodo CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) e restituisce il valore .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




