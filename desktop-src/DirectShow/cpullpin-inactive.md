---
description: Il metodo Inactive arresta il thread di lavoro che estrae i dati dal pin di output. Questo metodo disaccosta anche l'allocatore.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Metodo CPullPin.Inactive (Pullpin.h)
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
ms.openlocfilehash: 56307362651761dbe2bc5c0242a24f189cf14d1e820df6a5ba21bdeb9c7deb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565371"
---
# <a name="cpullpininactive-method"></a>Metodo CPullPin.Inactive

Il `Inactive` metodo arresta il thread di lavoro che esegue il pull dei dati dal pin di output. Questo metodo disaccosta anche l'allocatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Chiamare questo metodo quando il filtro proprietario diventa inattivo. Se il pin di input deriva da [**CBasePin,**](cbasepin.md)eseguire l'override del [**metodo CBasePin::Inactive.**](cbasepin-inactive.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




