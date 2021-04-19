---
description: Il metodo InputPin recupera un puntatore al pin di input del filtro.
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: Metodo CTransInPlaceFilter. InputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b92775eca87a88659326aa5b34eb0c15109ed8a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326392"
---
# <a name="ctransinplacefilterinputpin-method"></a>CTransInPlaceFilter. InputPin, metodo

Il `InputPin` metodo recupera un puntatore al pin di input del filtro.

## <a name="syntax"></a>Sintassi


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la variabile membro [**CTransformFilter:: m \_ Pinput**](ctransformfilter-m-pinput.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




