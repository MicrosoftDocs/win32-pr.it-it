---
description: Il metodo Ready segnala che una transizione di stato è stata completata.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Metodo CBaseRenderer.Ready (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a1870af825f2a33236d0fd86d0f730e0013df59297fec5cdaa2baf46a2b773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757521"
---
# <a name="cbaserendererready-method"></a>Metodo CBaseRenderer.Ready

Il `Ready` metodo segnala che una transizione di stato è stata completata.

## <a name="syntax"></a>Sintassi


```C++
void Ready();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo fa in modo che il metodo [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) restituisca S OK, che indica che il filtro ha completato la transizione \_ allo stato corrente. Il filtro chiama questo metodo ogni volta che completa una transizione di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer::NotReady**](cbaserenderer-notready.md)
</dt> </dl>

 

 




