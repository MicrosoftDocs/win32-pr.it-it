---
description: Il metodo AsynchronousBlockOutputPin blocca il PIN. Il metodo può restituire prima del blocco del PIN.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Metodo CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333464"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>CDynamicOutputPin. AsynchronousBlockOutputPin, metodo

Il `AsynchronousBlockOutputPin` metodo blocca il PIN. Il metodo può restituire prima del blocco del PIN.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hNotifyCallerPinBlockedEvent* 
</dt> <dd>

Handle per un evento. L'evento viene segnalato quando il pin di output è bloccato o se il chiamante Annulla l'operazione di blocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                                                    | Descrizione                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                           | Esito positivo.<br/>                                      |
| <dl> <dt>**\_pin VFW \_ E \_ già \_ bloccato**</dt> </dl>                   | Il PIN è già bloccato in un altro thread.<br/>     |
| <dl> <dt>**\_pin VFW \_ E \_ già \_ bloccato \_ in \_ questo \_ thread**</dt> </dl> | Il PIN è già bloccato nel thread chiamante.<br/> |



 

## <a name="remarks"></a>Commenti

Non chiamare questo metodo dal thread di streaming.

Se nessun thread di streaming usa il PIN, questo metodo blocca immediatamente il PIN. In caso contrario, lo stato del PIN viene impostato su "Pending" e viene restituito. Al termine dell'operazione di streaming, il thread di streaming chiama il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , che blocca il PIN e segnala l'evento **hNotifyCallerPinBlockedEvent** . Per annullare un blocco in sospeso, chiamare il metodo [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




