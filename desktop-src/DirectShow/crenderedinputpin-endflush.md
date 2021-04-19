---
description: "Il metodo EndFlush termina un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: EndFlush."
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Metodo CRenderedInputPin. EndFlush (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329366"
---
# <a name="crenderedinputpinendflush-method"></a>CRenderedInputPin. EndFlush, metodo

Il `EndFlush` metodo termina un'operazione di svuotamento. Questo metodo implementa il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esito è positivo o un codice di errore.

## <a name="remarks"></a>Commenti

Questo metodo cancella tutti gli eventi di [**\_ completamento EC**](ec-complete.md) in sospeso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




