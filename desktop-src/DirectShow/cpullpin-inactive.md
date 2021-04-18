---
description: Il metodo inattivo arresta il thread di lavoro che estrae i dati dal pin di output. Questo metodo consente inoltre di eseguire il commit dell'allocatore.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Metodo CPullPin. Inactive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331165"
---
# <a name="cpullpininactive-method"></a>Metodo CPullPin. Inactive

Il `Inactive` metodo arresta il thread di lavoro che estrae i dati dal pin di output. Questo metodo consente inoltre di eseguire il commit dell'allocatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Chiamare questo metodo quando il filtro proprietario diventa inattivo. Se il pin di input deriva da [**CBasePin**](cbasepin.md), eseguire l'override del metodo [**CBasePin:: inactive**](cbasepin-inactive.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




