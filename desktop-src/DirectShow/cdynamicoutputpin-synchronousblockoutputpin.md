---
description: Il metodo SynchronousBlockOutputPin blocca il pin. non restituisce finché il pin non viene bloccato.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Metodo CDynamicOutputPin.SynchronousBlockOutputPin (Amfilter.h)
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
ms.openlocfilehash: d8613a27d8af2dc2b69a93a1f324db17b054cf2dd312fdb0c9d6cd63e6c89ca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916311"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>Metodo CDynamicOutputPin.SynchronousBlockOutputPin

Il `SynchronousBlockOutputPin` metodo blocca il pin; non restituisce finché il pin non viene bloccato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                                                    | Descrizione                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Operazione completata.<br/>                                      |
| <dl> <dt>**PIN VFW \_ E \_ GIÀ \_ \_ BLOCCATO**</dt> </dl>                   | L'aggiunta è già bloccata in un altro thread.<br/>     |
| <dl> <dt>**IL \_ PIN VFW E È GIÀ BLOCCATO IN QUESTO \_ \_ \_ \_ \_ \_ THREAD**</dt> </dl> | Il pin è già bloccato nel thread chiamante.<br/> |



 

## <a name="remarks"></a>Commenti

Non chiamare questo metodo dal thread di streaming.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




