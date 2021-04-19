---
description: Il metodo Ready segnala che una transizione di stato è stata completata.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Metodo CBaseRenderer. Ready (Renbase. h)
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
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333339"
---
# <a name="cbaserendererready-method"></a>Metodo CBaseRenderer. Ready

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

Questo metodo fa sì che il metodo [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) restituisca S \_ OK, a indicare che il filtro ha completato la transizione allo stato corrente. Il filtro chiama questo metodo ogni volta che viene completata una transizione di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer:: nobattistrada**](cbaserenderer-notready.md)
</dt> </dl>

 

 




