---
description: Il metodo AsynchronousBlockOutputPin blocca il pin. Il metodo potrebbe restituire prima che il pin venga bloccato.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Metodo CDynamicOutputPin.AsynchronousBlockOutputPin (Amfilter.h)
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
ms.openlocfilehash: c8999f6dbb42c55c036ee3d7fcd02dc34def4bd0a036cf0b5d908d3c280e297e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317791"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>Metodo CDynamicOutputPin.AsynchronousBlockOutputPin

Il `AsynchronousBlockOutputPin` metodo blocca il pin. Il metodo potrebbe restituire prima che il pin venga bloccato.

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

Handle per un evento. L'evento viene segnalato quando il pin di output è bloccato o se il chiamante annulla l'operazione di blocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                                                    | Descrizione                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Operazione completata.<br/>                                      |
| <dl> <dt>**PIN \_ VFW E \_ GIÀ \_ \_ BLOCCATO**</dt> </dl>                   | L'aggiunta è già bloccata in un altro thread.<br/>     |
| <dl> <dt>**IL \_ PIN VFW E È GIÀ BLOCCATO IN QUESTO \_ \_ \_ \_ \_ \_ THREAD**</dt> </dl> | Il pin è già bloccato nel thread chiamante.<br/> |



 

## <a name="remarks"></a>Commenti

Non chiamare questo metodo dal thread di streaming.

Se nessun thread di streaming usa il pin, questo metodo blocca immediatamente il pin. In caso contrario, imposta lo stato del pin su "pending" e restituisce . Al termine dell'operazione di streaming, il thread di streaming chiama il metodo [**CDynamicOutputPin::StopUsingOutputPin,**](cdynamicoutputpin-stopusingoutputpin.md) che blocca il pin e segnala **l'evento hNotifyCallerPinBlockedEvent.** Per annullare un blocco in sospeso, chiamare il [**metodo CDynamicOutputPin::UnblockOutputPin.**](cdynamicoutputpin-unblockoutputpin.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




