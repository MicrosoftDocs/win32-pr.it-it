---
description: Il metodo BlockOutputPin blocca il pin.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Metodo CDynamicOutputPin.BlockOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc1f4cdafd732821398ee04e127c0525798dd6cc02f67f8af5d977b195a6a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983361"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>Metodo CDynamicOutputPin.BlockOutputPin

Il `BlockOutputPin` metodo blocca il pin. Mentre il pin è bloccato, il metodo [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) attende che il pin diventi sbloccato. Lo stato bloccato impedisce al pin di output di fornire esempi, modificarne il formato di output o riconnettersi.

## <a name="syntax"></a>Sintassi


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, mantenere la [**sezione critica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md) Non chiamare questo metodo se un thread di streaming usa il pin, per recapitare i dati o per modificare la connessione. Per verificare se un thread di streaming usa il pin, chiamare il metodo [**CDynamicOutputPin::StreamingThreadUsingOutputPin.**](cdynamicoutputpin-streamingthreadusingoutputpin.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




