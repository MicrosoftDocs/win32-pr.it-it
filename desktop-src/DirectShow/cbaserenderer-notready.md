---
description: Il metodo NotReady segnala che una transizione di stato non è ancora stata completata.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Metodo CBaseRenderer.NotReady (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52fddcbd92544a109340697e5865f87e6c5f74a14b01543e768495b7717d8f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954830"
---
# <a name="cbaserenderernotready-method"></a>Metodo CBaseRenderer.NotReady

Il `NotReady` metodo segnala che una transizione di stato non è ancora stata completata.

## <a name="syntax"></a>Sintassi


```C++
void NotReady();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo fa in modo che il metodo [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) restituisca VFW S STATE INTERMEDIATE, che indica che il filtro è ancora in fase di transizione \_ allo stato \_ \_ corrente. Il filtro chiama questo metodo ogni volta che è in sospeso una transizione di stato. Ciò si verifica quando il filtro viene sospeso, fino a quando non riceve un campione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




