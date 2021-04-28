---
description: "Metodo CRenderedInputPin.EndFlush: il metodo EndFlush termina un'operazione di scaricamento. Questo metodo implementa il metodo IPin::EndFlush."
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Metodo CRenderedInputPin.EndFlush (Amextra.h)
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
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098919"
---
# <a name="crenderedinputpinendflush-method"></a>Metodo CRenderedInputPin.EndFlush

Il `EndFlush` metodo termina un'operazione di scaricamento. Questo metodo implementa il [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo cancella tutti gli eventi [**EC \_ COMPLETE in**](ec-complete.md) sospeso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




