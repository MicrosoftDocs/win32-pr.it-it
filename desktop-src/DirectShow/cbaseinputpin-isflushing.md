---
description: Il metodo di svuotamento esegue una query per determinare se il filtro sta attualmente scaricando.
ms.assetid: 366b6162-7a2c-4882-8774-8b4bf83012b4
title: Metodo CBaseInputPin. IsValid (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsFlushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5af91e78d10f480596b8e0820ee6de4c4df2998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326061"
---
# <a name="cbaseinputpinisflushing-method"></a>Metodo CBaseInputPin. di scaricamento

Il `IsFlushing` metodo esegue una query per determinare se il filtro sta attualmente scaricando.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsFlushing();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la variabile membro [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




