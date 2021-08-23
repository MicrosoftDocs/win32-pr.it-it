---
description: Il metodo EndOfStream viene chiamato dopo che l'oggetto ha fornito l'ultimo esempio. La classe derivata deve implementare questo metodo.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Metodo CPullPin.EndOfStream (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9544a5f35c42fcf65bff58ad63d6f22bdd4dd817ae91951b01ffe122bce50c5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954020"
---
# <a name="cpullpinendofstream-method"></a>Metodo CPullPin.EndOfStream

Il `EndOfStream` metodo viene chiamato dopo che l'oggetto ha fornito l'ultimo esempio. La classe derivata deve implementare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Usare questo metodo per chiamare [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) su ogni pin di input downstream che riceve i dati da questo oggetto. Se i pin di output del filtro derivano da [**CBaseOutputPin,**](cbaseoutputpin.md)chiamare il metodo [**CBaseOutputPin::D eliverEndOfStream.**](cbaseoutputpin-deliverendofstream.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




