---
description: "Metodo CTransformInputPin.EndFlush: il metodo EndFlush termina un'operazione di scaricamento. Questo metodo implementa il metodo IPin::EndFlush."
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Metodo CTransformInputPin.EndFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095059"
---
# <a name="ctransforminputpinendflush-method"></a>Metodo CTransformInputPin.EndFlush

Il `EndFlush` metodo termina un'operazione di scaricamento. Questo metodo implementa il [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin di output non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) del filtro per recapitare la chiamata a valle. Chiama quindi il metodo [**CBaseInputPin::EndFlush del**](cbaseinputpin-endflush.md) pin.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




