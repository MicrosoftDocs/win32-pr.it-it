---
description: Il metodo nobattistrada segnala che una transizione di stato non è ancora completa.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Metodo CBaseRenderer. nobattistrada (Renbase. h)
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
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333360"
---
# <a name="cbaserenderernotready-method"></a>CBaseRenderer. nobattistrada (metodo)

Il `NotReady` metodo segnala che una transizione di stato non è ancora completa.

## <a name="syntax"></a>Sintassi


```C++
void NotReady();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo fa sì che il metodo [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) restituisca il metodo \_ \_ intermedio di stato di VFW \_ , che indica che il filtro sta ancora passando allo stato corrente. Il filtro chiama questo metodo ogni volta che una transizione di stato è in sospeso. Questo errore si verifica quando il filtro viene sospeso fino a quando non riceve un campione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




