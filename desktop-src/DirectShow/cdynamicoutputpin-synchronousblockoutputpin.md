---
description: Il metodo SynchronousBlockOutputPin blocca il PIN. non restituisce alcun risultato finché il PIN non viene bloccato.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Metodo CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333079"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>CDynamicOutputPin. SynchronousBlockOutputPin, metodo

Il `SynchronousBlockOutputPin` metodo blocca il PIN. non restituisce alcun risultato finché il PIN non viene bloccato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                                                    | Descrizione                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                           | Esito positivo.<br/>                                      |
| <dl> <dt>**\_pin VFW \_ E \_ già \_ bloccato**</dt> </dl>                   | Il PIN è già bloccato in un altro thread.<br/>     |
| <dl> <dt>**\_pin VFW \_ E \_ già \_ bloccato \_ in \_ questo \_ thread**</dt> </dl> | Il PIN è già bloccato nel thread chiamante.<br/> |



 

## <a name="remarks"></a>Commenti

Non chiamare questo metodo dal thread di streaming.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




